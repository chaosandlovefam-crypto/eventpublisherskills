# Source Cleanup Audit — 6 Cities (2026-04-15)

Based on actual scraping results from sessions 2026-04-14 and 2026-04-15.
Threshold: per Rule #19, sources yielding < 2 unique events should be removed.
Single-event "gem" sources (Mors Dag, Körkonsert, Nationaldagsfirande etc.) are kept per the gem exception.

---

## 🟢 KEEP (high-yield primary + niche gems)

These are productive sources that consistently yield ≥ 2 unique family-relevant events.

### Vallentuna
- ✅ `https://www.vallentuna.se/evenemang-och-upplevelser/evenemangskalender/` — primary, 73 events
- ✅ `https://bibliotek.vallentuna.se/aktiviteter#/` — bibliotek, 2 unique (Bokklubb, Sagostund KUBen)
- ✅ `https://www.facebook.com/vallentunakulturhus/events/?id=100066890562317&sk=events` — kulturhus FB, 1 gem (KUBenSöndag)

### Danderyd
- ✅ `https://www.danderyd.se/evenemang/` — primary, 22 events
- ✅ `https://bibliotek.danderyd.se/evenemang` — bibliotek (mörby centrum)

### Vaxholm
- ✅ `https://www.destinationvaxholm.se/en/sv/kommande-evenemang` — primary kommun events, 24 events
- ✅ `https://www.svenskakyrkan.se/kalender?q=Vaxholm` — church, 3 events (gem)

### Värmdö
- ✅ `https://www.varmdo.se/upplevaochgora/evenemang.4.62b6567e177d2c33d13c3489.html` — primary, 8 events
- ✅ `https://www.varmdo.se/upplevaochgora/evenemang/bibliotek.4.3789b5a6187080ee79c7feb.html` — bibliotek, 6 events
- ✅ `https://artipelag.se/hander-pa-artipelag/` — culture venue, 5 events
- ✅ `https://www.svenskakyrkan.se/varmdo/kalender` — church, 3 events
- ✅ `https://gustavsbergsporslinsmuseum.se` — museum, 3 events
- ✅ `https://www.siggestagard.se/kalendarium` — gård, 3 events

### Haninge
- ✅ Haninge primary kommun source — 67 events earlier batch
- ✅ Haninge bibliotek source

### Nykvarn
- ✅ `https://nykvarn.se/uppleva-och-gora/evenemang/evenemangskalendern` — primary, 5 events
- ✅ `https://www.taxingeslott.se/kalender/` — slott, 4 events
- ✅ `https://www.svenskakyrkan.se/kalender?q=Nykvarn` — 1 gem (Körkonsert)
- ✅ `https://www.bokabord.se/evenemang/nykvarn` — 1 gem (Mors Dag at Vidbynäs)

---

## 🔴 REMOVE (yielded 0-1 unique non-gem events)

These should be removed from the master spreadsheet — they consistently waste batch time without adding value.

