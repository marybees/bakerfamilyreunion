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
   "who's coming & when" shared travel plans,
   "where we're coming from" map, BOS vs PVD, city-by-city tips, driving and bridge-traffic tips,
   rental cars, carpools and golf cart rentals
4. **Accommodation** (its own tab; see spec below): our house's Airbnb
   listing now. Cape Cod rental house suggestions come in early 2027
5. **Itinerary** (replaces "Schedule"; see spec below): a rough
   day-by-day plan (lawn games, Red Sox, July 4th) plus **sign-ups to host
   game night and dinner each night**. Sign-ups update the calendar
   automatically
6. **Things to Do** (its own tab; see spec below): **Restaurants** and
   **Activities** sections for Sandwich and the Upper Cape
7. **RSVP:** who's coming and how many. Flight, arrival and lodging
   details are shared on the Travel tab's "Who's coming & when" form, so
   nobody enters them twice
8. **Family:** family tree and photo sharing
9. **FAQ:** what to pack, beaches, kids' activities, contact info

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
- Navigation tabs: Home · Calendar · Travel · Accommodation · Itinerary · Things to Do · RSVP ·
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
| **Travel** | Best arrival days, avoid-flying days, best departure days, holiday, **plus everyone's shared arrivals and departures** | Greens, ambers and blues (as in the Travel spec). **Pink ✈️ arrival** and **gray 👋 departure** chips |
| **Activities** | Red Sox game, July 4th, lawn games, dinners, game nights, group photo | **Red** Red Sox, **teal** lawn games, **orange** dinners, **purple** game nights |
| **Everything** | Travel, arrivals/departures and activities together: the **master itinerary** | All colors, with a combined legend |

**Behavior**
- Tabs are a simple segmented toggle: `Travel | Activities | Everything`.
  The default view is **Everything**.
- Each day cell shows small color-coded chips (e.g. "⚾ Red Sox @ Fenway",
  "🎆 July 4th"). Tapping a chip opens details: time, place, drive time and
  links.
- The legend below the calendar updates to match the selected tab.
- On phones, the month grid becomes a day-by-day list with the same colors.
- The Travel tab page embeds the **Travel** view, and the Itinerary page links
  to the **Activities** view, so there's one calendar and no duplicates to
  keep in sync.
- Colors need enough contrast, and every chip has an icon and label, so
  meaning doesn't rely on color alone.
- Optional: an "Add to my calendar" (.ics) link per event.

**Arrivals & departures (master itinerary)**
- Every shared travel plan (see Travel tab §6) shows on its day:
  - ✈️ **Arrival chip**, e.g. "✈️ Portland Bakers land BOS 7:05am"
  - 👋 **Departure chip**, e.g. "👋 Atlanta Bakers fly home from PVD"
  - 🚗 **Drivers too**, e.g. "🚗 NJ Bakers arrive ~3pm"
