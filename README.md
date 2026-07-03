# Dukaan Dreams 🪔 — Khushi's Bazaar Empire

A single-file browser tycoon game, built to work like the real *Shopping Street* classic: customers walk in from the left with a real wallet of money, cross the street, and automatically enter any shop that isn't full — no clicking needed. Shop **placement order** is the actual strategy: cheap, fast shops early catch customers before pricier shops later drain what's left. Set across 6 India-themed bazaar levels (Mumbai, Delhi, Jaipur, Kolkata, Kochi, Goa), with real capacity/dwell-time/price economics per shop, street boosters (benches, newsstands, music ads, a bus stop) that change customer flow, daily revenue goals with a "Perfect Day" bonus, and festival events (Diwali, Holi, Wedding Season) that multiply prices on specific shops.

## How to play locally (VS Code)
1. Open this folder in VS Code.
2. Install the "Live Server" extension (or just double-click `index.html` to open it in your browser).
3. That's it — no build step, no npm install. It's pure HTML/CSS/JS.

## How to deploy free on GitHub Pages
1. Create a new GitHub repo, e.g. `dukaan-dreams`.
2. Push this folder's contents (`index.html`, `README.md`) to the repo's `main` branch.
3. Go to **Settings → Pages** in the repo.
4. Under "Build and deployment", set Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)`.
5. Save. GitHub will give you a live link like `https://<your-username>.github.io/dukaan-dreams/` within a minute or two.
6. Share that link with Khushi — she can play on any device, no install needed.

## Save data
Progress auto-saves to the browser's local storage on the device she plays on, every game tick. It's per-browser, so if she plays on her phone and your laptop, those are two separate save slots (this is normal for browser games without a backend/login).

## Where to extend it next
The whole game is data-driven at the top of the `<script>` tag:
- `SHOP_TYPES` — add new shop types or rebalance income/appeal/cost
- `CITIES` — add new bazaar levels, change reputation unlock thresholds, change which shops appear where
- `DECORATIONS` — add new decor items
- `FESTIVALS` — add new festival events and which shops they boost
- `ACHIEVEMENTS` — add new milestones

If you want this on Khushi's phone as a proper app later, the whole thing can be dropped into a React Native WebView, or rebuilt as an Expo screen reusing the same game logic — happy to help with that when you're ready.
