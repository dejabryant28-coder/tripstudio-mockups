# Trip Studio: Manus 1.6 Mockup vs. Live Site - Transition Guide

## How to Use This Document

This is the master reference for bringing the live Trip Studio (built by Claude on mamedeeworld.com) into exact alignment with the Manus 1.6 HTML mockups. Give this entire document to Claude along with the HTML step files.

---

## File Index (What Each Step File Shows)

| File | What You See When You Open It |
|------|-------------------------------|
| Step 01 - Dashboard.html | The main admin dashboard with hero, stats, focus cards |
| Step 02 - Client Trips.html | All trips listed with cards, filters, search |
| Step 03 - The Vault.html | Smart library with templates, destinations, resources, notes |
| Step 04 - New Client - Upload Questionnaire.html | Step 1 of wizard: drag-and-drop questionnaire upload |
| Step 05 - New Client - Upload Consultation.html | Step 2 of wizard: consultation notes upload |
| Step 06 - New Client - Generated Client Profile.html | Step 3: AI-populated profile with hero image builder |
| Step 07 - Section Selector Popup.html | The popup asking Flights / Accommodation / Transportation |
| Step 07b - Flight Builder Cash Tab.html | Flight form with Cash payment selected |
| Step 07c - Flight Builder Points and Miles Tab.html | Flight form with Points/Miles: bank cards, transfer partners |
| Step 08 - Accommodation Builder.html | 3 hotel options side-by-side with photos and rates |
| Step 09 - Transportation Builder.html | Rideshare apps, transit cards, private transfers |
| Step 10 - Itinerary Builder.html | Day-by-day drag-and-drop with morning/afternoon/evening |
| Step 11 - Budget Calculator.html | Live-updating cost breakdown with toggles |
| Step 12 - Trip Detail Overview.html | Full trip summary with checklist and quick actions |
| Step 13 - Command Center.html | Email tracking, follow-ups, Mark Paid and Unlock |
| Step 14 - Dream Preview Admin.html | Day lock controls, email/SMS preview |
| Step 15 - Trip Unlocked Client Page.html | What the client sees after payment (full trip) |

---

## What Is Different Between Mockup and Live Site

### GLOBAL DIFFERENCES (affect every page)

**IMPORTANT UPDATE:** The sidebar and Agent Dee have been redesigned since the original mockups. Use the LIVE SITE version (Image 2 below) as the correct reference for these elements, NOT the original mockup HTML files.

**Sidebar (use live site style):**
- Nav items: Dashboard (home icon), Client Trips (monitor icon), New Trip (+ icon), Vault (lock icon), then SETTINGS section with Settings (gear icon)
- No badge count on Client Trips
- "Exit to WordPress" link near the bottom
- Agent Dee photo avatar at the very bottom ("Agent Dee" / "AI Assistant" in gold)
- No "MD" initials circle - use Agent Dee's actual photo instead

**Agent Dee (use live site style):**
- Appears as sidebar footer item with her real photo (not cartoon mascot)
- Photo is the librarian-style AI avatar (assets/agent-dee.png)
- Clicking her opens the chat panel
- NO floating mascot illustration in bottom-right corner
- The notification bubble ("Sarah & Michael's Lisbon preview is ready to send") appears from Agent Dee, not a floating character

| Element | Correct (Live Site) | Fix Needed |
|---------|-------------------|-----|
| Topbar search | Has "Search trips, clients, destinations" input | Keep as-is |
| Notification bell | Bell icon with rose dot indicator | Keep as-is |
| Topbar date | Day + date in italic Cormorant Garamond | Keep as-is |
| Greeting | "Good evening, Deja" (time-aware) | Keep as-is |
| Sidebar nav | Dashboard, Client Trips, New Trip, Vault, Settings | Keep as-is |
| Sidebar bottom | "Exit to WordPress" + Agent Dee photo avatar | Keep as-is |
| Agent Dee | Photo avatar in sidebar footer, opens chat | Keep as-is |
| WordPress bleed | App should completely cover wp-admin | Fix z-index/positioning |
| Font: body | DM Sans 14px | Standardize to DM Sans 14px |
| Scrollbar | 4px wide, gold thumb | Add scrollbar CSS |

### PAGE-SPECIFIC DIFFERENCES

**Dashboard (Step 01)**

