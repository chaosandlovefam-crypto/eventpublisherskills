# Famies Event Publishing - Exception Rules

## Rule #1: Duplicate Image Handling
**When:** Multiple events have the same image (same source image used for different events), making the app look repetitive and bad.

**Action:** Generate a unique, kid-friendly image using ChatGPT (already logged in on the browser).

**Image Prompt Format:**
```
authentic vertical 1:1 photo of Nordic children [activity/description-based keywords]
```

**Requirements:**
- Size: 500x500 (1:1 ratio) — this is the best size for Famies event cards
- Style: Authentic photo, NOT illustrated/cartoon
- Children: Nordic children specifically (targeted audience is Swedish kids and parents)
- Content: Based on the event description/activity (e.g., "reading books in a library", "playing piano", "painting outdoors")
- Always use "vertical 1:1" in the prompt

**Process:**
1. Detect if the same image is being used by multiple events
2. Keep the original image on ONE event
3. For the other event(s), go to ChatGPT in browser
4. Generate image with the prompt format above, tailored to that event's description
5. Download the generated image
6. Upload it to the event on the Famies dashboard (edit the event, replace image)

## Rule #2: Recurring Events — Single Event with Multiple Date Ranges
**When:** A source event has multiple dates (e.g., every Saturday in May, or specific recurring dates).

**Action:** Create ONLY ONE event on the Famies dashboard with multiple date ranges — do NOT create separate events for each date occurrence.

**Requirements:**
- One event = one title + one description + one image + one venue
- Multiple date ranges within that single event (use "Add Date Range" button for each date)
- Each date range should have the correct start and end time

**Process:**
1. Identify all dates for the recurring event from the source page
2. Create a single event with the first date
3. Use "+ Add Date Range" to add each additional date
4. Set the correct time (start and end) for each date range
5. Confirm all dates are added before publishing/updating

**Why:** Creating separate events for each date makes the app look cluttered and repetitive. Users see the same event multiple times, which is a bad experience. One event with multiple dates is cleaner.

## Rule #3: Text-Heavy Image Replacement
**When:** The source event's image contains prominent text (event titles, logos with text, banners with text, poster-style images). The Famies app uses 1:1 square image cards, so text-heavy images get cropped and look bad on mobile — text gets cut off and becomes unreadable.

**Action:** Do NOT use the source text-heavy image. Instead, generate a unique, kid-friendly image using ChatGPT based on the event description.

**How to Detect:**
- Image has large text/title overlaid on it (e.g., "LÄSMYS", "KLÄDBYTARDAGEN", poster-style)
- Image is a flyer/poster with event details as text
- Image where text is the primary visual element (not just a small watermark/logo)

**Image Prompt Format:**
```
authentic vertical 1:1 photo of Nordic children [activity based on event description]
```

**Requirements:**
- Same as Rule #1: Size 500x500, authentic photo style, Nordic children, based on description
- Generate a DIFFERENT style if this event's generated image might look similar to another nearby event's generated image
- The image should visually represent the EVENT ACTIVITY, not the text content

**Process:**
1. Check if the source event image is text-heavy
2. If yes, do NOT use it — generate a new image via ChatGPT
3. Use the event description to determine what activity to depict
4. Generate and upload the image to the Famies dashboard

**Why:** Text-heavy images get cropped in the 1:1 card layout on mobile, making them look unprofessional and unreadable. A clean activity-based photo looks much better on the Famies app.

## Rule #4: Skip Irrelevant / Senior-Only Events
**When:** The source event is clearly irrelevant to the Famies target audience (families with children, age range 0–49).

**Action:** Do NOT publish the event. Skip it entirely.

**Events to SKIP:**
- Events targeted at seniors (50–60+ years), e.g., "senior träff", "pensionärsaktivitet", events explicitly for elderly
- Events that are very irrelevant to families/children, e.g., lawyer help, legal advice ("advokat"), advocacy events
- Any event where the target audience is clearly NOT families or children/young people

**Events to PUBLISH (even if not explicitly for kids):**
- Events for age range 0–49 (children, teens, young adults, parents)
- General community/culture events that families could attend
- Events that don't specify a narrow senior-only audience

**Why:** Famies is a family app. Publishing senior-only or irrelevant professional events (lawyer, advocate) clutters the feed and confuses users. Only events relevant to families and younger audiences should be published.

## Rule #5: All Images Must Be Audience-Targeted (Kids + Parents)
**When:** ANY event image — whether from the source or AI-generated — is being used on the Famies dashboard.

