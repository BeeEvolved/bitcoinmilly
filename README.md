# BitcoinMilly.com
 **Live Price Tracker** – See Bitcoin’s real-time market price.
-  **Progress Bar** – Visual indicator of “how close to $1,000,000 per BTC.”
-  **Simple Price Chart** – Clean chart with:
  - Two smooth trend lines (spot general up vs. down moves).
-  **Volatility Gauge** – Shows how bumpy the price has been lately.
-  **RSI Hot/Cold Meter** – Quick read on momentum.
- **Timeline of All-Time Highs** – Key dates and milestones.
-  **Market Conditions Score (0–100)** – Rough snapshot of current vibes from trading activity and order book (not a prediction).
-  **Export to CSV** – Save your data for further analysis.
-  **Theme Switching** – Includes a fun alternative theme


> A tiny, fast, **no-build** dashboard that tracks Bitcoin’s live progress toward **$1,000,000**. Real-time price + simple TA + an experimental market-conditions index — all in a single HTML file.

![Bitcoin to 1 Milly preview](https://github.com/BeeEvolved/bitcoinmilly/blob/main/og-image.png)

---

## Features

- **Live BTC/USD price**
  - Coinbase REST **and** WebSocket ticker with graceful fallback, status labeling, and auto-reconnect.

- **% to $1,000,000**
  - Progress bars (with ARIA attributes) showing current progress to $1M.

- **Trend, Vol, RSI**
  - **Trend:** SMA(50) vs SMA(200) orientation (Golden/Death Cross).
  - **Vol:** 30-day realized volatility (log returns, annualized).
  - **RSI:** 14-period Wilder smoothing.

- **Price & Volume charts (no libs)**
  - Hand-rolled Canvas line chart with SMA overlays and responsive, DPI-aware rendering.
  - Volume bars beneath price.

- **ATH milestones**
  - Timeline of all-time highs from Coinbase BTC-USD. Cached for 24h.

- **$1M Market Conditions Index (experimental)**
  - Horizon scores (1D / 1W / 1M / 1Y) from:
    - order-book imbalance (near-mid),
    - recent buy/sell flow (5m),
    - volume EMAs (5/20),
    - ATR ratio (ATR14 / ATR50),
    - 30-bar trend t-statistic,
    - optional depth within +1% of mid.
  - Normalized → weighted → **0–100** score.
  - **Clearly labeled as a composite score — not a forecast or probability.**

- **CSV export**
  - One click to export `Timestamp, Close, SMA50, SMA200`.

- **Themes**
  - Light / Dark / **Brainrot 🧠⚡** (for the vibes).
This is a single static file app. **No build step. No API keys.**

