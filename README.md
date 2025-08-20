
---

# 📊 Exploring Trading Strategies Based on Semiconductor Stocks and Bitcoin Correlation

## Overview

This project investigates the evolving relationship between **Bitcoin (BTC)**, **semiconductor stocks**, and major U.S. market indices (S\&P 500, NASDAQ) between **2014–2024**.
We explore how Bitcoin has transitioned from being perceived as a hedge against downturns to exhibiting **strong positive correlation with equity markets**, especially semiconductors.

The project introduces and tests two systematic **trading strategies**:

* **Momentum-Based Strategy** (using Bollinger Bands + ATR)
* **Mean Reversion Strategy** (using Bollinger Bands)

## 🔑 Key Findings

* Since **2019**, Bitcoin’s correlation with S\&P 500 and NASDAQ has exceeded **0.7**, indicating it no longer serves as a safe haven.
* Strong positive correlation between **Bitcoin and semiconductor equities**, except outliers like GlobalFoundries.
* **Weekend BTC moves significantly influence Monday U.S. equity openings**.
* **Momentum strategy outperforms** in volatile/down markets.
* **Mean reversion strategy underperforms** due to regime shifts and overfitting risks.

## 📂 Project Structure

```
.
├── data/                 # Yahoo Finance data (downloaded via yfinance)
├── notebooks/            # Jupyter notebooks for analysis
├── figures/              # Plots (correlation, cumulative returns, drawdowns, etc.)
├── strategies/           # Backtesting scripts for Momentum & Mean Reversion
├── paper/                # Research paper (PDF)
└── README.md             # Project documentation
```

## ⚙️ Methodology

* **Data Source**: Yahoo Finance (2014–2024)
* **Assets Analyzed**: Semiconductor tickers (NVDA, TSM, AMD, etc.), SPY, BTC-USD
* **Techniques Used**:

  * Correlation & cross-correlation analysis
  * Event study around Bitcoin halving events
  * Technical indicators: **Bollinger Bands (SMA ± 2σ)**, **ATR (14-day)**
  * Backtesting with Python

## 📈 Trading Strategies

### 1. Momentum-Based

* **Buy Signal**: BTC closes above upper Bollinger Band + ATR rising
* **Sell Signal**: BTC closes below lower Bollinger Band + ATR high
* ✅ Performs well in **down markets**, strong drawdown protection

### 2. Mean Reversion

* **Buy Signal**: Stock closes below lower Bollinger Band (oversold)
* **Sell Signal**: Stock closes above upper Bollinger Band (overbought)
* ❌ Struggles in **volatile, trending markets**

## 🛠️ Tech Stack

* **Python**: NumPy, Pandas, Matplotlib, Seaborn, Statsmodels, SciPy
* **Finance Libraries**: `yfinance`, `pandas_datareader`, `quantstats`



## 👨‍💻 Authors

* **Xuhao Weng** – Northeastern University
* **Nilkanth Patel** – Northeastern University
* **Sarath Chandra Vn Chinnala** – Northeastern University

---

👉 Would you like me to make this README **more research-focused** (academic style, highlighting findings/methodology), or **developer-focused** (emphasizing setup, reproducibility, and code execution)?