**Core Principle:** The Famies app is for families with children (target: 0–12 years). Every image must feel relevant to THIS audience when users scroll the events feed. The image should not just represent the event topic generically — it must show kids and/or parents engaging with that topic.

**BAD examples (topic-only, no family connection):**
- Swedish flag alone for "Fira nationaldagen" → feels like a news article, not a family event
- Just birds or forest scenery for a nature event → no family connection
- A generic landscape or object photo → users scroll past, feels irrelevant

**GOOD examples (same topic BUT family-targeted):**
- "Fira nationaldagen" → Nordic kids waving small Swedish flags, families celebrating together outdoors
- Nature/bird event → A toddler pointing excitedly at a flying bird, parent and child birdwatching together
- Art exhibition → Kids painting at an easel, family looking at art together
- Music event → Children playing instruments, family dancing together

**Image Prompt Format (updated):**
```
authentic vertical 1:1 photo of Nordic children/families [engaging with the event activity in a way that feels warm, relatable, and relevant to parents browsing a family events app]
```

**Requirements:**
- ALWAYS include kids and/or parents in the image — never just objects, scenery, or flags alone
- The image must make a parent scrolling the Famies app think "this is for us / my kids would love this"
- Show ENGAGEMENT — kids doing, touching, watching, playing, reacting — not just standing
- Nordic children (Swedish target audience)
- Authentic photo style, 500x500, 1:1 ratio

