# XRP Oracle 4.0 — 15-minute Kalshi research dashboard

A mobile-friendly, single-file GitHub Pages website with live 1-minute XRP/USD candlesticks, EMA overlays, directional evidence scoring, manual Kalshi target comparison, UTC 15-minute countdown, and a simple contract value calculator.

## Deploy to GitHub Pages

1. Create a **new** public GitHub repository (for example `xrp-oracle-4`) to keep your Bitcoin predictor untouched.
2. Upload **index.html** to the repository root (not inside a ZIP or subfolder).
3. In **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
4. Wait for deployment, then open `https://YOUR-USERNAME.github.io/xrp-oracle-4/`.

No CSS or JS files are needed: everything is embedded in index.html.

## Data & limitations

- Uses Coinbase Exchange public XRP-USD 1-minute OHLCV endpoint; access can fail due to API/network/CORS/rate limiting. If the feed is unavailable, the signal stays WAIT. No fake prices are shown.
- Completed candles only. Updates every 30 seconds; the chart may lag the current spot tick.
- The 15-minute countdown is for UTC quarter-hour boundaries; verify your actual Kalshi contract's settlement window. Kalshi target must be entered manually, and Coinbase spot is **not** the Kalshi settlement oracle.
- Evidence scores are heuristic and are **not calibrated probabilities**. No profitability claims, trading orders, or direct Kalshi integration.
- The calculator ignores fees and slippage.
