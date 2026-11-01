# Baker Family Reunion 2027 — Website Plan

## Goal
A simple, mobile-friendly site that gives every branch of the family one
place for dates, travel, lodging, the schedule and RSVPs.

## Key facts
- **Location:** Sandwich, MA (Cape Cod), with a day trip to Boston
- **Dates:** July 4th week 2027. Proposed core window **Wed Jun 30 – Wed Jul 7**
  (see [travel-research.md](travel-research.md))
- **Coming from:** Bend OR, Portland OR, San Diego CA, Los Angeles CA,
  Atlanta GA, Columbus OH (flying), plus New Jersey, upstate NY and
  Long Beach NY (driving)

## Proposed pages
1. **Home:** title, dates, location, countdown, headline announcements
   (see Home page spec below)
2. **Calendar** (its own tab; see spec below): one calendar with toggle
   views for Travel, Activities and Everything
3. **Travel** (its own tab off Home; see detailed spec below): travel calendar view,
   "where we're coming from" map, BOS vs PVD, city-by-city tips, driving and bridge-traffic tips,
   rental cars and carpools
4. **Accommodation** (its own tab; see spec below): our house's Airbnb
   listing now. Cape Cod rental house suggestions come in early 2027
5. **Schedule:** day-by-day event details (Red Sox game, July 4th
   fireworks, beach day, family dinner, photo). Feeds the Activities
   calendar view
6. **RSVP:** who's coming, arrival and departure dates and flights (feeds
   airport-pickup coordination)
7. **Family:** family tree and photo sharing
8. **FAQ:** what to pack, beaches, kids' activities, contact info

## Home page: spec (not built yet)

The landing page should feel like a save-the-date: big, warm and simple.

**Hero (top of page)**
- Headline: **Baker Family Reunion 2027**
- Dates: **June 30 – July 7, 2027** (update once dates are final)
- Location line: **Sandwich, Massachusetts · Cape Cod · Boston**
  - Sandwich and Cape Cod are home base. Boston is mentioned because of the
    Red Sox outing and because most people fly into Logan.
- Background: a Cape Cod image (beach, dunes or the Sandwich boardwalk), or
  an illustrated Cape outline with a star on Sandwich
- Countdown: "X days until we're on the Cape"

**Below the hero**
- Navigation tabs: Home · Calendar · Travel · Accommodation · Schedule · RSVP ·
  Family · FAQ
- Two or three quick cards linking to the most important pages, e.g.
  "Plan your trip" (Travel), "See the calendar" (Calendar), "RSVP"
- Short announcements area for updates like "Red Sox tickets on sale"

## Calendar page: spec (not built yet)

One calendar covering Sun Jun 27 – Sat Jul 10, 2027, with **toggle tabs** at
the top to switch between views. Each view uses its own color family, and
**Everything** combines them all.

| Tab | Shows | Color family |
|---|---|---|
| **Travel** | Best arrival days, avoid-flying days, best departure days, holiday | Greens, ambers and blues (as in the Travel spec) |
| **Activities** | Red Sox game, July 4th, beach day, family dinner, group photo, etc. | **Red** for the Red Sox game, purple or teal for other activities |
| **Everything** | Travel and activities together | All colors, with a combined legend |

**Behavior**
- Tabs are a simple segmented toggle: `Travel | Activities | Everything`.
  The default view is **Everything**.
- Each day cell shows small color-coded chips (e.g. "⚾ Red Sox @ Fenway",
  "🎆 July 4th"). Tapping a chip opens details: time, place, drive time and
  links.
- The legend below the calendar updates to match the selected tab.
- On phones, the month grid becomes a day-by-day list with the same colors.
- The Travel tab page embeds the **Travel** view, and the Schedule page links
  to the **Activities** view, so there's one calendar and no duplicates to
  keep in sync.
- Colors need enough contrast, and every chip has an icon and label, so
  meaning doesn't rely on color alone.
- Optional: an "Add to my calendar" (.ics) link per event.

**Red Sox game**
- The 2027 MLB schedule is out. The Red Sox are home at Fenway around the
  holiday weekend against the **Baltimore Orioles**. NBC Sports Boston lists
  a game on **Sunday, July 4**, while ticket sites show games on Fri Jul 2
  and Sat Jul 3. Game times are still TBD.
