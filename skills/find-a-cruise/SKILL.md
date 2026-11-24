---
name: find-a-cruise
description: "Find cruises that fit: by departure port, destination, line, ship, dates, length, party and cabin, with the all-in price for the party, ratings and booking links; and this week's deals from a port. Use when someone wants cruise ideas, the cheapest sailing, deals from a port, a named ship's sailings, or the best ships or lines for them."
---

# Find a cruise

## Turn names into ids first

Call `find` for every port, ship, line or destination the traveller names. Pick the match whose country fits ("Sydney" is Sydney, Australia unless they say Nova Scotia). The other tools take these ids.

## Pick the tool

- A port, dates, length, line or ship: `search_sailings`. Pass `party` (2A two adults, 1A one adult, 2A2C a family of four) and `cabin` when they say; sort `price` for cheapest, `date` for soonest. Up to 10 rows: narrow rather than asking for more.
- "Deals from <port>", "what's on sale": `find_deals`. Lead with the picks and say why each was picked (its `why` and `evidence`).
- One sailing in detail: `get_sailing` (itinerary by day, prices per cabin).
- A ship or a line: `get_ship`, `get_line`. "Best ship for families", "best food": `rank_ships` with `traveller` or `topic`.

## Prices

- Quote only prices a tool returned, with who they're for and what they include ("$1,290 for two adults, inside cabin, including taxes, fees and gratuities"). Never add up, estimate or convert a price.
- A `fare_only` price may be low: say the taxes or fees weren't confirmed.
- Australia, New Zealand, UK: when `local_price.leads` is true (or `find_deals` returns `local_lead`), quote that all-in in A$, NZ$ or £ first, then the US$ total. A local `line_fare` that isn't all-in is the line's own fare: say what it includes, and never call it all-in. Write US$ for US dollar amounts for these travellers.
- Give ratings with their review count ("4.4 out of 5 from 812 passenger reviews"). When a rating is null, give its reason.

## Links

Link each sailing's `url` for details. To book, give `book_url`: it's our link and forwards to the booking site. Never name or guess a booking site. When a result has a `disclosure` line, add it beside its booking links as written.

## After a result

When the traveller likes a sailing, offer once to watch its price (watch-prices).
