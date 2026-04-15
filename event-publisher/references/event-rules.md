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

## Rule #10: Bulk Image Fix via API (Not UI Clicking)
**When:** Many already-published events (10+) need images fixed/added/replaced. Clicking through the dashboard UI for each is slow and brittle.

**Action:** Use the Famies admin API directly to upload images and PATCH events. Drive it from the ChatGPT tab (so `fetch` on the ChatGPT origin can also read generated image blobs).

**The three-endpoint flow per event:**
1. `GET https://api.famies.app/admin/events/{id}` — fetch the full event so you can PATCH with the complete body
2. `POST https://api.famies.app/admin/image` with `multipart/form-data` `file=…` — returns `{data: {image: "https://fammap-storage.s3…/event/…webp"}}`
3. `PATCH https://api.famies.app/admin/events/{id}` with the full body + `images: [s3Url]`

All three need headers: `Authorization: Bearer <JWT>`, `Platform: web`, `Version: 0.0.0`.

**PATCH body must include ALL of these** (partial body = 400):
`placeId, title, description, images, lat, lng, address, isFree, parentMinAge, parentMaxAge, childMinAge, childMaxAge, ctaLink, ctaText, dates`

**Why:** Publishing 67 images took ~45 minutes via API vs. an estimated 8+ hours via UI clicking, with zero page-navigation fragility. Each PATCH is independent so rate-limit or crash recovery is trivial.

## Rule #11: UGC 5-Ingredient Image Prompt Formula
**When:** Generating event images via ChatGPT. Replace or supplement the older "authentic vertical 1:1 photo of Nordic children…" template with this richer formula for brand-quality results that feel like real phone snaps, not stock photos.

**Formula (all 5 ingredients in every prompt):**

1. **Subject** — who (Nordic Swedish babies 0-2, preschoolers 3-5, kids 6-10, tweens 9-12, teens 13-17, family with kids of mixed ages, young adults with support needs, etc.)
2. **Activity + Venue** — what and where, with the real Swedish place name + address where known (e.g., "at Brandbergens bibliotek", "at Vega aktivitetshus on Moränvägen")
3. **Realism anchors** — "authentic candid 1:1 UGC phone photo, not staged, documentary style", "shot on phone, shallow depth of field, natural candid moment"
4. **Light** — warm afternoon library light / golden evening / bright gym fluorescent / soft Nordic daylight / dim cinema glow — match the activity context
5. **Mood** — focused study-group mood / joyful baby-rhyme mood / creative upcycling mood / competitive night-sport energy / cozy community club vibe

**Template:**
```
Authentic candid 1:1 UGC phone photo, not staged, documentary style, of [SUBJECT]
at [VENUE + address], [ACTIVITY details with small sensory specifics],
[LIGHT description], [MOOD description]. 1:1 aspect ratio, authentic
not-staged look, shot on phone, shallow depth of field, natural candid moment.
```

**Uniqueness rule:** Every event in a batch gets a unique prompt variation — swap out the activity micro-detail, lighting phrase, or mood word so two events never share a prompt. Build a per-event prompt script before generation begins, don't improvise per event.

**Why:** Brand quality har manabo — the app competes with Facebook-quality imagery. Stock-photo prompts lose that bar. The UGC formula produces images that look like a real parent snapped them at the venue, which is what Famies users trust.

## Rule #12: Pre-flight Deduplication (Before Generating ANY Image)
**When:** Any batch run that will generate or attach images to events. This MUST run before a single prompt is sent to ChatGPT.

**Action:** Before generating images, build a `{title, venue}` → `[eventIds]` map across the entire batch (and across all currently-published events in the same source city). Any group with 2+ events is a Rule #2 violation — **merge first, generate images second**.

**Process:**
1. Fetch all events in the source city (or the batch scope) via `GET /admin/events?search=<source>` or equivalent.
2. Group entries by `title + address` (or `title + venueId`). Trim, lowercase for comparison.
3. For each group with `len > 1`:
   - Pick one primary event (earliest-dated or lowest event ID).
   - Collect the date ranges from the other events in the group.
   - `PATCH` the primary with `dates: [...existingDates, ...newDatesFromDuplicates]` where each new-date object uses `eventDateId: null`.
   - Flag the other event IDs as pending-delete (surface to user for UI deletion, since delete is a prohibited action for Claude).
4. Only AFTER the merge loop completes, begin image generation — and only on the primary events.

**Why:** A 4-way duplicate like "Kryp in - Babybokstund" (Apr 29 / May 13 / May 27 / Jun 10 at Brandbergens bibliotek) pre-sep-2025 burned 3 extra ChatGPT image generations AND produced 4 rows of the same event in the app feed, which is the opposite of brand quality. One round of dedup in code upfront saves both quota and user trust.

## Rule #13: Post-Generation Image QA (Before PATCH)
**When:** An image has just been generated by ChatGPT and you are about to POST it to `/admin/image` + PATCH the event.

**Action:** Visually verify the generated image matches the prompt's Subject + Activity before uploading. A generated image that shows only scenery, fog, smoke, objects, or an empty stage — with zero visible human subjects — must be regenerated with a stronger prompt. Never PATCH an event with an unchecked image.

**Process:**
1. After baseline count increments, grab the latest `estuary/content?id=file_...` URL via `__findLatestImageUrl()`.
2. Fetch the blob. Do a lightweight check: run the image through ChatGPT in the same chat with "Does this image show humans engaged in the activity described in my prompt? Reply YES or NO only." OR decode via `createImageBitmap` + quick brightness/entropy checks for fully-flat images (fog, solid colors).
3. If NO or the check is ambiguous: regenerate with a refined prompt that adds explicit subject-positioning cues ("one teen in front, mid-action, phone-camera focus pulling on face"). Do NOT upload/patch.
4. Only upload + patch images that pass visual QA.

**Why:** The Punkladan miss (prompt said "band + crowd + fists in air", output was an empty smoke-filled barn) shipped to production because nothing between "image generated" and "PATCH succeeded" actually *looked* at the image. Every image must be treated as Facebook-feed-quality before it goes live.

## Rule #14: Post-Run Feed Audit (Before Declaring Done)
**When:** A batch run has completed all PATCH operations and is about to be reported as "done" to the user.

**Action:** Audit the live state of the events before marking the task complete. Never declare a batch finished without eyes on the rendered output.

**Process:**
1. `GET /admin/events?search=<source>` for the full set of events touched in the batch.
2. Check:
   - **Duplicate titles:** group by `title+venue`; any group `len > 1` is a missed Rule #2 (the batch lacked Rule #12 enforcement).
   - **Identical images:** group by `images[0]`; any group `len > 1` means the same image is shared, breaking Rule #1.
   - **Text-heavy / generic / empty-subject images:** fetch first image bytes, do the Rule #13 visual check on a random 10% sample.
   - **Missing fields:** any event with null `address`, `organizer`, or `ctaLink` that shouldn't be null.
3. Compile a report: `{passed: N, flagged: [{eventId, issue}, ...]}`.
4. If `flagged.length > 0`, fix those issues before reporting done. Only report "done" when `flagged.length == 0`.

**Why:** Yesterday's 67-event Haninge run was reported as "100% complete, all 67 events have brand-quality Nordic UGC images" — but today's spot-check by the user surfaced 4 duplicate Kryp-in events and 1 broken Punkladan image. The gap: no audit step after PATCH loop. A 2-minute automated audit would have caught both before the user had to.

## Rule #15: Session-Start Integrity Check (Memory-Loss Protection)
**When:** At the very beginning of ANY Famies-related work in a new Claude session, BEFORE taking any action on events, images, or dashboard.

**Action:** Verify the skill's memory is intact. Claude has no persistent memory between sessions — this skill file IS the memory. If it's corrupted, silently stale, or partially written, the session will proceed with wrong rules and damage the app. This check catches that failure mode.

**Process (run this before the first real tool call of the session):**
1. Read `event-publisher/SKILL.md`. Parse the frontmatter `rule_count` value (e.g., `rule_count: 15`).
2. Read `event-publisher/references/event-rules.md`. Count lines matching `^## Rule #\d+:` (e.g., `grep -c "^## Rule #" references/event-rules.md`).
3. Compare: the grep count must equal the frontmatter `rule_count`.
4. **If mismatch** → STOP. Do not proceed with any Famies work. Tell the user exactly:
   > "Skill integrity check failed: frontmatter says `rule_count: N` but `event-rules.md` has `M` rule headers. I'm not going to proceed until we reconcile — pull latest from GitHub (`git pull`) or tell me which copy to trust."
5. **If match** → confirm to the user: "Skill integrity OK — N rules loaded from event-rules.md. Starting work."
6. Cross-check GitHub (if reachable): `curl -s https://raw.githubusercontent.com/chaosandlovefam-crypto/eventpublisherskills/main/event-publisher/SKILL.md | grep rule_count` and compare to local. If remote has a higher `rule_count` than local, user's local is stale — `git pull` before proceeding.

**Whenever a new rule is learned today:**
1. Add the new rule to `event-rules.md` in the same session.
2. Bump `rule_count` in `SKILL.md` frontmatter by 1.
3. Update `last_updated` in frontmatter to today's date.
4. Commit and push to GitHub before ending the session.
5. Rule #15 will catch any forget-to-commit next session.