- **To do:** confirm the exact date and time on MLB.com/redsox, pick the
  game and decide on group tickets.
- Fenway is about 1–1.5 hours from Sandwich, longer with holiday traffic.
  Plan carpools or take the Plymouth & Brockton bus from the Sagamore park &
  ride to South Station plus the T. Add a note to the event detail.
- If the family is going to the July 4th game, plan around fireworks: Boston
  (Esplanade) vs. local Cape fireworks that night.
- Possible bonus: a **Cape Cod Baseball League** game (summer collegiate
  league, free, very family-friendly). Several teams play near Sandwich.

## Accommodation tab: spec (not built yet)

Purpose: help families find somewhere to stay on Cape Cod near Sandwich.

**Launch version (keep it simple)**
- Heading: **Where to Stay**
- **Featured: our house.** A card for our house on Airbnb, showing:
  - **Photo carousel** of the house, using the photos from the Airbnb listing
    - Swipe on phones. Arrows and dots on desktop. Don't auto-advance, or
      make it gentle and pause on hover
    - About 6–10 photos: outside, main house, the Old House, bedrooms, yard
      or beach
    - Save copies of the photos into the site (an `images/house/` folder)
      instead of linking to Airbnb's image URLs, which can change or block
      embedding
    - Each photo gets a short caption and alt text (e.g. "The Old House,
      front bedroom")
  - Name or short description of the house
  - **Availability callout**, styled as a badge:
    > 🛏️ **4 bedrooms available for family**
    > - Main house: the upstairs second bedroom
    > - The Old House: all of its bedrooms
  - Optional: a line on how to claim a room (e.g. "Reply on the RSVP form or
    text us"). Mark rooms as taken once claimed
  - A **"View on Airbnb"** button linking to the listing:
    https://www.airbnb.com/h/twentyroos
- **Placeholder notice** below the card, styled as a soft info banner:
  > 🏡 **More places to stay coming soon!** We're gathering rental house
  > suggestions around Sandwich and Cape Cod, and we'll add them here in
  > **early 2027**. Check back later for updates.

**Later version (early 2027)**
- A grid of rental house cards, each with:
  - Photo, name and town (Sandwich, Bourne, Barnstable, Falmouth, etc.)
  - Sleeps X, bedrooms and bathrooms, rough price per night
  - Drive time to the reunion house
  - Link to the listing (Airbnb, VRBO, etc.)
- Optional filters: sleeps 6+, walk to the beach, pet-friendly
- Optional "Who's staying where" list (pulls from RSVP) so families can
  coordinate or share houses
- Tip for families: Cape rentals for July 4th week book up early and many
  are Saturday-to-Saturday. Book soon once options are posted.

## Travel tab: detailed spec (not built yet)

The Travel tab is linked from the main navigation on the Home page. It has
three sections, top to bottom.

### 1. Calendar of proposed dates
This is the **Travel view** of the shared calendar (see Calendar page spec).
A June/July 2027 month view (Sun Jun 27 – Sat Jul 10) with color-coded days
and a small legend:

| Highlight | Days | Meaning |
|---|---|---|
| **Green: best to arrive** | Tue Jun 29, Wed Jun 30 | Quiet, cheaper flying days |
| **Star / accent: the reunion** | Wed Jun 30 – Wed Jul 7 | Proposed core window on the Cape |
| **Red flag: July 4th** | Sun Jul 4 (holiday observed Mon Jul 5) | The main event |
| **Amber: avoid flying** | Thu Jul 1, Fri Jul 2 (in); Mon Jul 5 (out) | Peak fares and bridge traffic |
| **Blue: best to leave** | Tue Jul 6, Wed Jul 7 | Normal fares |

- Short caption under the calendar: *"Fly in Tue or Wed, fly out the
  following Tue or Wed, and skip the holiday rush."*
- Optional "Add to calendar" (.ics) button for the core dates.
- On phones, collapses to a two-week strip.

### 2. "Where we're coming from" graphic
A simple, illustrated map of the continental US (not a heavy interactive map).
- A **pin for each home city**: Bend, Portland, San Diego, Los Angeles,
  Atlanta, Columbus, New Jersey, upstate New York, Long Beach NY.
- **Gently curved dashed lines** from each pin to Sandwich (a star on the
  Cape). Lines for flyers end at their suggested airport (BOS or PVD).
  Drivers get solid "road" lines.
- Two line styles distinguish **flying** (West Coast, Atlanta, Columbus) from
  **driving** (NJ and NY).
- **Tapping or hovering a pin** opens a small card with that city's
  suggestions. Below the map, the same info appears as a simple list for
  accessibility and printing.

### 3. City cards: light-touch suggestions
Keep the tone friendly and suggestive ("you might…", "worth checking…"), not
prescriptive. Each card has a headline tip plus one or two extras:

| City | Suggested airport | Subtle suggestion |
|---|---|---|
| Bend, OR | BOS | "No nonstop from Redmond, so connect via Seattle, Denver or Salt Lake, or drive to Portland for the nonstop." |
| Portland, OR | BOS | "Alaska's nonstop red-eye gets you to Boston by breakfast." |
| San Diego, CA | BOS | "Look for a nonstop first. One-stops are plentiful." |
| Los Angeles, CA | BOS | "Lots of nonstops. Compare LAX with Burbank or Orange County." |
| **Atlanta, GA** | **BOS or PVD** | "**Check Providence too.** Delta flies there and fares can be lower, with an easier airport and about the same drive to Sandwich." |
| Columbus, OH | BOS (check PVD) | "Nonstops to Boston on Delta and American." |
| New Jersey | Drive | "About 5 hours. Leave early to beat bridge traffic." |
| Upstate NY | Drive | "4–6 hours. Plan to cross the Sagamore Bridge in the morning." |
| Long Beach, NY | Drive | "About 4.5 hours. Avoid Friday, July 2." |

### 4. "Boston or Providence?" callout
A small side-by-side box below the cards:
- **Boston Logan (BOS):** the most flights and usually the best fares. About
  60 miles and 1–1.5 hours to Sandwich.
- **Providence (PVD):** smaller and calmer, with a similar ~1.25-hour drive.
  **Worth checking when fares are cheaper, especially from Atlanta.**
- Tip: search both airports at once in Google Flights ("BOS, PVD").

### 5. Smaller supporting bits
- "When to book" tip: set price alerts now, aim to book by March–April 2027,
  and choose fares with free changes.
- Rental cars and carpools: who's landing when (pulls from RSVP arrival info
  later).
- Content source: [travel-research.md](travel-research.md). Routes and dates
  must be re-verified before launch.

## Tech approach (proposal)
- Static site (plain HTML/CSS, or a lightweight generator like Astro or
  Eleventy) in this repo
- Hosted free on **GitHub Pages**
- RSVP via an embedded form (e.g. Google Form) at first. Upgrade later if needed.

## Next steps
1. Confirm the exact reunion dates and venue/lodging
2. Confirm the Red Sox game date and time and decide on group tickets
3. Set Google Flights price alerts for each origin city (see travel research)
4. Decide the RSVP method
5. Build the site skeleton (Home, Calendar and Travel first, since that's what people need earliest)
6. Pick and save the house photos for the Accommodation carousel
7. Send a save-the-date with the site link

## Sources (Red Sox schedule)
- [MLB.com — Red Sox to open 2027 season March 25 in Seattle](https://www.mlb.com/news/red-sox-to-open-2027-season-march-25-in-seattle)
- [NBC Sports Boston — Red Sox 2027 schedule](https://www.nbcsportsboston.com/mlb/boston-red-sox/2027-schedule-opening-day-yankees-series/795708/)
- [TickPick — Red Sox vs. Orioles, Sat July 3, 2027](https://www.tickpick.com/buy-boston-red-sox-vs-baltimore-orioles-tickets-fenway-park-7-3-27-3am/8140167/)
- [Sportsbrackets — 2027 Red Sox schedule](https://sportsbrackets.net/2026/06/04/2027-boston-red-sox-schedule/)