| Element | Mockup | Live | Fix |
|---------|--------|------|-----|
| Hero text | "You're creating unforgettable journeys." | "Today you build a brand that outlives the trend." | Change to mockup text |
| Stat labels | ACTIVE TRIPS, PREVIEW SENT, AWAITING PAYMENT, PIPELINE VALUE | ACTIVE TRIPS, DUE IN 30 DAYS, NEED ATTENTION, PIPELINE VALUE | Change labels |
| Stat card decoration | Subtle wave/line graphic in corner | None | Add decorative SVG |
| Dee's Daily Briefing | Not in mockup | Present (Claude added) | KEEP (good addition) |
| Dee's One Thing | Not in mockup | Present (Claude added) | KEEP (good addition) |

**Client Trips (Step 02)**

| Element | Mockup | Live | Fix |
|---------|--------|------|-----|
| Hero banner | None - goes straight to page header | Has full hero image banner | Remove hero banner |
| Sort control | "Sort: Newest" dropdown | Missing | Add sort dropdown |
| View toggle | Grid/list icon buttons | Missing | Add view toggle |
| Card: pin icon | Rose pin icon before destination | Missing | Add pin SVG |
| Card: traveler count | "2 Travelers" shown | Missing | Add traveler count |
| Empty state | Dashed border card with "+" | Missing | Add empty state card |

**The Vault (Step 03)**

| Element | Mockup | Live | Fix |
|---------|--------|------|-----|
| Hero/stats banner | None - goes straight to category pills | Has "The Vault" hero with stats | Remove hero banner |
| Category pill counts | All 92, Templates 12, Destinations 32, Resources 24, Notes 8, Inspiration 16 | Different counts or missing | Match mockup counts (or wire to real data) |

**New Client Wizard (Steps 04-07)**

| Element | Mockup | Live | Fix |
|---------|--------|------|-----|
| Progress bar | 5 circles with connecting lines, gold=done, rose=active, gray=pending | May differ in styling | Match exact mockup styling |
| Upload zone | Dashed gold border, centered icon + text + file type pills | Basic upload area | Match mockup exactly |
| Processing animation | Spinner + step-by-step progress items (dots turning green) | May be simpler | Match mockup animation |
| Section selector | 3 boxes in a popup: Flights, Accommodation, Transportation | May not exist as popup | Build as modal popup |
| Hero image builder | 3 buttons: Regenerate, Upload Image, Paste URL + AI badge | Exists but may differ | Verify matches mockup |

**Flight Builder (Steps 07b, 07c)**

| Element | Mockup | Live | Fix |
|---------|--------|------|-----|
| Cash/Points tabs | Pill toggle bar | May differ | Match mockup tab style |
| Upload methods | "Upload PDF or Screenshot" + "Paste Flight URL" side by side | May differ | Match mockup layout |
| Auto-extracted badge | Green/sage "AUTO-EXTRACTED FROM UPLOADED CONFIRMATION" | May be missing | Add badge |
| Form fields (Cash) | Airline, Flight Number, Cabin Class, Departure City, Arrival City, Trip Type, Departure/Arrival Date+Time, Duration, Stops, Total Cost, Per Person | Verify all present | Add any missing |
| Points/Miles: Bank cards | Chase, Amex, Capital One, Citi, Bilt as selectable cards | May be dropdown | Match mockup (cards) |
| Points/Miles: Program | Auto-fills based on bank selection (readonly) | Verify | Wire auto-fill |
| Points/Miles: Transfer Partner | Dropdown | Verify | Add if missing |
| Flight counter | Dot indicators "1 of up to 6 flights" | May differ | Match mockup |
| Add Another Flight | Link with dots | May differ | Match mockup |

---

## Pages That Do Not Exist Yet on Live Site

These need to be built from scratch using the mockup HTML as the exact visual reference:

1. **Step 08 - Accommodation Builder** - 3 options side-by-side, photo upload, auto-save to Vault
2. **Step 09 - Transportation Builder** - Rideshare apps by destination, transit cards, private transfers
3. **Step 10 - Itinerary Builder** - Drag-and-drop day cards, AI day vibes, Vault autocomplete
4. **Step 11 - Budget Calculator** - Live recalculation, per-person/total toggle
5. **Step 12 - Trip Detail Overview** - Full summary, checklist, quick actions
6. **Step 13 - Command Center** - Email tracking, follow-up automation, Mark Paid and Unlock
7. **Step 14 - Dream Preview Admin** - Day lock controls, email/SMS preview and send
8. **Step 15 - Trip Unlocked Client Page** - Client-facing page at unique URL

---

## Claude Prompt (Copy and Paste This Entire Section)

