#  MSC Scalper - XAUUSD Scalping Suite

[![TradingView Pine Script](https://img.shields.io/badge/Pine%20Script-v5-blue?logo=tradingview&logoColor=white)](https://www.tradingview.com/)
[![Asset](https://img.shields.io/badge/Asset-XAUUSD%20%28Gold%29-gold)](https://www.tradingview.com/symbols/XAUUSD/)
[![Timeframe](https://img.shields.io/badge/Timeframe-M1%20%2F%20M5-orange)](https://www.tradingview.com/)
[![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)](https://mozilla.org/MPL/2.0/)

**MSC Scalper** is an institutional-grade, high-frequency scalping indicator and backtesting suite built in **Pine Script v5** for TradingView, optimized specifically for **Gold (XAUUSD)**. 

It combines dynamic Support & Resistance Flip Zones, dual-entry recovery risk management (E1 + E2), ATR volatility filters, predictive ghost lines, and an institutional dashboard matrix.

---

##  Key Features

* **Dynamic SnR & Role Reversal (Flip Zones)**: Automatically detects swing highs/lows using lookback pivots. Broken support levels dynamically flip into resistance (and vice versa) upon confirmed breakout.
* **Dual Execution Modes**:
  * `Confirmed Bounce`: Waits for candle close confirmation and enters at the close price to eliminate repainting.
  * `Instant Touch`: Enters immediately when the price touches the SnR boundary (ideal for limit orders).
* **Smart Basket Recovery (E1 + E2)**:
  * **E1**: Primary entry at key boundary level.
  * **E2 (Add-on)**: Placed at adverse excursion (default: 500 pts / $5.00).
  * **Recovery Exit**: If E2 triggers, closes the entire basket at E1 price (E1 breakeven, E2 in profit).
* **Multi-Target Scaling**:
  * **TP1**: Primary scalping target (default: 500 pts / $5.00).
  * **TP2 Runner**: Optional partial close (50% at TP1, moves SL to Breakeven for remaining 50% targeting TP2).
* **Institutional Risk & Volatility Radar**:
  * Trend Filter: Blocks counter-trend trades when price deviates steeply from EMA 50 by $N \times \text{ATR}$.
  * News / Spike Detector: Highlights high-volatility bars in red and warns of extreme market conditions.
  * Market Session Tracking: Displays active market session (Tokyo / London / New York).
* **Projected Ghost Radar**: Projects upcoming potential buy/sell setup levels ahead of the live bar.
* **Built-in Backtest Dashboard**:
  * Multiple display formats: `Vertical Today`, `Pro Summary`, `Full Matrix`, `Weekly Detail`, `Daily Detail`.
  * Computes Win Rate, Net Points, Profit Factor, Expectancy, and Max Drawdown with spread & slippage deduction.
* **Webhook & Alert Ready**: Compatible with automated bots via TradingView dynamic alert calls.

---

##  Default Parameters (XAUUSD)

| Parameter | Default Value | Description |
| :--- | :---: | :--- |
| **Asset Mode** | `XAUUSD (Gold)` | Primary asset configuration preset |
| **Point Size** | `0.01` | 1 point = $0.01 on Gold ($1.00 = 100 points) |
| **TP1 Base** | `500.0 pts` | $5.00 primary scalp profit target |
| **TP2 Base** | `1000.0 pts` | $10.00 extended runner target |
| **Entry 2 Distance** | `500.0 pts` | Distance from E1 to trigger recovery leg E2 ($5.00) |
| **SL Base** | `1000.0 pts` | $10.00 stop loss buffer |
| **Min SnR Distance** | `200 pts` | Minimum distance between horizontal levels ($2.00) |
| **Min Wick Ratio** | `0.35` | 35% candle rejection wick required for bounce validation |
| **Spread + Slippage** | `25.0 pts` | Realistic friction cost ($0.25) deducted per order |
| **Reset Hour** | `5` | Daily rollover hour (05:00 AM Bangkok Time / UTC+7) |

---

##  Installation & Setup

1. **Open TradingView**: Navigate to your chart on [TradingView](https://www.tradingview.com/).
2. **Open Pine Editor**: Click on the **Pine Editor** tab at the bottom of the screen.
3. **Paste the Code**:
   * Open `MSC_XAUUSD_Scalper.pine` or copy the source code.
   * Clear any default code in the editor and paste the full script.
4. **Save & Add to Chart**:
   * Click **Save** (e.g., name it `MSC - XAUUSD Scalper`).
   * Click **Add to chart**.
5. **Select Chart**:
   * Recommended symbol: `XAUUSD` or `GOLD`
   * Recommended timeframe: **1m (M1)** or **5m (M5)**

---

##  Setting Up TradingView Alerts

To receive real-time notifications on mobile or connect to webhook automation bots:

1. Click the **Alert** icon (clock with plus) on TradingView.
2. Under **Condition**, select **`MSC - XAUUSD Scalper`**.
3. Select **`Any alert() function call`**.
4. Set **Expiration** to *Open-ended* (if available on your plan).
5. Choose your notification preferences (Webhook URL, App Push, Email, SMS).
6. Click **Create**.

---

##  Dashboard Views

The indicator features 5 configurable dashboard views under indicator settings (`View Format`):

* **Vertical Today**: Minimalist compact HUD showing today's trades, TP1 hits, SL, Win Rate, and Net Points.
* **Pro Summary**: Comprehensive performance overview including Yesterday, Weekly totals, Profit Factor, Expectancy, and active market session radar.
* **Full Matrix**: Calendar grid showing daily and weekly performance breakdown across the entire month.
* **Weekly Detail**: Day-by-day (Mon–Fri) performance breakdown for the current week.
* **Daily Detail**: Comparative side-by-side metrics comparing Today vs. Week vs. Month.

---

##  Risk Disclaimer

This trading script is provided for educational and research purposes only. Past performance does not guarantee future results. Gold scalping involves significant financial risk. Always thoroughly backtest and forward-test on demo accounts before deploying capital.

---

##  License

This source code is licensed under the [Mozilla Public License 2.0 (MPL-2.0)](https://mozilla.org/MPL/2.0/).
Copyright (c) MSC Scalper - Gold Scalping Suite.
