# Merger Arb Desk

One-page calculator for merger-arb ideas: deal spread and implied completion odds,
treasury-stock-method value per share, and option / call-spread P&L by scenario.
Everything runs in the browser; nothing connects to a broker and no data leaves the page.

## Deploy on Render (free static site)

1. Create a new GitHub repository (it can be private) and upload these three files:
   `index.html`, `render.yaml`, `README.md`.
2. In Render: **New → Blueprint**, connect GitHub, pick the repository, then **Apply**.
   Render reads `render.yaml` and creates the static site `merger-arb-desk`.
   (Or: **New → Static Site**, pick the repo, leave Build Command blank, Publish Directory `.`.)
3. Render gives you a URL like `https://merger-arb-desk.onrender.com`. Every push to the repo redeploys.

## Using it

- **Deal spread:** deal terms, break price and close date → spread, annualized return,
  implied completion probability, and sizing for a loss budget.
- **Valuation (TSM):** equity or enterprise value → value per share with fully diluted shares,
  plus a range table. Defaults are Modine's Q2 FY2027 / FY2026 10-K figures.
- **Options P&L:** enter a call chain (bid/ask by strike) or paste quotes, choose natural or mid fills,
  and see every call and call spread under talks-fail / no-news / deal-signed / higher-bid scenarios.
  Paste the `merger_MOD_*.csv` that `merger_arb.py` saves to load live TWS quotes.

Inputs are remembered in your browser (localStorage) only. Analysis only, not investment advice.
