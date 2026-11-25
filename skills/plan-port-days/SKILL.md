---
name: plan-port-days
description: "Plan days in port on a cruise: the hours ashore, docked or by tender, how busy the port is that day, the kinds of shore excursions that fit the call, and how many tours fit it. Use when someone asks what to do in a port, plans their port days for a sailing, or asks how many ships are in port."
---

# Plan port days

1. For a whole sailing, call `excursions_for_sailing` with the sailing id: each port day with its hours, whether passengers tender, and the tour kinds that fit. For one port, `find` it and call `port_excursions` (pass the date and ship when known, so the times fit that call).
2. `port_day` gives the ships in port that day and how crowded it is against a typical day. Mention it when it's busy.
3. For one kind of tour ("snorkeling in Cozumel"), call `excursion_activity` with the category slug the tool listed.
4. Excursions come as figures across tours (how many, typical length and price per person, average rating) and how many fit the call. For the tours themselves, link see_tours_url (our page for that call). Never name, price or link a single tour from memory.
5. Fit: tours that fit the call leave time to get back before all-aboard. When ashore is by tender, add that tenders take time at both ends.

Keep plans to what fits the hours ashore. Don't invent opening times, distances or transfer times beyond what the tools returned. Weather is monthly normals, not a forecast.
