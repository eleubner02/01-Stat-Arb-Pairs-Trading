# 01-Stat-Arb-Pairs-Trading  
Statistical Arbitrage: Cointegration‑Based Pairs Trading

---

## Results Overview

**In‑Sample (2020–22):**  
- Sharpe: 1.51 | Annualized Return: 2.08% | Trades: 14  

**Out‑of‑Sample (2023–24):**  
- Sharpe: 1.09 | Annualized Return: 2.17% | Trades: 12  

**Full Sample (2020–24):**  
- Sharpe: 1.54 | Annualized Return: 2.49% | Max Drawdown: –1.32% | Trades: 30  

---

## Project Summary
* **Pair Selection:** LUV–AAL (Southwest & American Airlines)  
* **Methodology:** OLS hedge ratio on log prices; spread z‑score with rolling window (60), ENTRY=2.0 / EXIT=0.5 thresholds; 16‑day time‑stop  
* **Stationarity:** ADF on residuals, p=0.027 (reject unit root)  
* **Costs:** 2 bps/leg transaction costs imposed on all position changes  
* **Sizing:** Dollar‑neutral ($10k leg, beta‑adjusted)  

Key Takeaway:  
Strategy shows strong mean reversion in‑sample, with weaker but **persistent out‑of‑sample performance**, supporting robustness.

## Figures

![Equity Curve](figures/equity_curve.png)
![Z‑Score w/ Trades](figures/zscore_trades.png)

---

## How to Reproduce

### Option 1: Run in Google Colab (recommended)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/eleubner02/01-Stat-Arb-Pairs-Trading/blob/main/notebooks/pairs_trading_analysis_v1.ipynb
)

### Option 2: Run Locally
```bash
git clone https://github.com/eleubner02/01-Stat-Arb-Pairs-Trading.git
cd 01-Stat-Arb-Pairs-Trading
pip install -r requirements.txt
jupyter notebook notebooks/pairs_trading_analysis_v1.ipynb
```
