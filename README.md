# Cruise Register

Cruise Register checks the cruise lines' own prices every day and adds the taxes, port fees and gratuities, so the price you see is what your party pays. This plugin connects your assistant to that data: find cruises, check whether a price is good, plan your port days, and get an email when a price you watch drops.

Travellers in Australia, New Zealand and the UK see the line's own price in A$, NZ$ or £ where we hold it.

## What you can ask

- "Find a 7-night Caribbean cruise from Miami in February for two, balcony."
- "What are the best deals from Port Canaveral right now?"
- "Is $2,400 for two a good price for Wonder of the Seas on 14 March?"
- "We're in Cozumel 8am to 5pm. What can we do?"
- "Watch that cruise and tell me if it drops."

## Install

- Claude Code: `/plugin install cruise-register --marketplace jacques-blom/cruise-register-plugin`
- Gemini CLI: `gemini extensions install https://github.com/jacques-blom/cruise-register-plugin`
- ChatGPT, Claude, Cursor, VS Code and others: https://www.cruiseregister.com/mcp

## Setup

Searching works straight away. To set up price alerts, connect your Cruise Register account when your assistant asks (a sign-in link by email, or Google).

## Use Cruise Register without installing the plugin

Add `https://mcp.cruiseregister.com` to your assistant as a custom MCP server (steps for each app: https://www.cruiseregister.com/mcp). To give your assistant the skills too, copy the folders in `skills/` into its skills.

Cruise Register doesn't sell cruises or take payments: booking links go to the booking site, and shore tours book on the tour operator's site. Some of these links earn us a commission; it doesn't change the price.

## Licence

The plugin's files (manifests, skills, this README and the icons) are MIT licensed: see LICENSE. Cruise Register's data, the MCP server's responses and cruiseregister.com are not covered and remain all rights reserved.

[Privacy](https://www.cruiseregister.com/privacy/) · [Terms](https://www.cruiseregister.com/terms/) · [Contact](https://www.cruiseregister.com/contact/)
