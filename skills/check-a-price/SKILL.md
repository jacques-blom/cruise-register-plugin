---
name: check-a-price
description: "Judge whether a cruise price is good, using what Cruise Register measured: the same sailing's other cabins and parties, the same ship's other dates, the port's deals and their evidence (price drops, below the usual price). Use when someone asks 'is this a good price', 'should I book now or wait', or pastes a quote."
---

# Check a price

Cruise Register doesn't give a verdict of its own; build one only from measured numbers, and say which numbers.

1. Identify the sailing: `find` the ship, then `get_sailing` with the sailing id (ship|date|nights) and the traveller's party. If they pasted a price from elsewhere, compare it with our all-in for the same party and cabin, and say what each includes. A quote without taxes, fees or gratuities isn't comparable until those are added; say so rather than adding them yourself.
2. Compare with the same ship's other dates: `search_sailings` with `ship` and a window of a month or two either side, same party and cabin, sorted by price. Say where this sailing sits ("the third cheapest of 8 sailings in March").
3. Check `find_deals` for its departure port: if this sailing is a pick, give its `why` and `evidence` (for example "down $200 since 1 Nov", or the line's earlier price).
4. Answer in one line first ("Fair, not a deal: two March dates on the same ship are $300 less"), then the numbers behind it.

Never predict prices. To protect against a drop after they decide, offer a price watch (watch-prices). If they've already booked, a watch still tells them when the price falls, which some lines honour with a re-price: say to check their line's own rules.
