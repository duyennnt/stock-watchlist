# Conviction Monitor — Stock Watchlist Dashboard

A single-file, self-contained dashboard for monitoring a personal stock watchlist,
grouped by conviction tier. Enter the current price for any name and it recomputes
P/E, upside to the analyst target, and the price's position within its 52-week range.
Your prices and notes are saved in the browser (localStorage) and persist between visits.

**Not investment advice.** All figures are research snapshots with an "as of" date on
each card and will drift — verify live before acting. P/E uses an approximate trailing
EPS and is directional only. Clinical-stage names have no earnings, so P/E shows "—".

## Use it locally
Open `index.html` in any browser. No build step, no dependencies (fonts load from Google Fonts).

## Publish it free with GitHub Pages
1. Create a new repository (e.g. `watchlist`) and upload `index.html` (and this README).
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick branch `main` and folder `/ (root)`, then **Save**.
5. Wait ~1 minute — your dashboard will be live at
   `https://<your-username>.github.io/<repo-name>/`

Because `index.html` is at the repo root, Pages serves it automatically.

## Files
- `index.html` — the dashboard (uses `localStorage`; correct for a hosted page)
- `README.md` — this file

## Updating the data
The watchlist lives in the `DATA` array near the top of the `<script>` block in
`index.html`. Each entry holds the ticker, tier, tags, default price, approximate EPS,
analyst target, 52-week low/high, next catalyst, key risk, and insider signal.
Edit that array to add names or refresh figures.