- If a day has many arrivals, collapse them into one chip ("✈️ 6 families
  arriving") that expands on tap.
- **Headcount per day:** a small "👨‍👩‍👧 23 on the Cape" counter on each day,
  calculated from arrival and departure dates. It shows when the house is
  fullest and helps dinner hosts plan portions.
- Optional filter: "Show only my family's arrival."

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

## Itinerary tab: spec (not built yet)

The Bakers love games and sports, so the itinerary is built around three
recurring pieces: **daytime lawn games**, a **family dinner every night**, and
a **game night every night**. Families sign up to host the dinners and game
nights, and those sign-ups show up on the Calendar automatically.

### 1. Rough day-by-day itinerary
Nights covered: **Wed Jun 30 through Tue Jul 6 (7 nights)**. Wed Jul 7 is
departure day. Everything is "rough" and easy to change.

| Day | Daytime | Dinner | Game night |
|---|---|---|---|
| Wed Jun 30 | Arrivals. Settle in. Casual lawn games | Welcome dinner *(sign up)* | Game night *(sign up)* |
| Thu Jul 1 | Arrivals continue. Beach or **volleyball** | *(sign up)* | *(sign up)* |
| Fri Jul 2 | **Lawn games tournament day**: croquet, bocce, badminton | *(sign up)* | *(sign up)* |
| Sat Jul 3 | Beach / free day *(possible Red Sox game)* | *(sign up)* | *(sign up)* |
| Sun Jul 4 | **July 4th**: parade or local events, cookout, fireworks *(possible Red Sox game)* | July 4th cookout *(sign up to help)* | Game night after fireworks *(sign up)* |
| Mon Jul 5 | Family photo. Volleyball and badminton rematches | *(sign up)* | *(sign up)* |
| Tue Jul 6 | Free day. Championship finals and awards | Farewell dinner *(sign up)* | Final game night *(sign up)* |
| Wed Jul 7 | Departures | | |

### 2. Lawn games & sports
The yard has **volleyball, badminton, croquet and bocce ball**.
- A small card for each game with an icon, where it's set up and "bring
  your A-game" flavor text.
- Optional **Baker Games tournament**: sign up teams or players, keep a
  simple bracket and scoreboard on the site, and hand out a trophy or
  bragging-rights award at the farewell dinner.
- Lawn games appear on the Calendar's **Activities** view.

### 3. Sign-ups: Game Night host & Dinner
One sign-up board per night, each with **two slots**:

**🎲 Game Night host** (one per night). Saved to the sheet's **Game Night
Host Signup** tab
- Fields (match the sheet's columns): **Date**, **Game** (e.g. "Codenames +
  Spades"), **Hosted by** (name or family)
- Each night should have a game night, so unclaimed nights show a friendly
  "**Needs a host!**" badge

**🍽️ Dinner** (one per night). Saved to the sheet's **Dinner Host Signup**
tab
- Fields (match the sheet's columns): **Date**, **Cuisine** (e.g. "lobster
  rolls" or "taco bar"), **Provided by** (name or family)
- **Dietary requests** (later, optional): would need a new column or tab in
  the sheet (e.g. a "Dietary Requests" tab with Name and Request columns)
  so cooks can see vegetarian, gluten-free, allergy and kids' notes
- Unclaimed nights show "**Dinner needed!**"

**How it works for the family**
- Each night is a card: **date → Dinner: [claimed by X / Sign up] → Game
  Night: [claimed by Y / Sign up]**
- Click **Sign up** → a short form → done. No login needed.
- A small "Change or cancel" option (e.g. edit with the name you used, or a
  note to text the organizer)
- Shows progress at the top: "**5 of 7 dinners covered · 4 of 7 game nights
  hosted**"

### 4. Sign-ups update the calendar automatically
- Every claimed slot becomes a calendar event in the Calendar page's
  **Activities** and **Everything** views, e.g.
  "🍽️ Dinner: Taco bar (Portland Bakers)" and "🎲 Game Night: Codenames
  (Atlanta Bakers)".
- Unclaimed slots appear on the calendar as faded "open" chips that link
  straight to the sign-up form.
- New colors for the Activities view: **orange for dinners** and **purple
  for game nights** (red stays for the Red Sox, teal for lawn games).
- There's one source of truth, the sign-up data. The Itinerary board and
  the Calendar both read from it, so they never get out of sync.

## Things to Do tab: spec (not built yet)

A guide to Sandwich and nearby for downtime between lawn games and dinners.
It has two sections, toggled like the Calendar: `Restaurants | Activities`.

**Starting point: our Airbnb listing.** Pull in the recommendations from the
listing's description and guidebook (https://www.airbnb.com/h/twentyroos),
then add family favorites. *(Claude couldn't reach Airbnb from this session.
Copy and paste the guidebook text or screenshots to bring them in.)*

**Card layout (both sections)**
- Photo, name, short "why we love it" line, town and **drive time from the
  house**
- Tags: 👨‍👩‍👧 kid-friendly · 🌧️ rainy-day · 💲–💲💲💲 · 🐕 dog-friendly ·
  🚲 bikeable
- Buttons: **Website** and **Map** (opens Google/Apple Maps)
- ⭐ **"Baker family favorite"** badge for places the family already loves
- Optional mini-map showing every pin around the house
- Optional "👍 I want to go!" button per card (stored in the Google Sheet) to
  spot group outings. Popular picks can become Calendar events

### Restaurants
Grouped so people can find what they need fast:

| Group | Starter ideas (verify hours and details before launch) |
|---|---|
| **Seafood & lobster** | **Fishermen's View** (Sandwich marina, canal views, deck, fish market) · **Seafood Sam's** (casual, kid-friendly, budget lobster dinners) · **Captain Scott's Seafood** (beachy, covered outdoor seating) |
| **Lobster to cook at the house** | **Superior Lobster & Seafood** (market with live lobsters and fresh fish). Great for a dinner sign-up night |
| **Breakfast & coffee** | *(add from the Airbnb guidebook and family favorites)* |
| **Ice cream & treats** | *(add family favorites)* |
| **Big-group friendly** | Flag places that take reservations for 15+ or have large outdoor tables. Call ahead for July 4th week |
| **Takeout / pizza** | Good for arrival nights or when nobody's signed up for dinner |

- Tip on the page: **July 4th week is the busiest week of the year. Reserve
  ahead for big groups.**

### Activities
Grouped by type:

| Group | Starter ideas |
|---|---|
| **Beaches** | **Town Neck Beach** (via the Sandwich Boardwalk; check boardwalk status) · **Scusset Beach** (gentle surf, canal views, good for families) · Sagamore Beach |
| **Outdoors & biking** | **Cape Cod Canal bike path** (~7 miles each side, flat and paved) · Canal Visitor Center (watch ships and tugs) · Scusset Beach trails · Green Briar Nature Center (East Sandwich) |
| **Family & kids** | **Heritage Museums & Gardens** (100 acres of gardens, antique cars, vintage carousel, Adventure Park ropes course) · Sandwich Fish Hatchery |
| **History & culture** | **Sandwich Glass Museum** (live glassblowing demos) · Hoxie House & Dexter Grist Mill (historic Sandwich village) |
| **Sports** | **Cape Cod Baseball League** game (free, summer college league) · Red Sox at Fenway (see Calendar) · nearby golf courses |
| **Rainy day** | Glass Museum, Heritage Museums, movie theater, board games at the house |
| **Day trips** | Boston, Provincetown, Martha's Vineyard or Nantucket ferry (book ahead) |

- July 4th specials get their own highlight box: local parades, fireworks
  and town events (to research closer to the date)

**Content source & upkeep**
- Start with the Airbnb guidebook plus the lists above, then let family
  suggest additions through a "Suggest a place" form (adds to a **Things
  to Do** tab in the Google Sheet for the organizer to approve).
- Re-check hours, closures (e.g. the boardwalk) and reservation policies in
  spring 2027.

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

### 5. Golf cart rentals
A friendly section for renting golf carts to get around the property during
the reunion.

**Recommended company: CCE Golf Carts (now C2 Vehicles)**
- We rented from **Country Club Enterprises (CCE)** in 2021. CCE now
  operates as **C2 Vehicles**, at the same address.
- **Website:** https://c2vehicles.com (golf cart page:
  https://c2vehicles.com/pages/cape-cod-golf-carts, online booking:
  https://book.c2vehicles.com)
- **Location:** 2D Express Drive, Wareham, MA 02571 (next to Buzzards Bay)
- **Phone:** (508) 273-9939 · weekdays 8–5, Saturdays by appointment
- They **deliver to and pick up from the house**.
- Card on the site shows the logo or name, "Family favorite — we used them
  in 2021", a **"Visit C2 Vehicles"** button, and the phone number.

**What we paid in 2021 (starting point for budgeting)**

| Item | 2021 price |
|---|---|
| Gas Club Car **6-passenger** w/ windshield, canopy & headlights | **$315 per cart** for a 5-day rental (Thu–Tue), + 6.25% MA tax |
| Delivery + pickup to East Sandwich | **$160** (flat, round trip) |
| **Total for 2 carts** | **$829.38** |

**Rough 2027 estimate** (assumes about 15–30% price increases since 2021 and
a slightly longer rental for the full week; get a real quote):
- About **$375–475 per 6-seat cart** for the week, plus tax
- About **$185–225** delivery and pickup
- **2 carts ≈ $1,000–1,250 total**, which works out to roughly $110–140 per
  household if split among the 9 home cities
- On the site, show this as "**Estimated ~$400/cart for the week — split
  among families**" with a note that prices are estimates until quoted.

**Important rules from the rental agreement (show as a short "Know before
you ride" box)**
- 🚫 **Carts stay on the property.** They are **not street-legal**, and the
  agreement prohibits driving them on public roads. They're not for trips to
  the beach or into town.
- 🪪 **Every driver needs a valid driver's license.**
- 👥 **Max 2 people per bench seat** (6 per cart). No standing on the back.
- 🔑 Remove keys after each use and store carts safely overnight.
- 🧼 Return carts clean. The renter pays for any damage.
- If C2 now rents **street-legal LSVs** (they sell them), ask about that
  option for beach and village trips. Rules vary by town and are limited to
  roads posted at 30 mph or less.

**Booking plan**
- One person places a **group order**, likely 2 carts as in 2021, adjusted
  for headcount.
- Call or book by **early spring 2027**. July 4th week is peak season, and
  delivery slots fill up.
- Optional "Chip in for golf carts" line or checkbox on the RSVP form to
  gauge interest and split costs.
- Privacy: don't put personal details from the old rental agreement (names,
  address, phone, email) on the website or in the repo.

### 6. "Who's coming & when": share your travel plans
A fun, excitement-building section where each family shares how and when
they're getting there.

**Share form** (short, no login)
- Name or family (e.g. "The Portland Bakers") and how many people
- Coming from (pick from the home cities)
- **Getting there:** ✈️ Flying / 🚗 Driving
- **Arrival:** date, time, airport (BOS / PVD / other), airline + flight
  number (optional)
- **Departure:** date, time, airport, airline + flight number (optional)
- **Where we're staying** (optional): "At the house", or the name or town of
  a rental (e.g. "Airbnb in Sandwich village")
- Fun optional extras: "Most excited for…" (e.g. "croquet revenge!") and a
  photo or emoji
- Checkboxes: "Need a ride from the airport", "Have room in my rental car
  for N"
- Families can update their entry later (same edit approach as the
  dinner/game night sign-ups)

**How it's shown**
- **Arrivals board**, styled like an airport departures/arrivals screen
  (a fun flip-board look): family · from · airline/flight · lands · airport.
  Sorted by arrival time, with a "✅ Landed!" status the week of.
- **"Where everyone's staying"** list: families grouped by the house or the
  town of their rental, so people can see who's nearby.
- On the "Where we're coming from" map (§2), each pin gets a little badge
  once that family shares plans: "✈️ booked! Arriving Wed 6/30".
- **Progress line:** "**7 of 9 families have shared travel plans**"
- **Airport buddies:** automatically highlights families landing at the same
  airport within about 2 hours of each other: "You and the Columbus Bakers
  both land at BOS Wed afternoon — share a rental car?"
- All of this feeds the **Calendar's arrivals and departures** (see Calendar
  spec), which makes the **master itinerary**.

**Privacy**
- Shows family names, cities, dates/times, airports and flight numbers
  only. No phone numbers, emails or home addresses.
- Rental addresses are **not** shown, just the town or "near the house".
  Exact addresses go to the organizer only.

### 7. Smaller supporting bits
- "When to book" tip: set price alerts now, aim to book by March–April 2027,
  and choose fares with free changes.
- Rental cars and carpools: powered by the shared travel plans (§6), with
  airport pickups and "airport buddies".
- Content source: [travel-research.md](travel-research.md). Routes and dates
  must be re-verified before launch.

## Tech approach (proposal)
- Static site (plain HTML/CSS, or a lightweight generator like Astro or
  Eleventy) in this repo
- Hosted free on **GitHub Pages**
- RSVP via an embedded form (e.g. Google Form) at first. Upgrade later if needed.
- **Sign-ups are stored in the family Google Sheet** (decided):
  https://docs.google.com/spreadsheets/d/1-NZnvlRHNE7zUl2nkmGNHLoTnw7PlUIWrsRG9bzwx3Y/edit

  | Sheet tab | Columns |
  |---|---|
  | **Game Night Host Signup** | Date · Game · Hosted by |
  | **Dinner Host Signup** | Date · Cuisine · Provided by |
  | **Travel Plans** *(new tab to add)* | Family · People · From · Mode (Fly/Drive) · Arrival Date · Arrival Time · Arrival Airport · Arrival Flight · Departure Date · Departure Time · Departure Airport · Departure Flight · Staying At · Excited For · Needs Ride · Seats to Share |

  - **Two-way sync:** the website both **reads from** and **writes to** the
    sheet. Signing up on the site adds a row to the sheet, and typing in the
    sheet shows up on the site.
  - **Writing:** a small **Google Apps Script** attached to the sheet,
    deployed as a web app. The site's sign-up form sends Date + Game + Hosted
    by (or Date + Cuisine + Provided by), and the script adds a row to the
    right tab. It rejects a second sign-up for a date that's already taken.
  - **Reading:** the same script returns both tabs as JSON, and the
    Itinerary board and Calendar build themselves from it. One source of
    truth.
  - **Editing:** the organizer can fix or remove sign-ups directly in the
    sheet, and the site picks up the change on the next page load.
  - **Date format:** use one consistent format in the Date column (e.g.
    `2027-06-30`), or format the column as a date, so the site matches rows
    to calendar days reliably.
  - **Security:** never put the sheet's edit link on the public site. The
    sheet's own sharing can stay private, since the script runs as the
    sheet owner.
  - Upgrade path: a hosted database (e.g. Firebase or Supabase) only if we
    later want logins, instant updates or tournament scoring.
- Keep it light on privacy: first names or family names only, no phone
  numbers or emails shown publicly.

## Next steps
1. Confirm the exact reunion dates and venue/lodging
2. Confirm the Red Sox game date and time and decide on group tickets
3. Set Google Flights price alerts for each origin city (see travel research)
4. Decide the RSVP method
5. ~~Decide how sign-ups are stored~~ Done: family Google Sheet (two tabs)
6. Add a **Travel Plans** tab to the Google Sheet with the columns listed
   under Tech approach
7. Rough out the daily itinerary and confirm which games and nights to include
8. Build the site skeleton (Home, Calendar and Travel first, since that's what people need earliest)
9. Send the Airbnb guidebook recommendations (copy/paste or screenshots) for the Things to Do tab
10. Pick and save the house photos for the Accommodation carousel
11. Get a 2027 golf cart quote from C2 Vehicles (formerly CCE) and book by early spring
12. Send a save-the-date with the site link

## Sources (things to do)
- [Wanderlog — Sandwich family restaurants](https://wanderlog.com/list/geoCategory/555800/)
- [Superpages — Seafood restaurants in Sandwich](https://www.superpages.com/sandwich-ma/steak-seafood-restaurants)
- [Superpages — Seafood restaurants in East Sandwich](https://www.superpages.com/east-sandwich-ma/steak-seafood-restaurants)
- [TravelAwaits — Sandwich, MA things to do](https://www.travelawaits.com/2682865/sandwich-ma-things-to-do/)
- [The Crazy Tourist — 15 best things to do in Sandwich](https://www.thecrazytourist.com/15-best-things-to-do-in-sandwich-ma/)
- [Wikivoyage — Sandwich (Massachusetts)](https://en.wikivoyage.org/wiki/Sandwich_(Massachusetts))
- [Dan'l Webster Inn — Sandwich & Cape Cod activities](https://danlwebsterinn.com/attractions/)
- [We Need a Vacation — Things to do in Sandwich](https://www.weneedavacation.com/blog/things-to-do-in-sandwich/)

## Sources (golf carts)
- 2021 CCE rental agreement (family records, not published)
- [C2 Vehicles — About us (formerly Country Club Enterprises)](https://c2vehicles.com/pages/about-us)
- [C2 Vehicles — Contact](https://c2vehicles.com/pages/contact)
- [C2 Vehicles — Online booking](https://book.c2vehicles.com/)
- [C2 Vehicles — Cape Cod golf carts](https://c2vehicles.com/pages/cape-cod-golf-carts)
- [C2 Vehicles — Street-legal golf cart laws in New England](https://c2vehicles.com/blogs/news/street-legal-golf-cart-laws-new-england)

## Sources (Red Sox schedule)
- [MLB.com — Red Sox to open 2027 season March 25 in Seattle](https://www.mlb.com/news/red-sox-to-open-2027-season-march-25-in-seattle)
- [NBC Sports Boston — Red Sox 2027 schedule](https://www.nbcsportsboston.com/mlb/boston-red-sox/2027-schedule-opening-day-yankees-series/795708/)
- [TickPick — Red Sox vs. Orioles, Sat July 3, 2027](https://www.tickpick.com/buy-boston-red-sox-vs-baltimore-orioles-tickets-fenway-park-7-3-27-3am/8140167/)
- [Sportsbrackets — 2027 Red Sox schedule](https://sportsbrackets.net/2026/06/04/2027-boston-red-sox-schedule/)
