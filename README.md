# 💎 VR_ALPHA: Real-Time AI Trading Intelligence Terminal

VR_ALPHA is a high-performance Python terminal designed for real-time market analysis and trade indication. Unlike standard backtesting scripts, VR_ALPHA connects directly to live exchange data to provide actionable signals based on current market volatility and trend momentum.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Financial-Data](https://img.shields.io/badge/Data-yfinance-yellow.svg)
![AI-Scan](https://img.shields.io/badge/Mode-Visual_AI-orange.svg)

## 🚀 Key Features
- **Live Data Stream:** Fetches high-granularity (1m interval) price data via Yahoo Finance API.
- **Smart Signal Logic:** Cross-verifies signals using 14-period RSI and 9-period Exponential Moving Averages (EMA).
- **Automated Risk Management:** Dynamic calculation of **Take Profit (TP)** and **Stop Loss (SL)** for every signal to maintain a professional Risk-to-Reward ratio.
- **Visual Pattern Scan:** Integrated image-processing module to overlay live data results on manual chart uploads.

## 🛠️ Tech Stack
- **Languages:** Python
- **APIs:** YFinance (Real-time Market Data)
- **Technical Analysis:** Pandas_TA (Quantitative Indicators)
- **Data Handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Pillow

## 📊 How the Intelligence Works
The engine uses a **Trend-Momentum** strategy to filter out market noise:
1. **Oversold Rebound:** Triggers a `STRONG BUY` only if RSI < 32 and the price is trending above the EMA 9.
2. **Overbought Rejection:** Triggers a `SELL SIGNAL` if RSI > 68 and the price drops below the EMA 9.
3. **Neutral Filter:** Automatically identifies sideways markets to prevent "over-trading" during risky periods.



## ⚙️ Installation & Usage
To run the terminal in Google Colab:

1. Install dependencies:
```bash
pip install yfinance pandas_ta

