# OpenClaw — EV Calculator

**Expected Value & Kelly Criterion Calculator for Crypto Trading**  
Live Binance prices • Built by Bobby

## Overview
OpenClaw EV Calculator helps crypto traders instantly calculate:

- Expected Value (EV) of any trade
- Full Kelly & Quarter Kelly position sizing
- Optimal position size based on your capital
- Maximum profit and maximum loss

It supports leverage from 1x to 75x and pulls real-time prices from Binance via WebSocket.

## Features
- Live Binance price feed (BTC, ETH, SOL, and more)
- Input fields: Entry Price • Take Profit • Stop Loss • Win Rate • Capital
- Automatic EV and Kelly calculations
- Responsive UI (works perfectly on mobile and desktop)
- One-click reconnect for fresh prices

## Expected Value (EV) Formula
Expected Value tells you the **average profit or loss per trade** over the long run.

\[
EV = (p \times R) - (q \times L)
\]

- \( p \) = Win Rate (probability of winning)
- \( q \) = 1 - \( p \) (probability of losing)
- \( R \) = Reward (profit amount if the trade wins)
- \( L \) = Loss (loss amount if the trade loses)

**Positive EV (> 0)** = The trade is profitable in the long run  
**Negative EV (< 0)** = The trade will lose money over time

## Kelly Criterion Formula
The Kelly Criterion tells you the **optimal percentage of your capital** to risk on each trade for maximum long-term growth.

\[
f = \frac{p \cdot b - q}{b}
\]

- \( f \) = fraction of capital to use (e.g. 0.25 = 25%)
- \( p \) = Win Rate
- \( q \) = 1 - \( p \)
- \( b \) = Net odds = Reward / Risk = TP distance / SL distance

## How EV + Kelly Combine to Create a Trading Signal

The combination of **EV** and **Kelly** gives you a clear, math-based **signal** to enter a trade:

1. **First check EV**  
   - If EV > 0 → The trade has positive expectancy (worth taking)  
   - If EV ≤ 0 → Skip the trade (no edge)

2. **Then apply Kelly**  
   - If EV is positive, Kelly tells you **how much** capital to allocate  
   - Full Kelly = aggressive (maximum growth)  
   - Quarter Kelly = safe & recommended for most crypto traders

**Trading Signal Rule (simple version):**
- **GREEN SIGNAL** → EV > 0 **AND** Kelly % > 0 → Enter the trade with the suggested position size
- **RED SIGNAL** → EV ≤ 0 → Do NOT enter (no matter how good the setup looks)

This is why OpenClaw is powerful: it doesn’t just show numbers — it gives you a **mathematically proven entry signal** based on real edge and optimal sizing.

## How to Use
1. Visit: [https://thienx.github.io/ev-calculator/](https://thienx.github.io/ev-calculator/)
2. Enter your trade details
3. Click **Reconnect** to fetch latest prices
4. Check the **EV GAUGE** for EV value and Kelly position size

## Important Notice
⚠️ **This is NOT financial advice**  
This tool is for educational and reference purposes only. Crypto trading involves high risk of loss.

## Tech Stack
- HTML + CSS + JavaScript
- Binance WebSocket API
- Hosted on GitHub Pages

## Author
**Bobby** (OpenClaw)  
GitHub: [thienx](https://github.com/thienx)

---

Made with ❤️ for the trading community
