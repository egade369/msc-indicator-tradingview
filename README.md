
<img width="1596" height="853" alt="image" src="https://github.com/user-attachments/assets/54e20253-2669-4e83-a015-31e5c1f76ab4" />


<img width="1594" height="819" alt="image" src="https://github.com/user-attachments/assets/76dbfc0f-d823-4129-9f04-e35cb5916f73" />



#  MSC Scalper &bull; XAUUSD
**Institutional-Grade Gold Scalping Engine & Real-Time Analytics for TradingView**

[![TradingView](https://img.shields.io/badge/TradingView-Pine_Script_v5-2962FF?style=flat&logo=tradingview&logoColor=white)](https://www.tradingview.com/)
[![Asset](https://img.shields.io/badge/Asset-XAUUSD%20%7C%20GOLD-F59E0B?style=flat)](https://www.tradingview.com/)
[![Timeframe](https://img.shields.io/badge/Timeframe-M1%20%2F%20M5-10B981?style=flat)](https://www.tradingview.com/)
[![License: MPL 2.0](https://img.shields.io/badge/License-MPL_2.0-8B5CF6?style=flat)](https://mozilla.org/MPL/2.0/)

</div>

---

###  Strategy Matrix

| Metric | Configuration | Specification |
| :--- | :---: | :--- |
| **Asset Pair** | `XAUUSD` | Gold Spot ($0.01 per point) |
| **Chart Timeframe** | `M1` / `M5` | High-frequency scalping |
| **Primary Target (TP1)** | `500 pts` | **+$5.00** base scalp target |
| **Runner Target (TP2)** | `1,000 pts` | **+$10.00** trend extension |
| **Add-on Layer (E2)** | `500 pts` | Recovery entry below E1 |
| **Stop Loss (SL)** | `1,000 pts` | **-$10.00** risk boundary |

---

###  Quick Setup

1. Open **TradingView** and select your `XAUUSD` chart.
2. Open the **Pine Editor** tab at the bottom toolbar.
3. Paste the contents of [`MSC_XAUUSD_Scalper.pine`](MSC_XAUUSD_Scalper.pine) and click **Add to chart**.

---

###  Automated Alerts

> [!TIP]
> Compatible with mobile push notifications and webhook execution bots.

* **Condition**: Select `MSC - XAUUSD Scalper`
* **Trigger**: Select `Any alert() function call`

---

### 📄 License

Distributed under the [Mozilla Public License 2.0](LICENSE). For research & educational purposes only.
