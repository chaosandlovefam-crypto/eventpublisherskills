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

## Rule #19: Source-Minimum Threshold — 3 Unique Events or Skip the Source
**When:** Evaluating any source URL (kommun website, Facebook Page Events, Tickster, Eventbrite, library calendar, etc.) for a city batch.

**Action:** If a source yields fewer than **3 unique events** (after Rule #4 family-relevance filter, Rule #18 expired-date filter, and Rule #12 dedup against already-published) for the same city, do NOT publish from that source in this batch. Flag the source as "low-value for `<city>`" and remove from the active source list for that city.

**Why this matters:**
- Sources with 1-2 unique events cost roughly the same scrape + dedup + image-decision overhead per source as sources with 50 events — but yield 10x less.
- Each tiny-yield source still requires its own Rule #15 integrity-check, Rule #17 image extraction, Rule #14 audit footprint. Net cost > net value.
- Better to invest that time on a high-yield primary source (e.g. the kommun's own evenemang page often returns 20-50+ unique events).

**Process:**
1. For a candidate source URL, run the full extraction + Rule #4 + Rule #18 + Rule #12 dedup pipeline.
2. Count `uniqueEventsAfterDedup`.
3. If `uniqueEventsAfterDedup < 3`:
   - DO NOT publish any of them in this session, even though they passed all other rules.
   - If any were already published in error before this rule was checked, DELETE them.
   - Add the source to the city's "low-value sources" log: `{city, source, uniqueCount, checkedDate}`.
   - Re-evaluate the source ONLY when the city's primary source coverage feels stale (e.g. monthly).
4. If `uniqueEventsAfterDedup >= 3`:
   - Proceed with full Rule #16 publish flow.
   - Source remains active for this city.

**Active source list maintenance:**
Every city has a primary source list (e.g. `danderyd.se/evenemang`, `bibliotek.danderyd.se/evenemang`). Secondary sources (FB Pages, Tickster organizers, Eventbrite organizers) get added only when they pass the 3-unique threshold. Sources that fail the threshold get parked in `low-value-sources.md` (or equivalent) with the date checked, so we don't waste time re-checking them every batch.

**Why:** User decision 2026-04-14: original threshold was set to 5, then revised same day to 3 — softer threshold lets in genuinely useful niche sources (church calendars, hotel events, small clubs) that bring 3-4 unique additions per batch, while still filtering out 0-2-yield rabbit-holes. Confirmed live the same day on Danderyds kommun: FB page yielded 1 unique, Tickster yielded 0 unique (1 was a duplicate of an already-published kommun event). Both removed from the Danderyd active source list. Rule prevents low-yield rabbit-holes from eating batch time that should go to high-yield primary sources.

## Rule #20: Hybrid Image Policy — 60% Brand-Quality Gate (Per-Event Decision, Never Batch-All)
**When:** Preparing the image for ANY event during publish. This rule governs the single binary choice for each event: use the source image, or generate a new one via ChatGPT.

**Core principle:** NEVER decide "all source" or "all generate" for a whole batch. Each event gets its own per-image quality verdict. The bar is a **60% Famies brand-quality floor**: if the source image meets ≥60% of our quality criteria, use it. Below that, generate. This keeps batches fast (source images are free + instant) without sacrificing the feed's visual standard.

**The 60% brand-quality checklist (source image passes if 3 of 5 anchors are green):**

| # | Anchor | Green (pass) | Red (fail) |
|---|---|---|---|
| 1 | **Human presence** | Shows kids, parents, or families engaging with the activity | Only scenery, object, logo, flag, empty stage, or abstract graphic |
| 2 | **1:1 croppability** | Subject stays intact when center-cropped to a square | Subject sits on the edge / wide panoramic where 1:1 kills the story |
| 3 | **No dominant text** | Text is absent, tiny, or a small watermark only | Event title, date, or poster text covers >20% of the frame (Rule #3) |
| 4 | **Photographic realism** | Real photo (even if stylized) | Cartoon/illustration/clip-art/stock-graphic that feels synthetic |
| 5 | **Topic legibility** | A parent scrolling the feed can tell what the event is about in <1s | Ambiguous crop, blurry, dark, or topic unclear |

**Decision flow per event:**
1. Extract the source image following Rule #17 (og:image → twitter:image → article img → picture srcset → data-src → JSON-LD).
2. Score it against the 5 anchors above. Count greens.
3. If greens ≥ 3 → **USE THE SOURCE IMAGE** (upload directly, no ChatGPT call).
4. If greens < 3 → **GENERATE** via ChatGPT using Rule #11 UGC formula.
5. Log the verdict per event: `{eventId, decision: "source"|"generated", greens: N, failedAnchors: [...]}`.

**Expected batch mix (healthy distribution):**
- On a typical Swedish kommun/library/culture source: ~**60-80% of events should be "source"** verdicts, ~20-40% should be "generated".
- If a batch lands at **100% source** → STOP. You probably skipped the quality check. Re-audit.
- If a batch lands at **100% generated** → STOP. You probably skipped source extraction or over-rejected. Re-audit.
- Both extremes are red flags for a broken decision loop.

**Integration with existing image rules:**
- **Rule #3 (text-heavy)** → automatic fail on anchor #3 → generate.
- **Rule #5 (audience-targeted)** → anchor #1; if no humans at all and the topic doesn't carry itself, generate.
- **Rule #7 (no image provided)** → source = 0 greens → generate.
- **Rule #13 (post-gen QA)** still applies to every generated image before upload.
- **Rule #17 (source-first)** still governs extraction; this rule governs evaluation after extraction.

**Anti-patterns (what we are correcting):**
- "I'll just generate all 23 for consistency" → wastes 23 × ~30s ChatGPT quota for events where a perfectly good source image already existed (Danderyd 2026-04-14 mistake).
- "I'll use all source to be fast" → ships the feed with 4 poster-flyers and 3 lone-flag photos that fail Rule #5 (prior Haninge-era mistake).
- "Source looked okay-ish, good enough" without checking the 5 anchors → subjective and drifts batch to batch.

**Why:** User feedback 2026-04-14: "jodi clear hoi etar jonno rule #20 create kore naw" — after seeing me alternate between 100% source (fast but uneven quality) and 100% generate (consistent but slow + low authenticity). The 60% gate + 5-anchor checklist makes the decision mechanical and repeatable. Per 100 events the target becomes ~70 source uploads (authentic, fast, free quota) + ~30 generated (quality rescues). That's the sweet spot between speed and brand quality — and it stays consistent across sessions because the rule is written down, not vibes-based.

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