```
I need you to bring the Trip Studio admin pages on mamedeeworld.com into exact visual alignment with the Manus 1.6 HTML mockups, then build the remaining pages that don't exist yet.

CRITICAL RULES:
- Copy the HTML mockups EXACTLY. Every color, font, layout, icon, spacing.
- Use the CSS variables from design-system.md
- Fonts: Playfair Display (headings), Cormorant Garamond (italic quotes/dates), DM Sans (UI/body)
- Icons: Use the inline SVGs from the mockup HTML files. NO emojis. NO Font Awesome.
- No em dashes anywhere. Use commas, periods, or plain hyphens.
- Backup before every change (WPvivid or manual copy).
- Deploy via File Manager Advanced plugin (Theme Editor loopback is broken).
- Code lives in hello-elementor-child theme functions.php (child theme, safe from parent updates).

WHAT EXISTS AND NEEDS FIXING (priority order):

1. GLOBAL: Fix WordPress admin bleed-through (app must cover wp-admin completely)
2. GLOBAL: Add topbar search bar ("Search trips, clients, destinations")
3. GLOBAL: Add notification bell with rose dot indicator
4. GLOBAL: Add date in italic Cormorant Garamond to topbar
5. GLOBAL: Change "Welcome back" to time-aware "Good morning/afternoon/evening, Deja"
6. GLOBAL: Sidebar should match the LIVE site (not original mockup): Dashboard, Client Trips, New Trip, Vault, Settings nav items + "Exit to WordPress" link + Agent Dee photo avatar at bottom
7. GLOBAL: Agent Dee is a PHOTO avatar in the sidebar footer (assets/agent-dee.png), NOT a cartoon mascot. Clicking opens chat panel.
8. GLOBAL: NO floating mascot illustration in bottom-right corner. Dee lives in the sidebar only.
9. Dashboard: Fix stat labels to "Preview Sent" and "Awaiting Payment"
10. Client Trips: Remove hero banner (go straight to page header)
11. Client Trips: Add Sort dropdown + grid/list view toggle
12. Client Trips: Add pin icon + traveler count to cards
13. Vault: Remove hero/stats banner (go straight to category pills)
14. New Client Wizard: Verify all 5 steps match mockup exactly
15. Flight Builder: Verify Cash and Points/Miles tabs match mockup exactly

WHAT NEEDS TO BE BUILT FROM SCRATCH (after fixes):

Phase 4: Accommodation Builder (match Step 08 HTML exactly)
Phase 5: Transportation Builder (match Step 09 HTML exactly)
Phase 6: Itinerary Builder (match Step 10 HTML exactly)
Phase 7: Budget Calculator (match Step 11 HTML exactly)
Phase 8: Trip Detail (match Step 12 HTML exactly)
Phase 9: Command Center (match Step 13 HTML exactly)
Phase 10: Dream Preview Admin (match Step 14 HTML exactly)
Phase 11: Trip Unlocked Client Page (match Step 15 HTML exactly)

BACKEND REQUIREMENTS:
- Every hotel, activity, restaurant saved in any builder must auto-save to the Vault (mdtw_vault table)
- Autocomplete in all builders queries Vault first, then Google Places API
- AI integration: OpenAI for document parsing, day vibe summaries, follow-up emails
- Email from support@mamedeeworld.com with branded templates
- Client pages at unique URLs: mamedeeworld.com/trip/client-name-destination-year
- "Mark Paid and Unlock" in Command Center flips a DB flag, same URL shows full trip

DESIGN SYSTEM (non-negotiable):
- --bg-deep: #0D0B0F
- --bg-card: #16121A
- --bg-card2: #1C1722
- --accent-gold: #C9A96E
- --accent-rose: #D4848A
- --accent-sage: #8DAF9B
- --text-primary: #F5EFE6
- --text-muted: #9A8F8A
- --text-label: #C9A96E
- --border: rgba(201,169,110,0.18)
- Cards: 16px border-radius, dark glass with subtle gold border
- Buttons: pill-shaped, gold gradient or ghost with gold border
- Status badges: rose=draft, gold=in progress, sage=complete
- Sidebar: 248px, gradient background, gold accent on active items

Start by confirming you can see all the HTML step files, then begin with the global fixes (items 1-8) since they affect every page. Take a backup first.
```

---

## Technical Notes for Claude

- The code currently lives in `wp-content/themes/hello-elementor-child/functions.php` (child theme)
- There is also `functions-addon.php` with database tables and REST endpoints
- The Vault data backbone (mdtw_vault table + auto-save hooks + search endpoint) is already deployed
- REST namespace: `mdtw/v1`
- Database prefix: `mdtw_` (not `ts_` as the original handoff doc suggested)
- Theme auto-updates are disabled
- The public-facing SPA lives at `trip-studio.php` (served at mamedeeworld.com/trip-studio)
- PHP OPcache is active on this shared host (changes may take a moment to reflect)
- The mascot illustration PNG is in the `assets/` folder (mascot.png)
