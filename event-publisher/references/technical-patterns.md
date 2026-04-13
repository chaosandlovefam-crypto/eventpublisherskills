# Technical Patterns for Famies Dashboard Automation

## Browser Tab Setup

You need 3 tabs open:
1. **Famies Dashboard** — https://dashboard.famies.app/events
2. **Source Website** — The event calendar being scraped
3. **ChatGPT** — https://chatgpt.com (for image generation)

Use `tabs_context_mcp` to get tab IDs at the start. Reference tabs by their IDs throughout.

## Dashboard Navigation

### Getting to the Events Page
- Navigate to https://dashboard.famies.app/events
- If redirected to /dashboard, click "Events" in the left sidebar under "OPERATIONAL CONTENT"
- Direct URL navigation to /events/edit often redirects — use the sidebar

### Searching for Events
1. Click the search input field ("Search events by name...")
2. Type the event title (partial match works)
3. **Wait 2 seconds** for results to filter — this is critical
4. Verify only the expected events show in the list before clicking

The search field gets cleared when you navigate away and come back. Re-type the search term each time.

### Editing an Existing Event
1. Search for the event
2. Wait for results to filter
3. Click the three-dot menu (⋮) on the correct row
4. Click "Edit" from the dropdown
5. Make changes
6. Scroll to "Update Event" button and click it

### Blank Page Bug
Scrolling too far down on the edit page sometimes causes a blank white screen. Fix:
```javascript
window.scrollTo(0, 0);
```
Then use the `find` tool to locate the "Update Event" button by reference and click via `ref`.

### Finding and Clicking Buttons
For buttons below the fold (like "Update Event" or "Create Event"):
1. Use `find` tool: `find("Update Event button")` → gets a ref like `ref_1234`
2. Use `scroll_to` with the ref: `scroll_to(ref="ref_1234")`
3. Click via ref: `left_click(ref="ref_1234")`

This is more reliable than guessing coordinates.

## Creating an Event — Form Fields

### Event Information
- **Event Title**: Text input at the top
- **Description**: Rich text editor (supports H1, H2, H3, bold, italic, lists, quotes)

### Event Images
- **Images section**: Shows a "+" button to add images
- Click the "+" or use the file input programmatically (see Image Upload below)
- Click on an existing image thumbnail to remove it (shows red X)
- Images show "New" label after upload

### Organizer
- **Organizer dropdown**: Select an existing organizer or create new
- To create new: Click "Create Organizer" or the add button
- Fields: Name (required), Email (optional — skip if creation fails with email)
- Use specific names: "Bibliotek Vallentuna", "Kultur Vallentuna", "Vallentuna Kulturskola"
- Do NOT default to generic "Vallentuna kommun" when a specific name is available

### Venue
- **Venue dropdown**: Select existing or create new
- To create new: Click "Create Venue" or the add button
- Fields: Name (required), Address, Interest Category (required)
- **Municipality selection is NOT needed** — skip it
- **Interest Category IS required** — select the most relevant one

### Date Range
- **Start Date/Time** and **End Date/Time** fields
- For recurring events: Click "+ Add Date Range" to add more dates
- Create ONE event with multiple date ranges, not separate events

### Pricing
- Toggle between Free and Paid
- If paid, enter the price amount

### Call to Action (CTA)
- **CTA Text**: Set to "Läs mer"
- **CTA Link**: Set to the source event URL (where the event was scraped from)

### Push Notification
- **Default is ON** — you must manually toggle it OFF
- This is a switch/toggle control, find it and click to turn off

## Image Upload via JavaScript

The Famies dashboard uses a standard `<input type="file">` for image uploads. To upload
programmatically (e.g., from a URL), use the DataTransfer API:

```javascript
(async () => {
  const imageUrl = 'YOUR_IMAGE_URL_HERE';
  const resp = await fetch(imageUrl);
  const blob = await resp.blob();
  const file = new File([blob], 'event-image.jpg', { type: 'image/jpeg' });
  const input = document.querySelector('input[type="file"]');
  const dt = new DataTransfer();
  dt.items.add(file);
  input.files = dt.files;
  input.dispatchEvent(new Event('change', { bubbles: true }));
  return 'Image uploaded: ' + blob.size + ' bytes';
})();
```

For cross-origin images (like tmpfiles.org), use the wsrv.nl proxy:
```
https://wsrv.nl/?url=ENCODED_URL&w=500&h=500&fit=cover&output=jpg
```

## Downloading Source Images

To download an image from a source website and upload to tmpfiles.org:

```javascript
(async () => {
  const imgSrc = 'SOURCE_IMAGE_URL';
  const resp = await fetch(imgSrc);
  const blob = await resp.blob();
  const bitmap = await createImageBitmap(blob);
  const canvas = document.createElement('canvas');
  canvas.width = 500; canvas.height = 500;
  canvas.getContext('2d').drawImage(bitmap, 0, 0, 500, 500);
  const dataUrl = canvas.toDataURL('image/jpeg', 0.85);
  const arr = dataUrl.split(',');
  const bstr = atob(arr[1]);
  const u8arr = new Uint8Array(bstr.length);
  for (let i = 0; i < bstr.length; i++) u8arr[i] = bstr.charCodeAt(i);
  const uploadBlob = new Blob([u8arr], { type: 'image/jpeg' });
  const formData = new FormData();
  formData.append('file', uploadBlob, 'event-image.jpg');
  const uploadResp = await fetch('https://tmpfiles.org/api/v1/upload', { method: 'POST', body: formData });
  const json = await uploadResp.json();
  return JSON.stringify(json);
})();
```

## ChatGPT Image Generation

1. Switch to the ChatGPT tab
2. Find the message input and type the image generation prompt
3. Send the message and wait for the image to generate (can take 15-30 seconds)
4. Once generated, use the JavaScript pattern above to capture the image from ChatGPT
5. The captured image gets uploaded to tmpfiles.org for temporary hosting
6. Then transfer it to the Famies dashboard via the wsrv.nl proxy

## Error Handling

### Organizer creation fails
- Try creating without the email field
- Use an existing organizer if available

### Event save fails
- Scroll to top with `window.scrollTo(0, 0)`
- Check for validation errors (required fields highlighted)
- Ensure organizer and venue are selected
- Ensure at least one date range is set
- Ensure push notification toggle is visible and set correctly

### Image upload doesn't show
- Verify the file input element exists: `document.querySelector('input[type="file"]')`
- Check the blob size is > 0
- Try re-dispatching the change event

### Wrong event opened from search
- The search results hadn't filtered yet when you clicked
- Always wait 2+ seconds after typing before clicking the three-dot menu
- Verify the correct event name/ID is visible before clicking
