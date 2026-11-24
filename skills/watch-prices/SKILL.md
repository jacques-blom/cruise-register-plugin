---
name: watch-prices
description: "Set up and manage cruise price alerts: watch a sailing's all-in price for a party and cabin, list watches, stop one. Use when someone says yes to a price watch, asks to be told when a price drops, wants to see or stop their alerts."
---

# Watch prices

1. Offer, once per conversation, after showing a sailing the traveller likes: "Want me to email you if this price drops?" Don't push it again if they say no.
2. On yes, call `watch_sailing` with the sailing id, their party and cabin, and `target_total_usd` only if they name a price.
3. If the result asks them to connect, the assistant shows a connect button: tell them to use it to sign in to Cruise Register (a link by email, or Google), then call `watch_sailing` again. Never ask for their email address in the chat.
4. Confirm what was set up, in one line: the sailing, party and cabin, today's price from the result, and the rule (an email when the all-in drops by 3% and at least $25, or reaches their target; at most one a day). Mention they can manage alerts at the `manage_url`.
5. "What am I watching?": `my_watches`. "Stop watching X": find its `watch_id` with `my_watches`, then `stop_watching`.

A watch is the traveller's request for those emails. It doesn't book, hold or pay for anything.