### Vallentuna — REMOVE 4
- 🔴 `https://www.facebook.com/places/Things-to-do-in-Vallentuna/103138059726221/` — only adult events (motorcycle expo, makeup outlet, popup shop)
- 🔴 `https://www.vallentuna.se/fritid-och-kultur/kultur/evenemang/` — brochure download page, no events
- 🔴 `https://www.facebook.com/vallentunacentrum.se/events` — all 4 events past 2019-2025 (Rule #18)
- 🔴 `https://www.instagram.com/vallentunakulturhus` — IG can't be scraped without login + scroll-loaded

### Danderyd — REMOVE 3
- 🔴 `https://www.facebook.com/danderydskommun/events` — 1 unique only, all others duplicates of kommun events
- 🔴 `https://www.tickster.com/se/sv/events/by/2r3mc57m605z1u9/danderyds-kommun` — 0 unique (duplicates)
- 🔴 `https://allevents.in/danderyd#` — 0 unique

### Vaxholm — REMOVE 8
- 🔴 `https://www.destinationvaxholm.se/en/events` — duplicate of /sv/kommande-evenemang
- 🔴 `https://www.facebook.com/vaxholmsstad/events` — only past events (Rule #18)
- 🔴 `https://www.vaxholm.se/uppleva--gora/evenemang` — duplicate content of destinationvaxholm
- 🔴 `https://www.stromma.com/sv-se/stockholm/utflykter/dagsutflykter/` — Stockholm-wide tours, no Vaxholm-specific events
- 🔴 `https://www.waxholmshotell.se/evenemang` — hotel events (adult-leaning, 0-1 unique)
- 🔴 `https://bio.se/biografer/vaxholms-biografteater-2` — cinema (could keep if treated as venue, but movies are paid-per-show, low yield)
- 🔴 `https://www.waxholmsgolfklubb.se/` — sports club, not public events
- 🔴 `https://vaxholmstennisklubb.se/kalender` — sports club, not public events

### Värmdö — REMOVE 8
- 🔴 `https://evenemang.se/se/stockholms-län/värmdö` — Cloudflare 403 blocked, can't scrape
- 🔴 `https://www.instagram.com/varmdokommun` — IG, can't scrape
- 🔴 `https://www.facebook.com/varmdokommun/events` — only past events (Rule #18)
- 🔴 `https://gustavsbergshamn.se/kalender/` — only 2025 past events
- 🔴 `https://www.facebook.com/gustavsbergsporslinsmuseum/events` — duplicate of museum site
- 🔴 `https://www.djuronaset.com/evenemang/` — adult-only (pianobar, champagne, brunch)
- 🔴 `https://www.sandhamn.com/sv/kalender` — empty calendar (hotel only)
- 🔴 `https://mojadansbana.se/kalender/` — only 1 upcoming, mostly past
- 🔴 `https://www.gustavsbergsbadet.se/upplevaochgora/evenemang.4.62b6567e177d2c33d13c3489.html` — duplicate of varmdo.se primary

### Haninge — REMOVE
- 🔴 `https://evenemang.se/se/stockholms-län/haninge` — Cloudflare blocked (same as Värmdö)
- 🔴 `https://tickster.com/se/nb/events/by/1xel5zrbvg1enf4/haninge-kultur` — to be re-checked but likely low-yield
- 🔴 `https://www.eventbrite.com/d/sweden--haninge/events/` — only US online webinars
- 🔴 `https://www.facebook.com/events/search/?q=Haninge%2C%20Sweden` — login + Rule #18

### Nykvarn — REMOVE 9
- 🔴 `https://www.instagram.com/nykvarnskommun/` — IG, can't scrape
- 🔴 `https://www.facebook.com/Nykvarnskommun/events` — only past events
- 🔴 `https://www.tickster.com/se/sv/events/in/nykvarn` — "no events found"
- 🔴 `https://evenemang.se/se/stockholms-län/nykvarn?c=standup` — Cloudflare blocked
- 🔴 `https://www.laget.se/NykvarnsIBF` — sports team page, calendar 404 without specific team URL
- 🔴 `https://www.laget.se/NykvarnsSK/Event/Month/2025/12/2?eventid=29194709` — single dated link (already past)
- 🔴 `https://www.eventbrite.com/d/sweden--nykvarn/events/` — only US online webinars
- 🔴 `https://www.facebook.com/events/search/?q=Nykvarn%2C%20Sweden` — login + Rule #18
- 🔴 `https://www.ticketmaster.se/search?q=Nykvarn` — 0 results

---

## 📊 Summary

| City | Total in sheet | Keep | Remove |
|---|---|---|---|
| Vallentuna | 12 | 3 | 4 (others are unverified) |
| Danderyd | 6 | 2 | 3 |
| Vaxholm | 14 | 2 | 8 |
| Värmdö | 19 | 6 | 9 |
| Haninge | 10 | 2 | 4 |
| Nykvarn | 13 | 4 | 9 |

**Total to remove: ~37 low-yield URLs across the 6 cities.**

After cleanup, the spreadsheet will only contain sources that have proven to yield ≥ 2 unique events OR a single high-value gem.

---

## Note on patterns to AVOID adding for future cities

Based on this audit, these source patterns are systematically low-yield across all small-to-medium Swedish kommuns:

1. **Instagram pages** — can't scrape without login + scroll
2. **Eventbrite by city** — returns US online webinars, not local events
3. **Ticketmaster search** — returns 0 results for small cities
4. **Tickster organizer pages** — usually duplicates kommun events
5. **Facebook /events pages of small kommuns** — mostly past events (Rule #18)
6. **Facebook /events/search?q=City** — login required + mostly past
7. **evenemang.se** — Cloudflare blocks scraping
8. **Sports team pages (laget.se)** — game schedules not in standard calendar format
9. **Sports clubs (golf/tennis/etc.)** — not public events, member-only
10. **Hotel kalender pages** — usually offers/conferences, not family events

For each new city, only add: official kommun page + bibliotek + 1-2 main culture venues + svenska kyrkan.