**Apply this rule to:**
1. AI-generated images (Rule #1, #3) — always generate with family audience in mind
2. Source images that are generic/non-family — replace with a generated family-targeted image
3. Source images that already show kids/families engaging — keep as-is, these are perfect

**Why:** Famies users are parents looking for activities for their kids. When they scroll the events feed, every card image should immediately communicate "this is a family-friendly event." A Swedish flag or a lone bird doesn't do that. But kids waving flags or a child watching birds — that creates instant relevance and engagement.

## Rule #6: Missing Organizer/Venue — Use the Source Website
**When:** An event does not have a specific arranger/organizer name, or does not have a real physical address/venue.

**Action:** Use the SOURCE WEBSITE (where the event was scraped from) as both the organizer and the venue.

**Process:**
1. Check if the event has a specific organizer name (e.g., "Bibliotek Vallentuna", "Kultur Vallentuna") → If yes, use it
2. If NO specific organizer → Create an organizer using the source website name (e.g., "Vallentuna kommun" for vallentuna.se events)
3. Check if the event has a specific venue/address → If yes, use it
4. If NO specific venue/address → Create a venue using the source website name as the venue name
5. Then publish the event with these

**Example:**
- Source: vallentuna.se, event has no specific arranger or location
- Organizer: "Vallentuna kommun" (or use existing one if already created)
- Venue: "Vallentuna kommun" (or use existing one if already created)

**Why:** Every event on the Famies dashboard requires an organizer and a venue. When the source doesn't provide these details, the source website itself is the best fallback — it tells users where the event information came from.

## Rule #7: No Image Provided — Generate via ChatGPT
**When:** An event has all required information (title, description, date, venue, organizer) but the source does NOT provide any image.

**Action:** Generate a relevant, family-targeted image using ChatGPT, then use it to publish the event.

**Process:**
1. Notice the source event page has no image at all
2. Go to ChatGPT in the browser
3. Generate an image based on the event description, following Rule #5 (audience-targeted: kids + parents)
4. Upload the generated image to the Famies dashboard event
5. Publish the event as normal

**Image Prompt Format (same as Rule #5):**
```
authentic vertical 1:1 photo of Nordic children/families [engaging with the event activity]
```

**Requirements:**
- Follow all Rule #5 guidelines (kids/parents in image, engagement, Nordic, 500x500)
- Image must be relevant to the event topic/activity
- Never publish an event without an image — always generate one if missing

**Why:** Every event on Famies needs an image for the card layout. A missing image would break the UI or look unprofessional. Generating a relevant family-targeted image ensures consistent quality across all events.


## Rule #8: City-Aware Duplicate Check (Multi-City Context)

**When:** Working with event sources from multiple cities (27+ Swedish municipalities). A single event title may exist on the dashboard but belong to a DIFFERENT city than the one currently being processed.

**Action:** Before skipping an event as a "duplicate", verify the existing event belongs to the SAME city as the one being published. If it's from a different city, it is NOT a duplicate — publish the new event.

**The Problem:**
Yesterday published "Bim Bam Bom" under Vallentuna kommun. Today processing Haninge kommun — the same event title "Bim Bam Bom" exists in Haninge too but as a DIFFERENT event (different venue, different organizer, different date). Searching the dashboard by title alone would show the Vallentuna version and incorrectly mark the Haninge event as a duplicate.

**City Verification Steps:**
1. Search the Famies dashboard by event title
2. If no results → NOT a duplicate, proceed to publish
3. If results found → for each matching event, check:
   - **Venue city** (e.g., "Vallentuna bibliotek" vs "Haninge kulturhus")
   - **Organizer** (e.g., "Kultur Vallentuna" vs "Kultur Haninge")
   - **Source URL / CTA link** (vallentuna.se vs haninge.se)
4. If ALL matching events are from DIFFERENT cities → NOT a duplicate, publish the new event
5. If ANY matching event is from the SAME city → IS a duplicate, SKIP

**Examples:**

**Scenario A — Publish (different cities):**
- Currently processing: "Bim Bam Bom" from haninge.se (target city: Haninge)
- Dashboard search shows: "Bim Bam Bom" under Vallentuna bibliotek, organizer "Kultur Vallentuna"
- Decision: Different city → PUBLISH the Haninge version

**Scenario B — Skip (same city):**
- Currently processing: "Kreativt skrivande" from vallentuna.se (target city: Vallentuna)
- Dashboard search shows: "Kreativt skrivande" under Vallentuna bibliotek
- Decision: Same city → SKIP as duplicate

**Scenario C — Publish (no match):**
- Currently processing: "Sommarfest" from botkyrka.se
- Dashboard search shows no results
- Decision: Not a duplicate → PUBLISH

**Why:** Famies covers 27+ Swedish cities. Many Swedish events share names (e.g., "Sommarfest", "Familjedag", "Bokcirkel") across different municipalities but are genuinely separate local events. Skipping them as duplicates would leave users in other cities without local events. City context is as important as title when determining duplicates.

**Implementation Note:** Always track the "current city context" when batch-processing events from a source URL. The city/municipality of the source URL determines the city context for ALL events scraped from that source. Use this city context to compare against the venue/organizer/source URL of matching events on the dashboard.


---

## Rule #9: Image Prompt Writing Style (Authentic Nordic UGC-Style)

**Context:** All images must look like authentic real Swedish/Nordic family moments — NOT cartoonish, illustrated, or studio-staged. Images should feel like a candid phone snapshot from a real Swedish home or public space.

### The Required Prompt Formula (5-part structure)

```
Authentic vertical 1:1 photo of Nordic [subject] + [activity + setting] + [realism details] + [natural light] + [mood]. Real life, not staged.
```

### 5 Ingredients Explained

1. **Subject** — Nordic/Scandinavian children, parents, families (specify ages, hair, skin naturally)
2. **Activity + Setting** — concrete action in a real Swedish/Nordic environment (home kitchen, förskola, park, biblioteket, lekplats, skog)
3. **Realism details** — slight motion blur, imperfect framing, everyday clothes, real textures, visible toys/books/snacks
4. **Natural light** — soft window light, overcast Nordic daylight, lamp glow, golden hour through trees
5. **Mood** — warm, calm, joyful, cozy, curious, focused — never posed or plastic

### Strict DON'Ts

- ❌ NO cartoon, illustration, anime, 3D render, CGI, Pixar, digital art
- ❌ NO studio lighting, white backdrops, professional photoshoot look
- ❌ NO overly perfect/staged compositions — must feel candid
- ❌ NO HD/4K/8K/hyperrealistic tags — these push toward plastic look
- ❌ NO models, stock photo aesthetic, or commercial vibes
- ✅ ALWAYS end the prompt with "Real life, not staged."
- ✅ ALWAYS use 1:1 aspect ratio (500x500 output) — Famies event cards are square
- ✅ ALWAYS specify Nordic/Swedish/Scandinavian subjects

### Client-Approved Sample Prompts (1:1)

**1. Barnkalas (Children's party)**
Authentic vertical 1:1 photo of Nordic children around age 5–7 at a cozy Swedish birthday party at home. Kids laughing, blowing out candles on a simple homemade cake. Balloons tied to chairs, paper plates, juice glasses, one child in a paper crown. Warm window light, slight motion blur from movement, imperfect framing. Joyful, real, candid. Real life, not staged.

**2. Helgplaner (Weekend plans)**
Authentic vertical 1:1 photo of a Nordic family of four packing a weekend bag in a bright Swedish hallway. Parents helping two kids zip jackets, one child holding a stuffed animal, rain boots by the door. Overcast Nordic daylight through the window, soft shadows. Calm, everyday energy. Real life, not staged.

**3. Efter skolan (After school)**
Authentic vertical 1:1 photo of a Nordic child age 8 at the kitchen table eating a mellanmål — yogurt with berries and a knäckebröd sandwich. Backpack on the floor, jacket on the chair. Soft afternoon light from a window, slightly messy kitchen counter in background. Quiet, tired-happy mood. Real life, not staged.

**4. Enkel middag (Simple dinner)**
Authentic vertical 1:1 photo of a Nordic family around a small wooden dining table eating pannkakor with jam. Two kids age 4 and 7, parents serving, milk glasses, a simple IKEA-style kitchen in background. Warm evening lamp light. Cozy, real, unposed. Real life, not staged.

**5. Gratis aktiviteter (Free activities)**
Authentic vertical 1:1 photo of Nordic kids age 5–9 playing at a public Swedish lekplats on an overcast day. Kids climbing the wooden play structure, one on a swing, parents chatting on a bench in the background. Jackets, rubber boots, slightly muddy ground. Natural gray daylight. Real, candid. Real life, not staged.

**6. Regniga dagar (Rainy days)**
Authentic vertical 1:1 photo of a Nordic child age 6 sitting by a rainy window inside a cozy Swedish apartment, drawing with crayons on paper. Raindrops on the glass, soft lamp light, a blanket on the sofa nearby. Calm, focused mood. Slight reflection in the window. Real life, not staged.

**7. Lekplatser (Playgrounds)**
Authentic vertical 1:1 photo of Nordic children age 3–7 on a Swedish neighborhood playground in spring. Kids in overalls, one on a slide, one digging in sand, a parent kneeling to help. Birch trees in background, soft morning light. Candid, joyful, real. Real life, not staged.

**8. Utflykter nära (Nearby outings)**
Authentic vertical 1:1 photo of a Nordic family walking on a forest path in the Swedish countryside. Two kids age 4 and 8 ahead of parents, one holding a stick, autumn leaves on the ground. Soft dappled sunlight through birch and pine trees. Peaceful, adventurous mood. Real life, not staged.

**9. Lov (School holidays)**
Authentic vertical 1:1 photo of Nordic siblings age 5 and 9 in pajamas on a Swedish living room floor, building a pillow fort with blankets from the sofa. Morning light through the window, toys scattered, parent reading in background. Relaxed, playful. Real life, not staged.

**10. Aktiviteter (Activities)**
Authentic vertical 1:1 photo of a Nordic child age 7 at a Swedish kommun-run pottery workshop, hands muddy with clay, focused on shaping a bowl. Other kids working in soft background blur, wooden tables, warm overhead light. Curious, immersive mood. Real life, not staged.

**11. Orkar inte planera (Can't be bothered to plan)**
Authentic vertical 1:1 photo of a Nordic parent age 35 on a Swedish living room sofa with a tired smile, two young kids age 3 and 6 climbing on them with a picture book. Messy blankets, a cup of kaffe on the side table. Soft evening light. Warm, imperfect, real. Real life, not staged.

**12. Vardagsvinster (Everyday wins)**
Authentic vertical 1:1 photo of a Nordic child age 4 proudly holding up a drawing to a parent in a Swedish kitchen. Parent kneeling, smiling, fridge covered in other drawings and magnets in background. Afternoon light. Tender, authentic moment. Real life, not staged.

### Adaptation Examples (applying the formula to Famies events)

**Event: Sagostund på biblioteket**
`Authentic vertical 1:1 photo of Nordic children age 3–5 sitting cross-legged on a colorful rug at a Swedish public library storytime. A librarian reading a picture book, kids watching intently, one with thumb in mouth. Soft indoor library light, bookshelves in background. Calm, curious mood. Real life, not staged.`

**Event: Pianokurs för nybörjare**
`Authentic vertical 1:1 photo of a Nordic child age 8 at an upright piano in a Swedish music school room, concentrated, small hands on the keys. Sheet music on the stand, wooden floor, natural daylight from a window. Focused, gentle mood. Real life, not staged.`

### Why This Rule Matters

Famies is a brand built on **real Swedish family life**. Users scroll the app to find events for their real kids — the images must feel like something a Swedish parent would actually photograph, not a stock illustration or a commercial shoot. Authentic UGC-style Nordic images drive trust, engagement, and conversion. Any cartoon/illustrated/staged image breaks the brand feel and must be regenerated.