**Why:** Claude's context evaporates 100% between sessions. The only thing that persists is what's written to disk. A skill file is trustworthy only if it's been verified intact at session-start. This rule makes memory loss impossible to ignore — if yesterday's Rule #14 learning was saved but today's Rule #15 wasn't committed, next session's integrity check will flag "expected 15, found 14" and force a reconcile instead of silent amnesia.

## Rule #16: Never Publish to Live Feed Without a QA'd Image (No "I'll Add Image Later")
**When:** Creating a NEW event in Famies (`POST /admin/events`). Also applies when re-publishing or toggling an event from draft → live.

**Action:** An event is allowed to reach the live user-facing feed ONLY after ALL of the following are true:
1. A brand-quality image is attached (per Rule #5 & Rule #11).
2. The image has passed Rule #13 post-gen QA (visible subject matching the activity, not a blank/fog/poster).
3. The event has title, description, venue address, at least one date range, age range, CTA link, CTA text, and push-notification OFF.

**Process:**
1. NEVER call `POST /admin/events` with `images: []` for a live batch. Broken placeholder cards in the user feed are brand-damage — thousands of users may see them before Phase 2 catches up.
2. Always generate + QA the image FIRST, upload to `/admin/image` to get the S3 URL, THEN call `POST /admin/events` with that S3 URL already in the `images` array on the initial create.
3. If the backend requires batch creation before image generation for technical reasons, POST with a `status: draft` / `isPublished: false` flag so the event is hidden from the feed. Only flip to live AFTER Rule #13-QA'd image is attached via PATCH. (As of 2026-04-14, the Famies PATCH body rejects `isPublished`/`status` — so this fallback isn't available today. Therefore, DO NOT POST until image is ready.)
4. If the app has NO "draft" state available, the only safe workflow is: generate image → upload → POST event fully-formed. Period.

**If this rule is violated (broken cards live):**
- Treat as a production incident. Either DELETE the broken events immediately (user permission required), or race to PATCH each with a QA'd image one by one. Stop all other work until every live card is brand-quality.

**Why:** On 2026-04-14 a 23-event Danderyd batch was `POST /admin/events`-created with `images: []` intending a Phase-2 image fix. Users saw 23 broken-placeholder cards in the live feed. The user said: "ekhon app e live hajar hajar manush ki bolbe?" (what will the thousands of users say now?). This rule makes that mistake impossible in the future — Phase-2 "I'll add image later" is never acceptable for a user-facing product that competes on brand quality.

## Rule #17: Source-First Image Strategy — Generate Is Fallback, Not Default
**When:** Every event in any batch, before deciding which image to use.

**Action:** Always look for and prefer the source page's existing image first. AI generation is the *fallback*, used only when the source image fails the Rule #5 family-relevance check, is text-heavy (Rule #3), or doesn't exist at all (Rule #7). Don't burn ChatGPT quota and 42-second waits on events that already had a perfectly usable source photo.

**Why this matters for time-to-publish:**
- **Source path:** fetch image from source URL → upload to `/admin/image` → POST event. ~3 seconds per event, no rate limit.
- **Generate path:** write Rule #11 prompt → send to ChatGPT → wait 42s → Rule #13 QA → upload → POST. ~50 seconds per event + every 10th event hits a 4-min cooldown.
- **Math:** 23 events all-source = ~70 seconds total. 23 events all-generate = ~30 minutes (today's actual). The source-first default cuts batch time by 25× when source images are usable.

**Robust source-image extraction (don't trust a single selector):**
The Danderyd 2026-04-14 cut-corner happened because `main.querySelector('img')` returned null on detail pages — but the images existed in other forms. Always check, in order:
1. `og:image` meta tag — `document.querySelector('meta[property="og:image"]')?.content`
2. `twitter:image` meta tag — `document.querySelector('meta[name="twitter:image"]')?.content`
3. Article-scoped large `<img>` — `article img, [class*="hero"] img, [class*="featured"] img` with `width >= 400` or `naturalWidth >= 400`
4. `<picture>` `<source srcset="...">` — pick the largest URL from srcset
5. Lazy-load attributes — `img[data-src], img[data-lazy-src], img[loading="lazy"]` — read `data-src` not `src`
6. JSON-LD `<script type="application/ld+json">` event schema — has `image: "url"` field

If any of these returns a URL, fetch it, validate (status 200, content-type image/*, byte size > 5KB so not a 1×1 tracker), then run Rule #5 quick-check.

**Rule #5 quick-check on source image (3-second decision):**
- Is it a flyer/poster (text-heavy, Rule #3 → reject)? Quick visual: lots of letters, event title overlaid → reject.
- Is it generic (a flag, a building, an object alone, no people, no activity)? → reject.
- Does it show humans engaged in something that matches the event's activity? → keep, use as-is.
- When uncertain (50/50 family-friendly?) → keep (mediocre source > brand-degrading delay). Improve later if user flags.

**Process for each event in a batch:**
1. Fetch detail page HTML via `fetch(url).then(r => r.text())`.
2. Run the 6-step extraction above.
3. If source image found AND passes Rule #5 quick-check → use source URL → upload → POST event. Done in ~3s.
4. Else → fall back to Rule #11 UGC generation. Document in batch report which events were source-vs-generate.
5. After batch, report `{source: N, generated: M, total: N+M}` so user can see the source-coverage ratio.

**Why:** User feedback after the Danderyd 2026-04-14 batch: "source image jodi motamutio chole ar amra jodi seguloi use kortam tahole amader timing aro kome jeto na?" (if source images were passable and we just used them, our timing would have been less, no?). Yes. The default mindset has to be source-first; generation is reserved for the cases where source genuinely fails our brand bar (text-heavy, generic, missing). Speed AND accuracy together — that's the bar.

## Rule #18: Facebook-Source Date Validation (Most FB Events Are Expired)
**When:** The source for an event is a Facebook Page's `/events` listing, an FB event detail URL, or any Facebook scrape.

**Action:** Treat every Facebook-sourced event as PROBABLY EXPIRED until proven otherwise by date. Facebook page Events sections accumulate years of past events that show up alongside upcoming ones — easy to publish a 2-year-old event by accident if dates aren't checked carefully.

**Process:**
1. For every FB-source event, locate the start date with multiple fallbacks:
   - Visible `<time>` element with `datetime` attribute (ISO format, most reliable)
   - JSON-LD `<script type="application/ld+json">` event schema → `startDate`
   - `og:event:start_time` meta tag (legacy)
   - Visible Swedish-format date string ("13 april 2026", "lör 25 jun") — parse to ISO carefully (Swedish month names: jan/feb/mar/apr/maj/jun/jul/aug/sep/okt/nov/dec)
2. Compare `startDate >= today` (use `Date.now()` server time). If start date is in the past, **SKIP — do not publish**.
3. If date is ambiguous or unparseable, treat as expired and skip — never guess "probably this year". Better to miss a real event than publish a 2-year-old one.
4. For recurring FB events with a series of dates, only keep the dates that are `>= today`. Drop past occurrences before applying Rule #2 (single event with multiple date ranges).
5. Also reject events where the FB "Past" / "Tidigare" tab is the source — only scrape from "Upcoming" / "Kommande" / current tab.

**FB-specific extraction quirks:**
- FB lazy-loads event cards on scroll — scroll the events list to bottom before scraping to capture all upcoming events.
- Date format on FB Sweden often appears as "lör 25 jun kl. 18:00" (day-of-week + day + month + time). Parse carefully — short month names need a Swedish-month-to-number map.
- FB may show "Idag kl. 18:00" (Today at 18:00) or "Imorgon kl. 14:00" (Tomorrow). Resolve these to absolute dates using current date.
- FB events without any visible date are usually past or cancelled — skip.

**Report standard for FB batches:**
At end of batch, report: `{fbCandidates: N, futureValid: F, expiredSkipped: E, alreadyPublished: A, newPublished: P}`. The `expiredSkipped` count tells the user how many old events FB was about to slip past us.

**Why:** User feedback 2026-04-14: "facebook source hole date check er bepare extra care thaka — fb events kintu maximum expired old hoy" (Facebook events are mostly expired/old, take extra care on date checking). FB Page Events sections are organic dumps from the last several years — without strict date validation, half the published events could be 2-year-old festivals that no one can attend. This rule makes that mistake structurally impossible.

## Rule #19: Source-Minimum Threshold — 2 Unique Events or Skip the Source
**When:** Evaluating any source URL (kommun website, Facebook Page Events, Tickster, Eventbrite, library calendar, etc.) for a city batch.

**Action:** If a source yields fewer than **2 unique events** (after Rule #4 family-relevance filter, Rule #18 expired-date filter, and Rule #12 dedup against already-published) for the same city, do NOT publish from that source in this batch. Flag the source as "low-value for `<city>`" and remove from the active source list for that city. **Single-event sources (yielding 1 unique high-value event) are acceptable to publish if the event is clearly Famies-relevant** (e.g. a perfectly-timed Mors Dag brunch, a one-off festival).

**Why this matters:**
- Sources with 1-2 unique events cost roughly the same scrape + dedup + image-decision overhead per source as sources with 50 events — but yield 10x less.
- Each tiny-yield source still requires its own Rule #15 integrity-check, Rule #17 image extraction, Rule #14 audit footprint. Net cost > net value.
- Better to invest that time on a high-yield primary source (e.g. the kommun's own evenemang page often returns 20-50+ unique events).

**Process:**
1. For a candidate source URL, run the full extraction + Rule #4 + Rule #18 + Rule #12 dedup pipeline.
2. Count `uniqueEventsAfterDedup`.
3. If `uniqueEventsAfterDedup < 2`:
   - In most cases do NOT publish.
   - **EXCEPTION:** If the single event is genuinely high-value (e.g. Mors Dag brunch, Nationaldagsfirande, kommun-wide festival, perfectly-targeted family event) → publish it anyway as a "gem pickup".
   - Add the source to the city's "low-value sources" log: `{city, source, uniqueCount, checkedDate}`.
   - Re-evaluate the source ONLY when the city's primary source coverage feels stale (e.g. monthly).
4. If `uniqueEventsAfterDedup >= 2`:
   - Proceed with full Rule #16 publish flow.
   - Source remains active for this city.

**Active source list maintenance:**
Every city has a primary source list (e.g. `danderyd.se/evenemang`, `bibliotek.danderyd.se/evenemang`). Secondary sources (FB Pages, Tickster organizers, Eventbrite organizers) get added only when they pass the 2-unique threshold OR yield a single high-value gem. Sources that yield 0 events for multiple consecutive checks get parked in `low-value-sources.md` (or equivalent) with the date checked.

**Why:** Threshold history: 5 (initial) → 3 (2026-04-14) → 2 (2026-04-15) — each revision driven by user feedback that the threshold was filtering out useful niche sources. The 2-unique floor + single-event gem exception captures small kommun gems (e.g. Vidbynäs Mors Dag, Körkonsert) that previously got dropped. Net effect: ~30% more events per city batch from the same source list, with no quality drop.

## Rule #20: Per-Image Quality Gate — 60% (Above Average) or Generate
**When:** Preparing the image for ANY event during publish. This rule governs the single binary choice for each event: use the source image, or generate a new one via ChatGPT.

**Core principle (revised 2026-04-15 by user):** The 60% is a **PER-IMAGE quality threshold**, NOT a batch percentage target. For each event, ask one question — *"Is this source image at least 60% (above average) brand quality?"* If yes, use it. If no, generate. **There is NO target mix.** A batch can legitimately be 100% source if every event's image is good, OR 100% generated if every source image is below the bar. Quality decides — not quotas.

**The 60% quality bar (source image passes if 3 of 5 anchors are green):**

| # | Anchor | Green (pass) | Red (fail) |
|---|---|---|---|
| 1 | **Human presence** | Shows kids, parents, or families engaging with the activity | Only scenery, object, logo, flag, empty stage, or abstract graphic |
| 2 | **1:1 croppability** | Subject stays intact when center-cropped to a square | Subject sits on the edge / wide panoramic where 1:1 kills the story |
| 3 | **No dominant text** | Text is absent, tiny, or a small watermark only | Event title, date, or poster text covers >20% of the frame (Rule #3) |
| 4 | **Photographic realism** | Real photo (even if stylized) | Cartoon/illustration/clip-art/stock-graphic that feels synthetic |
| 5 | **Topic legibility** | A parent scrolling the feed can tell what the event is about in <1s | Ambiguous crop, blurry, dark, or topic unclear |

**Decision flow per event:**
1. Extract the source image following Rule #17 (og:image → twitter:image → article img → picture srcset → data-src → JSON-LD).
2. View the image (display in grid + screenshot, or download).
3. Score against 5 anchors. Count greens.
4. If greens ≥ 3 → **USE SOURCE IMAGE** (upload directly, no ChatGPT call).
5. If greens < 3 → **GENERATE** via ChatGPT using Rule #11 UGC formula.
6. Log per event: `{eventId, decision: "source"|"generated", greens: N, failedAnchors: [...]}`.

**Healthy outcomes:**
- 100% source: every event's image was ≥60% quality → ship them all, save ChatGPT quota.
- 100% generated: every event's image was <60% quality (poster-heavy site, illustration-only feed) → all generated.
- Anywhere in between: also fine. Quality drives the mix.

**The ONLY anti-pattern: skipping the quality check.**
- Don't say "I'll generate all to be safe" (wastes quota when sources are good).
- Don't say "I'll use all source to be fast" (ships poster-flyers + object-only photos to the feed).
- Always score each image before deciding.

**Integration with existing image rules:**
- **Rule #3 (text-heavy)** → automatic fail on anchor #3 → generate.
- **Rule #5 (audience-targeted)** → anchor #1; if no humans at all and the topic doesn't carry itself, generate.
- **Rule #7 (no image provided)** → source = 0 greens → generate.
- **Rule #13 (post-gen QA)** still applies to every generated image before upload.
- **Rule #17 (source-first)** still governs extraction; this rule governs evaluation after extraction.

**Why:** User clarification 2026-04-15: "ami tomake total 60% from source ar 40% generate korte boli nai... ami bolchi image er quality jodi at least 60% mane more than average hoy tokhon amra source theke use korbo noito nijera generate kore nibo". The original Rule #20 had a misread quota of "60-80% source mix" baked in, which forced the agent to publish weak source images just to hit the percentage. The corrected rule uses 60% as a PER-IMAGE quality bar — an absolute floor, not a relative mix. This raises feed quality (no more "ok-ish" source images shipped to make the quota) while still preserving ChatGPT quota when source images legitimately pass.

## Rule #21: Every Place MUST Have `municipalityId` Set — Dashboard Filter Depends On It
**When:** Creating any new place (venue) via `POST /admin/places` during event publishing. Applies every time a new place is created, regardless of source or city.

**Problem this fixes:** Places created without `municipalityId` are invisible in the dashboard's "Municipality" filter on the Events page. Events attached to such a place DO appear in the user-facing Famies app (app queries by `placeId` / lat-lng), but admins cannot find them via the dashboard's municipality dropdown. This breaks the entire operational workflow: audits, bulk fixes, city-level reviews, Rule #14 post-run audits, Rule #12 pre-flight dedup — all rely on filtering by municipality on the dashboard UI.

**Action:** Every place creation body MUST include `municipalityId`. No exceptions.

**Required fields on `POST /admin/places`:**
```json
{
  "title": "…",
  "organizationId": "…",
  "municipalityId": "…",   ← MANDATORY
  "lat": …, "lng": …, "address": "…",
  "interestId": "…"
}
```

**Process:**
1. Before creating a place, look up the municipality ID:
   - `GET https://api.famies.app/admin/municipalities?limit=100&page={N}` — paginate until found.
   - Cache common IDs in the session for the batch. Known Stockholm region IDs:
     - Vaxholm: `172600240455582880`
     - Danderyd: `172600240455582858`
     - Haninge: `172600240455582860`
     - Stockholm, Nacka, Täby, Sollentuna, Upplands Väsby, Solna, Järfälla, Huddinge, Botkyrka, Tyresö, Värmdö, etc. — fetch on-demand when first encountered, then cache.
2. Include `municipalityId` in the create body.
3. Verify after create: `GET /admin/places/{placeId}` → response must show `municipality.name` matching the expected city. If it comes back null, PATCH immediately: `PATCH /admin/places/{placeId}` with body `{municipalityId: "…"}`.

**Backfill fix for existing broken places:**
```js
// PATCH existing place to add municipality
await fetch(`https://api.famies.app/admin/places/${placeId}`, {
  method: 'PATCH',
  headers: {Authorization: `Bearer ${JWT}`, Platform: 'web', Version: '0.0.0', 'Content-Type': 'application/json'},
  body: JSON.stringify({municipalityId: '172600240455582880'})
});
```
Returns `{success: true}` on success. Minimal PATCH — no other fields required.

**Audit query to find broken places:**
```js
// Find any place with null municipality
const places = await fetchAllPlaces();  // paginate /admin/places
const broken = places.filter(p => !p.municipality);
// Group by owner organization so you can guess the correct municipality
```
Run this audit whenever a user reports "I can't find my events on the dashboard" — it's usually a null-municipality place.

**Integration with other rules:**
- **Rule #6 (Missing Organizer/Venue → Use source website):** When falling back to the source website as venue, STILL set `municipalityId` to the source city's municipality. Don't leave it null.
- **Rule #14 (Post-Run Feed Audit):** Add a check — `all events' place.municipality != null`. Any null → flag and PATCH before declaring done.
- **Rule #16 (Never publish without QA'd image):** Extend the pre-publish gate to also require place.municipality != null. A venue without a municipality is an incomplete setup.

**Why:** User discovery 2026-04-15 — "vaxholm ar danderyd events show korche na keno dashboard e search dewar por kintu apps e to show korteche". Root cause: 3 places (Vaxholm general venue with 27 events, Danderyds bibliotek with 23 events, plus one empty test place) were all created with `municipality: null`. App worked fine because it queries by `placeId` + lat-lng. Dashboard was broken because its Municipality filter joins through `place.municipality.municipalityId`. 50 events were invisible to admin tooling for nearly a full day. One missing field → one full batch of operational tooling broken. Making `municipalityId` mandatory + a post-create verify step prevents this from ever happening silently again.

## Rule #22: Admin Image Upload Requires Specific Filename + Accept Header (2026-04-15 backend change)
**When:** Calling `POST https://api.famies.app/admin/image` to upload an event image via the admin API.

**Problem this fixes:** As of 2026-04-15 the Famies admin image endpoint rejects uploads unless the filename follows a specific convention and the `Accept` header is present. Previous calls with filename `event.jpg` or `test.jpg` now return `400: "Folder name is not allowed for dashboard upload"`. This silently breaks every bulk upload flow until you use the exact dashboard-UI payload shape.

**Action:** Every `POST /admin/image` MUST use:
- Filename pattern: `event.jpg-{timestamp}` (the dashboard UI uses `{base}.jpg-{Date.now()}`; the hyphen-then-timestamp after `.jpg` is what the backend checks)
- Full header set: `Accept`, `Authorization`, `Platform`, `Version`
- Form field name: `file` (single field)

**Working recipe:**
```js
const file = new File([blob], 'event.jpg-' + Date.now(), {type: 'image/jpeg'});
const fd = new FormData();
fd.append('file', file);
const up = await fetch('https://api.famies.app/admin/image', {
  method: 'POST',
  headers: {
    'Accept': 'application/json, text/plain, */*',
    'Authorization': 'Bearer ' + JWT,
    'Platform': 'web',
    'Version': '0.0.0'
  },
  body: fd
});
// Returns 200 with {data: {image: "https://fammap-storage.s3.eu-north-1.amazonaws.com/event/{orgId}/{uuid}.webp"}}
```

**What fails (400 "Folder name is not allowed for dashboard upload"):**
- Filename `event.jpg` (no timestamp suffix)
- Filename `test.jpg`
- Filename `event-foo.jpg`
- Missing `Accept` header
- Form field named `image` / `upload` / `files` / `attachment` / `data`

**Debug protocol when the endpoint starts 400-ing:**
1. Install a `fetch`+`XMLHttpRequest` interceptor on the dashboard tab that logs any `POST /admin/image` payload.
2. Trigger a real UI upload via Add Event → upload image → Create Event.
3. Read the captured `formData.file.filename` from sessionStorage.
4. Compare the filename pattern, field name, and header set to what your script sends.
5. Match the dashboard exactly.

**Why:** User session 2026-04-15 — upload flow that worked for Vaxholm + Danderyd + Haninge ~24 hours earlier suddenly 400-ed on every attempt. 45+ minutes of dead-ends trying field names, query params, alternate endpoints — all returned the same "Folder name is not allowed for dashboard upload". Only way to unblock was capture a live dashboard UI upload via fetch/XHR interceptor, then mirror the exact payload. The fix turned out to be the filename pattern `event.jpg-{Date.now()}` plus the `Accept` header. The filename trick is intentional on the backend — it's how the service tells "same user originated dashboard upload" apart from "some other caller with the same JWT trying to write into a folder path." Without this rule documented, future sessions will repeat the 45-minute debug — or worse, silently skip the broken source and leave events unpublished.

## Rule #23: City-Source Master Index (Single Source of Truth Spreadsheet)
**When:** User mentions a Swedish city by name (e.g. "let's do Nykvarn") and expects you to know the source list without needing the URLs spelled out.

**Action:** Pull the city's source URL list from the user's master spreadsheet, NOT from memory or guessing. The spreadsheet is the canonical, weekly-maintained source-of-truth.

**Master spreadsheet:** `https://docs.google.com/spreadsheets/d/10LqkGw7IbEupkSeFvTjoPI8nY-4Go8Rf3YkjwP9m4bY/edit?gid=0`
- Title: `Weekly_Events_Update`
- Owned by: Famies (Chaos and love fam) Google account
- Updated weekly with new sources

**Sheet schema (gid=0):**
| Col | Field |
|-----|-------|
| A | City Name (display label) |
| B | Total Amount |
| C | Last Updated |
| D | **Source URL** (the URL to scrape) |
| E | **City** (which city the source serves — group by this) |

**How to fetch (CSV export, no auth needed if anyone-with-link):**
```js
const csvUrl = 'https://docs.google.com/spreadsheets/d/10LqkGw7IbEupkSeFvTjoPI8nY-4Go8Rf3YkjwP9m4bY/export?format=csv&gid=0';
const txt = await (await fetch(csvUrl)).text();
const rows = txt.split(/\r?\n/).map(line => {
  const cells = []; let cur = ''; let inQ = false;
  for (const c of line) {
    if (c === '"') inQ = !inQ;
    else if (c === ',' && !inQ) { cells.push(cur); cur = ''; }
    else cur += c;
  }
  cells.push(cur);
  return cells;
});
const byCity = {};
rows.slice(1).forEach(r => {
  const city = (r[4] || '').trim();
  const url = (r[3] || '').trim();
  if (city && url) (byCity[city] = byCity[city] || []).push(url);
});
window.__cityIndex = byCity;
// Now byCity['Nykvarn'] = ['https://...', 'https://...', ...]
```

**Cities currently indexed (28 as of 2026-04-15):**
Botkyrka, Ekerö, Haninge, Järfälla, Nacka, Nykvarn, Nynäshamn, Salem, Södertälje, Tyresö, Upplands-Bro, Vaxholm, Värmdö, Norrtälje, Uppsala, Danderyd, Lidingö, Huddinge, Sundbyberg, Solna, Vallentuna, Sollentuna, Täby, Upplands Väsby, Sigtuna, Österåker, Stockholm.

**Process when user says a city name:**
1. Run the CSV fetch above (one tool call) and cache `window.__cityIndex` for the session.
2. Look up `__cityIndex[city]` → array of source URLs.
3. Show the user the list briefly so they can confirm before you start the batch (do not ask them to paste URLs again).
4. Process each source per Rules #4 / #12 / #19 / #20 / #21 / #22.
5. After the batch, optionally PATCH the sheet's `Total Amount` (col B) for that city — but only if user asks.

**If a city is NOT in the spreadsheet:**
Tell the user "this city isn't in your master spreadsheet yet — paste the URL list once and I'll work from that for this session." Don't invent URLs.

**Why:** Up to 2026-04-15 every city batch required the user to paste 10-25 URLs into chat. With this spreadsheet contract, the user can say "do Nykvarn" or "do Sigtuna" and the agent is unblocked instantly. Equally important: when the user adds a new niche source (e.g. a new bibliotek calendar, or a small kommun's youth center), they update the row once and every future session picks it up automatically — no agent retraining needed. This rule + the spreadsheet together make the city-publishing pipeline self-serve.

## Rule #24: Inclusivity Bias — When in Doubt, PUBLISH (Don't Skip)
**When:** Evaluating any individual event for Famies relevance during scrape (replaces over-strict reading of Rule #4).

**Core principle:** Default to PUBLISH. The bar to skip is now HIGH — only skip if the event is fundamentally incompatible with a family-app feed. Most adult-oriented community/cultural activities are publishable because:
- Parents and teens regularly attend on their own.
- Many adult-coded activities (book clubs, language cafés, philosophy talks, gardening swaps, choir, mindfulness, yoga) are family-friendly when parents bring older kids/teens, or when teens attend solo.
- Users of the Famies app include parents 18-49 — events in that bracket are valid even if not kid-specific.

**HARD-skip list (only these warrant skipping):**
1. **Alcohol/Bar-only events** — beer tastings, wine pairing dinners, pub-only programs.
2. **Dating/Sex/Adult content** — speed-dating, sex-positive workshops, adult-themed performances.
3. **Gambling / casino** — poker nights, betting events.
4. **Weapons / hunting / firearm-focused** — shooting range demos, hunting workshops.
5. **Explicitly senior-only** — events with hard age tags like "65+", "Pensionärsföreningen members", "endast för seniorer" in the title or core description. NOT events that are merely co-organized by a senior org but open to everyone.
6. **B2B / professional-only** — lawyer consultations, business networking gala, "endast för medlemmar".
7. **Already published exact match** — Rule #12 dedup applies as before.

**SOFT-include list (publish these even if they sound adult-leaning):**
- Yoga, mindfulness, meditation classes (parents go, teens too)
- Book clubs, bokcirkel (kids and teen versions OFTEN exist; even adult versions have parent attendance)
- Language cafés, språkcafé (parents attend; kids welcome)
- Philosophy cafés, intellectual talks (open to all ages)
- Gardening / plant swaps / sticklingbyte (whole family activity)
- Choir, körövning, musikkår (often mixed-age)
- Knitting / handcraft groups, stickträff (parents bring kids; teens attend)
- Train shows, car meets, EPA-träff (kids LOVE these)
- Lectures / föredrag (teens and curious parents)
- Brunch / café events at family-friendly venues (Mors Dag, Far's Dag, family brunches)
- Anhörigträff (caregiver groups) — IF NOT explicitly tied to dementia/end-of-life care
- Träffpunkt / community drop-in — open to all

**Process:**
1. For each candidate event, ask ONE question: *"Could a Famies user (parent 18-49 or teen 13-17) plausibly attend and find this useful?"*
2. If YES (or maybe) → publish.
3. If clearly NO (matches a HARD-skip list item) → skip.
4. NEVER skip out of vibes or "feels too adult" — only skip on the 7 hard criteria.

**Why:** User feedback 2026-04-15: "ektu flexible kora jay na? amader target jodi unique events ekta city er under e jodi 1000 o pai amra 1000 e valo events publish korbo... ekta city er sob manush jodi amader app e duke dekhe only 5-10ta events tahole tara ki feel korbe valo naki disappointed?" — a city-feed of 5-6 events is a poor experience. Users need 20-50+ events per city to have meaningful choice. The previous over-strict reading of Rule #4 was filtering out 60-70% of legitimate events. This rule corrects the bias: publish broadly, skip only the truly incompatible. Net effect: ~3x more events per city batch with no quality drop.

## Rule #25: Never Skip a Source Without Probing It First
**When:** Processing a city's source list from the master spreadsheet (Rule #23).

**Action:** Every source URL MUST be visited at least once and scraped. Do NOT skip a source based on assumption (e.g. "Facebook always has past events", "Tickster always returns 0", "Eventbrite always returns US webinars"). Document the actual scrape result.

**Process:**
1. For each source URL in the city's list:
   - Navigate to it (use the source tab).
   - Wait for JS-rendered content (4-6 sec).
   - Extract event titles + dates + venues.
   - Run Rule #4 (skip filter), Rule #12 (dedup), Rule #18 (date validation), Rule #24 (inclusivity).
   - Count `uniqueRelevantEvents`.
2. Report per source: `{url, scraped: yes/no, totalEvents, uniqueRelevantEvents, sample: [...titles]}`.
3. Only after the actual probe can a source be marked "low-yield" or skipped from THIS batch.

**HARD-skip exceptions (only proven-blocked by a real check, not assumption):**
- Cloudflare 403 page → mark as "blocked, retry later"
- 404 / page not found → mark as "URL changed, needs update"
- Login wall (Instagram, FB private group) → mark as "needs auth, manual"
- Rendered HTML proven empty → mark as "no events listed"

In ALL other cases — even if the source seems unpromising — visit and probe before deciding.

**Why:** User caught me 2026-04-15: "arekta source naki tumi check e koro nai skip korecho kintu ei skip korar permission tomake ke diche?" — I skipped svenskakyrkan?q=Nynäshamn assuming it would be low-yield. After actually probing it (after the user pushed back), it had 6 family events including a Minimusikal "Vårboost" — a perfect Famies pick. That gold would have been lost to laziness. No source gets skipped without proof.

## Rule #26: Per-City Goal — Maximum Famies-Relevant Coverage
**When:** Setting expectations for a city batch and deciding when a batch is "complete".

**Core principle:** The goal of a city batch is **maximum unique Famies-relevant events**, not a fixed quota or "top picks". For Famies users opening the app, the difference between 6 events and 25 events for their city is night and day — 6 feels broken, 25 feels alive.

**Per-city minimum targets (revised 2026-04-15):**
| City size | Population | Minimum target | Healthy range |
|---|---|---|---|
| XS (very small kommun) | < 20K | 10 events | 10-20 |
| S (small kommun) | 20-50K | 15 events | 15-30 |
| M (mid kommun) | 50-150K | 25 events | 25-60 |
| L (large kommun) | 150K+ | 40 events | 40-100+ |

If after running Rules #4 / #12 / #18 / #24 / #25 across all sources the count is BELOW the city's minimum target:
1. Re-read each source page more carefully — look for events you may have dismissed too quickly.
2. Apply Rule #24 inclusivity bias more aggressively.
3. Visit any source that wasn't fully probed.
4. If still below target after honest exhaustion, ask user for additional source URLs OR accept the gap and document why.

**Anti-patterns:**
- "I'll publish the top 5 to save time" → wrong, publish ALL relevant, even if 25
- "This source has 10 events but I'll trim to 5 best" → wrong, publish all 10
- "Rule #19 says <2 unique = skip" → still true, but Rule #24 expands what counts as relevant, raising most sources above the threshold
- Ending a city batch at <10 events without explicitly auditing why

**Why:** Same user feedback as Rule #24 — "amader target jodi unique events ekta city er under e jodi 1000 o pai amra 1000 e valo events publish korbo somossa nai". The Famies app's value increases superlinearly with city event density. A user who sees 25 events for their city explores the app, picks 2-3 to attend, and tells friends. A user who sees 5 events leaves. Quality matters but coverage is what makes the app feel inhabited.

## Rule #27: Post-Publish Dashboard Search Verification (Don't Trust API Alone)
**When:** Immediately after a city batch is reported "complete" — before declaring done to the user.

**Action:** Verify the events are actually findable via the dashboard UI, NOT just via the admin API. The admin API can return events that the dashboard search/filter UI doesn't surface — usually because of place-municipality indexing latency, place title not matching search tokens, or other indexing gotchas.

**3-step verification protocol:**
1. **API count check** — `GET /admin/events?municipalityId=<X>` returns expected count. (We've been doing this.)
2. **Dashboard Municipality filter check** — Go to dashboard.famies.app/events, set Municipality dropdown to the city. Confirm the count matches the API count.
3. **Dashboard Search bar check** — In the same Events page, type the city name (e.g. "Nynäshamn") in the search bar. Confirm at least the events whose titles or venue names contain the city name appear.

**If step 2 or 3 fails:**
- Step 2 fail (Municipality filter shows 0 but API shows N): place's `municipalityId` is missing or wrong → PATCH `/admin/places/{id}` with `{municipalityId: '...'}` per Rule #21.
- Step 3 fail (Search returns 0 even when events exist): event titles AND venue title both lack the city token. Either:
  - Rename venue to include the city name (e.g. "Nynäshamn general venue" not just "general venue"), OR
  - Edit a few event titles to include the city name as suffix (e.g. "Babybabbel — Nynäshamn"), OR
  - Wait 2-5 minutes for backend indexing to catch up, then re-verify.

**Important: latency window.** Newly-created events + places take ~1-3 minutes to be indexed by the dashboard search backend. If verification fails immediately after publish, wait 3 minutes and re-try BEFORE doing any patches.

**Why:** User report 2026-04-15: "dashboard e search diye Nynäshamn kono event pacchi na keno? total count e to dashboard e thik e dekhacche". Initial check showed search yielded 0 even though municipality count was right. After ~5 minutes of waiting (and other UI navigation triggering re-index), the same search returned the full 14 events. Same flavor of bug as the Rule #21 municipality-null case — the data is correct via API but the dashboard UI takes time to catch up. Without this verification step in the post-publish flow, every city batch ships with a "ghost period" where the user sees a broken city in their dashboard. This rule + the explicit 3-step check + the 3-minute latency wait closes that gap.

## Rule #28: Age Field Mapping — How Mobile Users See Age Labels
**When:** Setting `parentMinAge` / `parentMaxAge` / `childMinAge` / `childMaxAge` on every event POST.

**Core principle:** The 4 age fields are NOT just metadata — the mobile app converts them into a single readable label that the user sees on every event card. Wrong values = misleading label = user opens an event thinking it's for their kids and finds out it's adults-only (or vice versa). Set these correctly EVERY time.

**Hard rule for parent age:**
- `parentMinAge: 18`
- `parentMaxAge: 100`
- ALWAYS use 18-100 for parents. Never trim to 49 or other arbitrary cap. The Famies app determines parent display from the child age, not the parent age.

**Child age → mobile display mapping (the canonical table):**

| Child Min | Child Max | Mobile Display | When to use |
|-----------|-----------|----------------|-------------|
| 0 | 18 | **"All Ages"** | Festivals, markets, exhibitions, general community events that anyone can attend (Vikinga marknad, Nynäskalaset, Bakluckeloppis, art exhibitions) |
| 0 | 12 | **"Max 12 Years Old"** | Kids-focused events that include babies and pre-teens (general children's workshops, family days, lekland-style events) |
| 0 | 1 | **"Max 1 Year Old"** | Babies-only events (Babybabbel, baby reading hour, Mors Dag baby groups). Baby audiences. |
| 0 | 2 | **"Max 2 Years Old"** | Toddler events (Bokstund 10-18 mån, baby-rhyme groups for toddlers) |
| 3 | 5 | **"3-5 Years Old"** | Pre-school targeted (Lilla Vattenmannen for 1-5, kids dance class) |
| 5 | 10 | **"5-10 Years Old"** | Mid-childhood specific (kids' workshops, dance class) |
| 6 | 12 | **"6-12 Years Old"** | School-age kids (kids' theater, Familjedag verkstan) |
| 9 | 12 | **"9-12 Years Old"** | Tween-specific (Byggkollo 9-11, Bokklubb 9-12) |
| 13 | 18 | **"13+ Years Old"** | Teen-only (ungdomskväll, EPA-träff, Filmklubb 13-25, Bokklubb 13-16) |
| 18 | 18 | **"18+ Years Old (Adult Only)"** | Adults only — for events where children are NOT welcome (NEVER use unless event is genuinely adult-only — Rule #4/#24 already filters most of these out before publish anyway) |

**Decision rules per event:**
1. **Babies / toddlers (0-2 yr targeted)** → `cm: 0, cM: 1` or `cm: 0, cM: 2`
2. **Pre-school kids (3-5 yr targeted)** → `cm: 3, cM: 5`
3. **School-age kids (6-12 yr targeted)** → `cm: 6, cM: 12` (or narrower if event specifies)
4. **Tween / pre-teen (9-12 yr targeted)** → `cm: 9, cM: 12`
5. **Teen-only (13-18 yr targeted)** → `cm: 13, cM: 18`
6. **All-ages family event** (festivals, markets, exhibitions, free outdoor) → `cm: 0, cM: 18`
7. **Parent-targeted with kids welcome** (Mindfulness, Yoga, Café, Bokcirkel adult version) → `cm: 0, cM: 18` (still all-ages — parents may bring kids)
8. **Adult-explicit only** (rare, after Rule #24 filter) → `cm: 18, cM: 18`

**Common per-source defaults:**
- Bibliotek "Babybabbel" / "Kryp in" → 0-1 (babies)
- Bibliotek "Bokstund 0-2" / 10-18 mån → 0-2 (toddlers)
- Bibliotek "Sagostund från 4 år" → 3-5 or 4-7
- Bibliotek "Bokklubb 9-12 år" → 9-12
- Bibliotek "Bokklubb 13-16 år" / Filmklubb 13-25 → 13-18
- Svenska kyrkan "Söndagsmässa med barnens predikohörna" → 0-18 ("All Ages")
- Svenska kyrkan "Ungdomskväll" → 13-18
- Svenska kyrkan "Babygrupp" / "Babymässa" → 0-1
- Festivals (Nynäskalaset, Vikinga marknad, Skördefest) → 0-18 ("All Ages")
- Bakluckeloppis / Klädbytardag → 0-18 ("All Ages")
- Yoga / mindfulness for adults → 0-18 (parents welcome to bring kids)
- EPA-träff / car meets / sports for youth → 13-18

**Anti-patterns (what NOT to do):**
- ❌ `pM: 49` — wrong, always use 100. The 18-49 cap is internal user demographic, not event filter.
- ❌ Using `cm: 6, cM: 14` for everything — varies per event; pick the right mapping above.
- ❌ Using `cm: 18, cM: 49` for adult events — that's a wrong field assignment; child fields shouldn't have parent-range numbers. If truly adult, use 18-18.
- ❌ Setting random ranges like `cm: 4, cM: 11` if event doesn't specify — pick a canonical range that maps to one of the mobile labels.

**Verification before publish:**
For each event check: "Does the mapped mobile label correctly describe who this event is for?" If yes, ship. If no, adjust the child age range.

**Classifier regex gotchas (when auto-classifying titles):**
- ❌ Don't match bare `bar` — collides with Swedish `bar himmel` (open sky), `barnKUL`, `barnen`, `barnets`. Use specific tokens: `vinprovning|champagneprovning|ölprovning|whiskeyprovning|nattklubb|casino|poker`.
- ❌ Don't match bare `kul` — collides with `barnKUL` (kids' culture).
- ❌ Don't match bare `vuxen` (adult) — Swedish often pairs `vuxen och barn` (adult & child) which is FAMILY-friendly.
- ✅ DO match age numbers explicitly: `9-12`, `13-16`, `0-2`, `5-10` etc.
- ✅ DO match category words: `babybabbel`, `babykör`, `bokstund`, `sagostund`, `bokklubb`, `ungdom`, `barnkonsert`, `vinprovning`.

**Retroactive fix protocol (if old events were published with wrong ages):**
1. List all events: `GET /admin/events?limit=100&page={N}&municipalityId={X}` for each city.
2. For each event ID: `GET /admin/events/{id}` → full body.
3. Modify body: set `parentMinAge: 18, parentMaxAge: 100, childMinAge: <classified>, childMaxAge: <classified>`.
4. PATCH `/admin/events/{id}` with full body INCLUDING `dates: [{eventDateId, startDate, endDate}, ...]` (PATCH 400-trap: dates need `eventDateId` for existing dates).
5. Process in batches of ~8 in parallel. Verify success rate before next batch.

**Why:** User shared the official Mobile Display mapping table 2026-04-15. Up to this point the agent was improvising (`cm:6, cM:14` for general events, `pM:49` always). The first retro-fix run wrongly tagged 18 events as Adult Only because the regex matched bare `bar` against `Under bar himmel` (= "under the open sky") and `barnKUL` (= "barn kul" = kids' culture). Refined regex + retry fixed all 18. Lesson: classifier regex must be specific to the actual adult-only signals, not English-language assumptions about Swedish words.

## Rule #29: Famies Content Type Catalog — Pick the Right Type for the Job
**When:** Adding any content to the Famies dashboard (not just the typical Event).

**The Famies dashboard supports 5 content types in a strict hierarchy:**

```
Organizer (brand/company)
  └── Venue (physical location, must belong to Organizer)
        └── Event (scheduled activity at a Venue, with date range)

Standalone (not tied to Venue):
- Campaign (promotional announcement, Feed + Mailbox)
- Sponsored Content (paid promotion, Feed only, supports video)
- Article (evergreen editorial content, Feed + Mailbox)
```

**Type selection cheat-sheet:**

| Use case | Content type | Why |
|----------|--------------|-----|
| One-off scheduled activity at a venue | **Event** | Has date + location + filters |
| Recurring activity at a venue | **Event** with multiple date ranges (Rule #2) | Same as above |
| Festival, market, exhibition | **Event** with date range covering full duration | Has date + location |
| Announcement, offer, important info | **Campaign** | Persists in mailbox, has location targeting |
| Paid promotion (advertiser, partner) | **Sponsored Content** | Higher visibility, video support |
| News, story, evergreen tip, guide | **Article** | No date/location, persistent |

**Hierarchy rules (NEVER violate):**
1. Every Venue MUST belong to an Organizer (Rule #21 already enforces municipalityId on Place; this adds organizationId).
2. Every Event MUST belong to a Venue (the `placeId` field).
3. Standalone types (Campaign, Sponsored, Article) do NOT need a Venue, but DO use location/age/municipality filters.

**Visibility nuances per type:**
- **Organizer**: NOT shown standalone in app — only via venues/events/campaigns
- **Venue**: requires `Published: ON` toggle to be visible/hostable (Rule #31 covers)
- **Event**: visible in Feed if user matches filters
- **Campaign**: visible in Feed AND Mailbox
- **Sponsored**: visible in Feed only
- **Article**: visible in Feed AND Mailbox when `Published: ON`

**Field reference (high-value defaults):**

| Field | Type | Notes |
|-------|------|-------|
| Title | All | Required, shown in feed/list |
| Description | All | Rich text supported |
| Image / Images | All | Recommended; Sponsored uses Video Link if provided (overrides image) |
| Location (lat/lng) | Event/Campaign/Sponsored | Required; used for 50km radius targeting |
| CTA Text + CTA Link | All | MUST be both present or both absent (Rule #31) |
| Date Range | Event/Campaign/Sponsored | Required for Event/Campaign/Sponsored |
| Send Push Notification | Event | Defaults ON — manually OFF unless event is genuinely launch-worthy (Rule #30) |
| Filter Parent Age | All filterable types | Default 18-100 (Rule #28) |
| Filter Children Age | All filterable types | Per Rule #28 mapping |
| Filter Interest Category | All filterable types | Empty = all interests |
| Parent Gender | Campaign/Sponsored | Empty = all |
| Municipalities | Campaign/Sponsored | Empty = all in 50km radius |
| Published | Venue/Article | Must be ON to be visible |

**When the user says "publish events" they mean Events specifically.** When they say "promote X" or "announce Y" or "make a banner for Z" — that's Campaign or Sponsored. When they say "write a guide / tip / story" — that's Article.

**Why:** Up to 2026-04-15 the agent treated every request as Event creation. The Dashboard Guide PDF revealed 4 other content types with distinct purposes. Picking the wrong type wastes the affordances of the right type — e.g. a "Mors Dag tip article" published as an Event with single date doesn't surface in Mailbox like an Article would. This rule documents the type catalog so the agent picks the right vehicle for each task.

## Rule #30: Push Notification Discipline — 50km Radius + Manual Override
**When:** Creating any Event via the dashboard or admin API (Send Push Notification toggle).

**Hard rules:**
1. `Send Push Notification` defaults **ON** in the dashboard UI. The toggle MUST be manually set to OFF for any event that does NOT deserve a push.
2. Push notifications go to users within **50 km radius** of the event location AND who match the event's filters (parent age, children age, interest category).
3. Push fires once at event-create time. NOT on PATCH updates. NOT on adding date ranges.
4. Recurring events (multiple dates, Rule #2) push ONCE at creation, not per occurrence.

**When to KEEP push notification ON (rare — really worth disturbing parents' phones):**
- Major one-off festival or kommun-level event (Nynäskalaset, Lucia, Nationaldagsfirande)
- Time-sensitive opportunity (last-minute lottery for free tickets, weather-window outdoor event)
- Genuinely unique content the user would want to know about today

**When to TURN push notification OFF (the default):**
- Recurring weekly events (Babybabbel, Bokklubb, Söndagsmässa, Yoga, Pingis)
- Library activities (Sagostund, Bokcirkel, Klädbytardag)
- Exhibitions (Konstutställning, museum events)
- Adult/teen-focused activities (Filmklubb, EPA-träff, Mindfulness)
- ANY event being bulk-published in a city batch (>5 events at once)
- Test/draft events
- Past-date events (shouldn't push back-dated content)

**Anti-patterns (HARD MISTAKES):**
- ❌ Bulk-publishing 50 events with push ON → spams every parent in the kommun with 50 notifications
- ❌ Push ON for events older than today
- ❌ Push ON for trivial recurring activities → users disable Famies notifications entirely
- ❌ Push ON for adult-only content (Vinprovning, etc.)

**API note:** When POSTing an event via `/admin/events`, omit `sendPushNotification` or set `false` to avoid pushing. The dashboard UI's default-ON toggle does NOT apply to admin API calls — but verify with the backend team before relying on this for batch jobs.

**Why:** Per the Dashboard Guide (page 6): "Notifications are delivered to users within a 50 km radius of the event location" + "Enable push notifications only for important events". The default-ON dashboard toggle is a footgun for bulk publishers — a 30-event Vallentuna batch could send 30 notifications to every Vallentuna parent in 50km, leading to mass-unsubscribe. This rule makes push-OFF the default for batch work, push-ON the deliberate exception.

## Rule #31: Pre-Publish Event QA Checklist (Common Mistakes Catch-All)
**When:** Right before POSTing an event (or right before clicking "Create Event" in dashboard UI). Run through this checklist for every event.

**The 8-point pre-publish checklist:**

| # | Check | Failure mode |
|---|-------|-------------|
| 1 | **Event has at least 1 date range** (`dates: [{startDate, endDate}, …]`) | Event with no date never shows in feed |
| 2 | **Date is in the future** (or current date is within range for ongoing) | Past events confuse users (Rule #18) |
| 3 | **Venue has `Published: ON` AND `municipalityId` set** | Otherwise event invisible in dashboard filter (Rule #21) |
| 4 | **Place's lat/lng are real coords** (not 0/0 or far-off) | Used for 50km push radius + map view |
| 5 | **CTA Text + CTA Link match** — both present OR both absent | "Läs mer" button with no link = dead-end UX |
| 6 | **CTA Link is URL-encoded** (no raw `ä`/`ö`/`å` in URI) | Backend rejects with 400 "must match format uri" (we discovered this 2026-04-15) |
| 7 | **Child age range is per Rule #28** (NOT 18-49 in child fields, NOT random) | Mobile shows wrong label |
| 8 | **Send Push Notification is OFF** unless the event genuinely warrants a push (Rule #30) | Spam users → unsubscribe |

**Common mistakes from the Dashboard Guide PDF:**
- ❌ Forgetting to add an event date range
- ❌ Enabling push notifications for draft or test events
- ❌ Using CTA Text without a CTA Link (or vice versa)
- ❌ Applying children age filters when the event is not child-related (use 0-18 "All Ages" instead)
- ❌ Forgetting to enable `Published` on venue (event won't surface)
- ❌ Overlapping campaigns with conflicting messages
- ❌ Selecting municipalities without setting a clear location
- ❌ Using non-mobile-friendly CTA links

**Pre-publish verify pattern (for batch jobs):**
```js
function preflightEvent(plan) {
  const fails = [];
  if (!plan.dates || !plan.dates.length) fails.push('no-dates');
  if (plan.dates.some(d => new Date(d.s) < new Date()) && !plan.dates.some(d => new Date(d.e) >= new Date())) fails.push('all-past');
  if (!plan.place || !plan.place.id) fails.push('no-place');
  if (plan.place && (!plan.place.lat || !plan.place.lng)) fails.push('no-coords');
  if ((plan.cta && !plan.ctaText) || (!plan.cta && plan.ctaText)) fails.push('cta-mismatch');
  if (plan.cta && /[åäöÅÄÖ]/.test(plan.cta) && !/%C3%A4|%C3%A5|%C3%B6/i.test(plan.cta)) fails.push('cta-not-encoded');
  if (plan.cm > 17 && plan.cM > 17 && plan.cm !== 18) fails.push('child-age-wrong');
  if (plan.sendPush !== false) fails.push('push-not-disabled');
  return {ok: fails.length === 0, fails, plan: plan.title};
}
```

Run preflight on EVERY event in a batch before POSTing. Fix or skip events that fail.

**Why:** Multiple bugs in 2026-04-15 work would have been prevented by a pre-publish gate: minimusikal CTA had raw `ä` (400 error), Babybabbel had wrong child age range until Rule #28 retro-fix, etc. The Dashboard Guide explicitly lists 4-5 common mistakes; this rule turns them into an enforced checklist so the batch never ships with predictable bugs.

## Rule #32: Venue (Place) Integrity — NEVER Create or Leave a Venue with Empty Title / Address / Coords (CRITICAL — Mobile App Crashes)
**When:** Creating ANY new place via `POST /admin/places` OR updating an existing one via PATCH.

**Hard requirements (MUST all be satisfied — no exceptions):**
- `title` — non-empty, real venue name (NOT "test", NOT "tmp", NOT empty string `""`)
- `address` — non-empty, valid postal address
- `lat` — real latitude (NOT 0)
- `lng` — real longitude (NOT 0)
- `organizationId` — exists in the system (referenced org is real)
- `municipalityId` — set (Rule #21 still applies)
- `interestId` — set
- `isPublished: true` ONLY if all the above are valid; otherwise `false`

**Pre-create gate (MANDATORY before POST /admin/places):**
```js
function validatePlace(plan) {
  const fails = [];
  if (!plan.title || !plan.title.trim()) fails.push('empty-title');
  if (!plan.address || !plan.address.trim()) fails.push('empty-address');
  if (!plan.lat || plan.lat === 0) fails.push('zero-lat');
  if (!plan.lng || plan.lng === 0) fails.push('zero-lng');
  if (!plan.organizationId) fails.push('no-orgId');
  if (!plan.municipalityId) fails.push('no-muniId');
  if (!plan.interestId) fails.push('no-interestId');
  if (fails.length) throw new Error('Refusing to POST broken place: ' + fails.join(','));
  return true;
}
```
Run `validatePlace(plan)` BEFORE every `POST /admin/places`. If it throws, fix the plan; do NOT POST.

**PATCH protection (this is where venues silently break):**
When PATCHing an existing place to update one field (e.g. `municipalityId`), the backend may CLEAR other unspecified fields (this happened to Vaxholm + Danderyd places in 2026-04-15 — `address`, `lat`, `lng` got reset to empty/0 after a `municipalityId`-only PATCH). PATCH protocol:
1. GET the existing place first.
2. Build the PATCH body INCLUDING all critical fields: `title, address, lat, lng, organizationId, municipalityId, interestId, isPublished`.
3. Override only the field you intend to change.
4. POST the full body — never partial.

**Daily venue audit (run at end of any session that touched places):**
```js
const places = await getAllPlaces();
const broken = places.filter(p =>
  !p.title?.trim() ||
  !p.address?.trim() ||
  p.lat === 0 ||
  p.lng === 0
);
if (broken.length) console.error('BROKEN PLACES:', broken);
```
If any broken places exist, PATCH to fix OR set `isPublished: false` so the mobile app never tries to render them.

**HARD-skip mobile-app crash protection:**
If a place has `isPublished: true` AND any of (empty title, empty address, lat=0, lng=0), the mobile app will:
- Show the venue card with no name (broken UX)
- Possibly **crash to homepage** when user taps it (the actual incident on 2026-04-15)
- Consume an event slot in the feed without working content

If you discover such a place during ANY work — even unrelated — set `isPublished: false` immediately. Don't wait to fix everything; unpublish first, fix later.

**Anti-patterns (HARD MISTAKES — these have been observed):**
- ❌ POSTing a place to "probe the API" without a real title/address (the empty Danderyd test place from 2026-04-14)
- ❌ Leaving lat/lng as `0/0` because the source didn't have coords — this breaks the map view AND push 50km radius
- ❌ PATCHing only `municipalityId` and accidentally clearing address/lat/lng (the Vaxholm general venue regression)
- ❌ Setting `isPublished: true` on places that will be filled in "later"
- ❌ Skipping the validatePlace gate "just for this test" — every test creates a real DB row that goes live

**Real-world incident report (the reason this rule exists):**
On 2026-04-14, during early API probing for the Danderyd batch, the agent POSTed a place with `organizationId` only — no title, no address, lat/lng=0, but `isPublished: true`. The empty venue propagated to the mobile app. When the CEO opened the app to demo to investors, the home feed referenced this venue → tapping it crashed the app back to the homepage. Investor + engineer + CEO Slack thread spent multiple hours diagnosing. Root cause: Claude created a broken venue and never cleaned it up. Fix protocol: this rule. Never again.

**Why:** Real production damage. Real CEO impact. Real investor visibility. The cost of one broken venue is dramatically higher than the cost of an extra validation step. validatePlace() runs in microseconds; the alternative is a multi-hour incident.

---

## Rule #33: Organizer (Organization) Completeness — NEVER Create an Organizer Without Logo + Contact Fields (CRITICAL — Mobile Black Screen)

**Severity:** CRITICAL. Incomplete organizers render as blank black screens on the Famies mobile app when users tap them.

**Schema — every organizer has these fields:**
```
organizationId, name, avatar, isPartnered, isGovernment,
phoneNumber, email, website, instagram, facebook, youtube
```

**HARD REQUIREMENTS — an organizer MUST have:**

1. **`name`** — non-empty, specific (not "kommun" alone; use "Nynäshamns kommun")
2. **`avatar`** — REQUIRED. Must be **1:1 square**, **250x250 or 500x500 px minimum**. Logo should be **centered with padding** so it looks balanced on the circular mobile crop. Kommun coat-of-arms (kommunvapen) from Wikipedia Commons is the standard for government entities.
3. **`email`** — at least one contact email (e.g., `kommun@nynashamn.se`, `info@bibliotek.se`)
4. **`phoneNumber`** — kommun switchboard or organizer main phone (Swedish format: `08-520 680 00`)
5. **`website`** — official website URL (https://...)
6. **`isGovernment`** — set to `true` for kommuns, biblioteks, svenska kyrkan, state-funded entities
7. **`isPartnered`** — `false` unless explicitly confirmed as paid Famies partner
8. **At least ONE social:** `instagram` OR `facebook` (both preferred). **MUST be full URI** — backend validates with `format: "uri"`. Use `https://www.instagram.com/nynashamnskommun` NOT the bare handle `nynashamnskommun` (400: `/body/instagram must match format "uri"`).
9. **`youtube`** — optional but add if kommun has an active channel

**If any of the 7 required fields (name, avatar, email, phoneNumber, website, isGovernment set, ≥1 social) is missing → DO NOT create the organizer yet. Gather first, then post.**

### Pre-Create Validation Gate

```js
function validateOrganization(plan) {
  const fails = [];
  if (!plan.name || !plan.name.trim()) fails.push('empty-name');
  if (!plan.avatar) fails.push('no-avatar-logo');
  if (!plan.email) fails.push('no-email');
  if (!plan.phoneNumber) fails.push('no-phone');
  if (!plan.website) fails.push('no-website');
  if (plan.isGovernment === undefined || plan.isGovernment === null) fails.push('isGovernment-unset');
  if (!plan.instagram && !plan.facebook) fails.push('no-social');
  // URI validation — backend 400s on bare handles
  const uriFields = ['website', 'instagram', 'facebook', 'youtube'];
  for (const f of uriFields) {
    if (plan[f] && !/^https?:\/\//i.test(plan[f])) fails.push(f + '-not-uri');
  }
  if (fails.length) throw new Error('Refusing to POST broken organization: ' + fails.join(','));
  return true;
}
```

Run validateOrganization() **before every POST /admin/organizations**. Never bypass, never `// TODO: fill in later`.

### Duplicate-Organizer Pre-Check (MANDATORY before every POST)

Backend enforces unique constraint on `(email, phoneNumber, website)` — a POST with fields matching an existing org returns `400: Query error, code 23505` (Postgres unique violation). This fails AFTER you've already wasted the image upload + form fill.

**ALWAYS search first:**

```js
async function findExistingOrg(name, email, website, headers) {
  let page = 1;
  while (page <= 20) {
    const r = await fetch('https://api.famies.app/admin/organizations?limit=100&page=' + page, { headers });
    const d = await r.json();
    const arr = d?.data?.organizations || [];
    if (!arr.length) return null;
    const match = arr.find(o =>
      (name && o.name?.toLowerCase() === name.toLowerCase()) ||
      (email && o.email === email) ||
      (website && o.website?.replace(/\/$/,'') === website.replace(/\/$/,''))
    );
    if (match) return match;
    if (arr.length < 100) return null;
    page++;
  }
  return null;
}

// Usage:
const existing = await findExistingOrg('Vaxholms stad', 'kansliet@vaxholm.se', 'https://www.vaxholm.se', headers);
if (existing) {
  console.log('Reuse existing org:', existing.organizationId);
  // Use existing.organizationId; DO NOT POST a new one
} else {
  validateOrganization(plan);
  // proceed with POST
}
```

**If a duplicate is found** — reuse the existing organizationId. Do not create a second one. The Vaxholm incident (2026-04-15) created 2 "Vaxholms stad" orgs because the duplicate check was skipped; merging them later required renaming one to `[Legacy 2025]` and reconciling unique-field conflicts.

### Logo Sourcing Protocol (1:1 centered, 250x250+)

**Priority order for sourcing an organizer logo:**

1. **Official kommun/entity website** — check favicon + "press/media kit" page; many kommuns publish their kommunvapen as PNG
2. **Wikipedia Commons** — every Swedish kommun has a `File:[Kommun] kommunvapen.png` or `.svg` with multiple resolutions. Example: `https://upload.wikimedia.org/wikipedia/commons/thumb/.../500px-...png`. Always use ≥500px source.
3. **Official Facebook/Instagram profile picture** — if both above fail, download the organization's FB/IG profile photo (already square).
4. **Generate square crop with padding** — if the best available logo is non-square, pad with white/transparent background so the final image is 1:1. Logo must be **centered with ≥10% padding on all sides** so the mobile app's circular crop doesn't clip it.

**After sourcing:**
- Resize to 500x500 PNG (preferred) or 250x250 minimum
- POST to `/admin/image` with `multipart/form-data` to get the Famies CDN URL
- Use that URL as `avatar` value in the organizer POST

**If no logo can be sourced:** DO NOT create the organizer. Either skip the event (if it's a single event) or escalate to the user for a manual logo.

### Contact Info Sourcing Protocol

For Swedish kommun organizers, the `/kontakt` or `/kontakta-oss` page has everything:

- Email: always `kommun@[kommun].se` (e.g., `kommun@nynashamn.se`, `kommun@nykvarn.se`) — if not present, try `info@` or `[kommun]@[kommun].se`
- Phone: main switchboard (växel), Swedish format with space groups
- Social handles: scan the footer — every kommun has IG + FB in the footer

For non-kommun organizers (bibliotek, svenska kyrkan, kulturhus, museums):
- Bibliotek: email usually `bibliotek@[kommun].se`, phone on contact page
- Svenska kyrkan: website always `svenskakyrkan.se/[församling]`, email + phone on the församling page
- Museums/kulturhus: contact page + FB/IG on every public-facing site

**If the source won't load** (Cloudflare, geo-block) → use the kommun's main contact page; most kulturhus are operated by kommuns anyway.

### PATCH Protocol — Always Send Full Body (Same as Rule #32)

When updating an organizer, the backend may clear unspecified fields. Always PATCH with the **full object** you want in the final state, not just the changed field:

```js
// ❌ WRONG — will clear email, phone, etc.
await fetch('/admin/organizations/' + id, { method: 'PATCH', body: JSON.stringify({ avatar: newUrl }) });

// ✅ RIGHT — sends full desired state
const current = await (await fetch('/admin/organizations/' + id, { headers })).json();
const full = { ...current.data, avatar: newUrl };
await fetch('/admin/organizations/' + id, { method: 'PATCH', body: JSON.stringify(full) });
```

### Daily Audit Script

Run this at the start of every Famies session to catch any broken organizer before it hits mobile:

```js
async function auditOrganizers(headers) {
  const r = await fetch('https://api.famies.app/admin/organizations?limit=100&page=1', { headers });
  const orgs = (await r.json())?.data?.organizations || [];
  const broken = orgs.filter(o =>
    !o.avatar || !o.email || !o.phoneNumber || !o.website ||
    (!o.instagram && !o.facebook)
  );
  if (broken.length) console.warn('BROKEN ORGS:', broken.map(o => o.name));
  return broken;
}
```

If `broken.length > 0` → fix before creating ANY new content.

### Anti-Patterns (HARD MISTAKES — these have been observed on 2026-04-14/15)

- ❌ POSTing `{ name: "Nynäshamns kommun", isGovernment: false }` and nothing else — this is what caused mobile black screen
- ❌ Using a non-square logo and letting the mobile app stretch/crop badly
- ❌ Copying the event's venue image as the organizer logo (wrong aspect, wrong meaning)
- ❌ Creating organizer-first and planning to "enrich later" — later never comes
- ❌ Setting `isGovernment: false` on kommuns (disables government badge in app)
- ❌ Using bare handles for `instagram`/`facebook`/`website` (backend requires full `https://` URI — validation error `/body/instagram must match format "uri"`)
- ❌ POSTing a new organizer without first checking if one already exists by name/email/website (creates duplicates, then 400s on unique constraint — see Duplicate-Organizer Pre-Check above)

### Real-World Incident Report (Why This Rule Exists)

On 2026-04-14 to 2026-04-15, the agent created 4 kommun organizers during Danderyd/Vaxholm/Haninge/Nykvarn/Nynäshamn batches with name-only posts:

- Nynäshamns kommun (340079934422680746) — no avatar, no email, no phone, no social, isGovernment: false
- Nykvarns kommun (340017136472720526) — same
- Vaxholms stad (339626102701982774) — had website + isGovernment, missing everything else
- Haninge kommun (339270162144331424) — partial

Result: mobile app showed **blank black screen** when users tapped any event from these organizers. The Famies CEO noticed during demo. Root cause: the agent focused on events + venues and treated organizers as "just a foreign key" — never sourced the logo or contact details.

**Fix protocol:** this rule. Every organizer POST now runs through `validateOrganization()`. No logo, no POST.

### Why This Rule Exists

The organizer screen is the second page users see after tapping an event. It's supposed to build trust: "this kommun is hosting, here's how to contact them, here's their website." An empty organizer screen on a "government" entity breaks that trust instantly and looks like a broken app.

One complete organizer = one extra GET to the kommun's /kontakt page + one logo download. Cost: 2 minutes per organizer. Value: mobile screen renders correctly forever.
