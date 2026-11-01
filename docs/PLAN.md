# Baker Family Reunion 2027 — Website Plan

## Goal
A simple, mobile-friendly site that gives every branch of the family one
place for dates, travel, lodging, the schedule and RSVPs.

## Key facts
- **Location:** Sandwich, MA (Cape Cod)
- **Dates:** July 4th week 2027. Proposed core window **Wed Jun 30 – Wed Jul 7**
  (see [travel-research.md](travel-research.md))
- **Coming from:** Bend OR, Portland OR, San Diego CA, Los Angeles CA,
  Atlanta GA, Columbus OH (flying), plus New Jersey, upstate NY and
  Long Beach NY (driving)

## Proposed pages
1. **Home:** dates, location, countdown, headline announcements
2. **Travel** (its own tab off Home; see detailed spec below): calendar,
   "where we're coming from" map, BOS vs PVD, city-by-city tips, driving and bridge-traffic tips,
   rental cars and carpools
3. **Lodging:** the main house or rentals, nearby hotels and campgrounds,
   who's staying where
4. **Schedule:** day-by-day events (July 4th fireworks, beach day, family
   dinner, photo)
5. **RSVP:** who's coming, arrival and departure dates and flights (feeds
   airport-pickup coordination)
6. **Family:** family tree and photo sharing
7. **FAQ:** what to pack, beaches, kids' activities, contact info

## Travel tab: detailed spec (not built yet)

The Travel tab is linked from the main navigation on the Home page. It has
three sections, top to bottom.

### 1. Calendar of proposed dates
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
2. Set Google Flights price alerts for each origin city (see travel research)
3. Decide the RSVP method
4. Build the site skeleton and Travel page first, since that's what people need earliest
5. Send a save-the-date with the site link
