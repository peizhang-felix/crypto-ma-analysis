# Crypto Momentum & Risk Intelligence — BTC / ETH / ADA

A quantitative research project on major crypto assets analyzing momentum behavior, market stress levels, and risk-adjusted performance.

📌 Deliverables include:
- Price momentum regime detection (MA20 vs MA60)
- Multi-asset drawdown analytics
- Tail-risk & recovery scoring
- Institutional-style risk radar comparison

---
## 1️⃣ Trend & Momentum Insights

| Asset | MA20 vs MA60 Signal | Commentary |
|------|--------------------|------------|
| **BTC** | Bearish → Neutral | Weak recovery; leadership remains intact |
| **ETH** | Approaching Bullish | Higher sensitivity to upside momentum |
| **ADA** | Persistent Bearish | Structural weakness in trend stability |

> ETH currently demonstrates the strongest rebound potential among the three.

---
## 2️⃣ Drawdown Stress — Market Risk Snapshot (Last ~540 Days)

### Bitcoin (BTC)
![BTC Drawdown](btc_dd.png)

- **Max Drawdown:** ~ -32%
- Strong structural resilience
- Shallow corrections vs peers

### Ethereum (ETH)
![ETH Drawdown](eth_dd.png)

- **Max Drawdown:** ~ -55%
- Higher beta asset → deeper cycle shocks
- Attractive when liquidity flows improve

### Cardano (ADA)
![ADA Drawdown](ada_dd.png)

- **Max Drawdown:** ~ -67%
- Recovery remains weak after market stress  
- More speculative → dependent on retail flows

> Drawdown severity accurately reflects institutional confidence and capital stability.

---
## 3️⃣ Tail-Risk vs Recovery — Stress & Resilience Score

| Metric | Definition | Investment Preference |
|--------|------------|---------------------|
| Max Drawdown | Worst loss from peak | Lower better |
| Volatility | Daily return fluctuation | Lower better |
| Tail Risk | Probability of crash days | Lower better |
| Recovery | Price / Cycle peak | Higher better |

---
## 4️⃣ 🔺 Risk Radar — BTC vs ETH vs ADA

![Risk Radar](RiskRadar.png)

### Key Interpretation
- **BTC** → widest radar → **risk anchor & benchmark**
- **ETH** → healthy risk/growth balance
- **ADA** → collapses toward center  
  → **highest downside exposure with limited resilience**

> ADA behaves like leveraged beta — strongest only in confirmed bull phases.

---
## 5️⃣ Portfolio Implications

| Strategy Role | Asset | Allocation Range | Rationale |
|--------------|-------|-----------------|-----------|
| Core Holding | BTC | 70–90% | Structural strength & recovery |
| Growth Overlay | ETH | 10–25% | Beta expansion during bull cycle |
| Cyclical Enhancer | ADA | 0–10% | Tactical only, high volatility risk |

📌 **Risk Control Rules**
- Reduce ADA allocation if BTC breaks below **200-day MA**
- Increase ADA only **after BTC reclaims ATH with volume**

---
## 6️⃣ Future Upgrades

- ⏳ Regime Classification (Momentum + Drawdown Zone)
- ⏳ Strategy Backtesting vs Buy & Hold
- ⏳ Efficient Frontier Optimization
- ⏳ Sharpe / Sortino / Calmar Ratios

> Goal: Build a live **Crypto Risk Intelligence Dashboard** for active management.

---
## 7️⃣ Run the Notebook

```bash
git clone https://github.com/peizhang-felix/crypto-ma-analysis.git
jupyter notebook crypto_ma_analysis.ipynb
👤 Author
Pei Zhang — Aspiring FinTech & Crypto Data Analyst
Python • Crypto Markets • Quant Research
