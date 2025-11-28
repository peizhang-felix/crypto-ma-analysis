# Crypto Market Trend Analysis using Moving Average Models

**Author:** Pei Zhang  
**Last updated:** 2025-11-28  

A Python-based quantitative study of short-term vs mid-term price momentum in major crypto assets using 20-day and 60-day moving averages, with VOO as a traditional equity benchmark.

---

## 1. Research Objective

The goal of this project is to:

- Compare **short-term (MA20)** and **mid-term (MA60)** price trends of BTC, ETH and ADA  
- Contrast crypto momentum behavior with a **traditional equity benchmark (VOO)**  
- Build intuition for **trend strength, reversals and volatility regimes** in crypto markets

This project is an early step in my transition toward **FinTech & Crypto Quant Research**.

---

## 2. Assets & Data

**Assets analyzed**

- **BTC** – Bitcoin  
- **ETH** – Ethereum  
- **ADA** – Cardano  
- **VOO** – Vanguard S&P 500 ETF (benchmark)

**Data source**

- Historical daily prices downloaded via **`yfinance`**  
- Close prices used to compute moving averages  
- Time window: recent months (rolling window, updatable at any time)

---

## 3. Methodology

For each asset, I compute:

- **20-day moving average (MA20)** → captures **short-term momentum**
- **60-day moving average (MA60)** → captures **mid-term trend**

Basic idea:

- **MA20 > MA60** → bullish momentum, short-term trend stronger than mid-term  
- **MA20 < MA60** → bearish momentum, short-term weakness relative to mid-term  
- **Crossovers** between MA20 and MA60 signal potential **trend shifts / momentum reversals**

Mathematically (for closing price \(P_t\)):

\[
MA_{20}(t) = \frac{1}{20}\sum_{i=0}^{19} P_{t-i}, \quad 
MA_{60}(t) = \frac{1}{60}\sum_{i=0}^{59} P_{t-i}
\]

All calculations and plots are implemented in the Jupyter Notebook:
`crypto_ma_analysis.ipynb`.

---

## 4. Price Momentum Analysis

### 4.1 BTC — Bitcoin

![BTC Moving Averages](BTC.png)

**Observations**

- BTC shows relatively **clean MA20–MA60 crossovers** with less noisy whipsaws.  
- In uptrend phases, MA20 stays consistently above MA60 with visible distance.  
- During corrections, MA20 quickly reacts and converges toward MA60.

**Interpretation**

- BTC exhibits the **most stable momentum structure** among the three crypto assets.  
- Trend signals are comparatively more reliable, reflecting **higher liquidity** and  
  stronger participation from long-term / institutional holders.  
- BTC still acts as a **liquidity and sentiment anchor** within the crypto market.

---

### 4.2 ETH — Ethereum

![ETH Moving Averages](ETH.png)

**Observations**

- ETH’s MA20 crosses MA60 **more frequently** than BTC.  
- Short-term rallies often fade quickly, leading to fast reversals around the MA60 line.  
- Distance between MA20 and MA60 tends to be narrower and less persistent.

**Interpretation**

- ETH shows **less stable mid-term momentum** compared with BTC.  
- Price action is more sensitive to **narrative shifts and speculative flows**  
  (DeFi, L2, staking themes, etc.).  
- Momentum signals are usable but require **tighter risk management**.

---

### 4.3 ADA — Cardano

![ADA Moving Averages](ADA.png)

**Observations**

- ADA displays the **noisiest crossover pattern** among the three.  
- MA20 flips above/below MA60 frequently, with many short-lived moves.  
- Trend phases are shorter and reversals more abrupt.

**Interpretation**

- ADA has the **weakest momentum persistence** and **highest volatility exposure**.  
- Momentum behavior suggests stronger **retail-driven trading** and  
  a higher share of speculative capital.  
- Any MA-based strategy on ADA must assume **larger drawdowns** and **lower signal reliability**.

---

### 4.4 VOO — Traditional Equity Benchmark

![VOO Moving Averages](VOO.png)

**Observations**

- VOO’s MA20 and MA60 move **smoothly**, with much fewer crossovers.  
- Trend shifts are slower and more gradual compared to crypto assets.  
- Distance between MA20 and MA60 widens and narrows in a more orderly way.

**Interpretation**

- VOO reflects a market dominated by **institutional capital and long-only flows**.  
- Momentum structure is **more stable and predictable**, with lower emotional trading.  
- Using VOO as a benchmark highlights how **crypto trades in a higher-volatility,  
  higher-reversal regime**.

---

## 5. Key Insights (so far)

1. **Crypto vs Equity Momentum**  
   - BTC, ETH and ADA all exhibit **stronger and more frequent momentum reversals**  
     than VOO, reflecting elevated **speculative sensitivity** and looser anchoring  
     to fundamental cash flows.

2. **Momentum Stability Ranking**  
   - In terms of mid-term momentum stability, a rough ordering is:  
     **BTC > ETH > ADA**.  
   - BTC behaves closest to a “macro asset”, while ADA behaves more like a  
     high-beta speculative token.

3. **Role of BTC in Crypto Structure**  
   - BTC maintains the **cleanest MA structure** and tends to lead trend direction.  
   - This supports the view that BTC acts as a **liquidity and sentiment anchor**  
     for the broader crypto market.

These are **work-in-progress observations**, not investment advice.

---

## 6. Limitations

- Analysis is based on **moving averages only** (trend-following indicator).  
- No transaction costs, slippage or position sizing are included yet.  
- Results depend on the **chosen time window** and **lookback periods (20 / 60)**.  
- No full backtest or risk-adjusted performance metrics are implemented (yet).

These limitations will be addressed in future iterations (see Roadmap).

---

## 7. Future Work & Roadmap

Planned extensions of this project:

1. **Volatility Analysis**  
   - Compute and visualize **rolling volatility** for BTC / ETH / ADA / VOO.  
   - Compare crypto volatility regimes vs equity volatility.

2. **Risk-Adjusted Performance (Sharpe Ratio)**  
   - Estimate **Sharpe ratios** over rolling windows.  
   - Evaluate whether higher returns (if any) compensate for the higher volatility in crypto.

3. **BTC Beta & Cross-Asset Correlation**  
   - Analyze how BTC co-moves with VOO and other benchmarks.  
   - Estimate **beta** and correlation over time to understand structural linkages.

4. **Moving-Average Trading Signal Backtest**  
   - Implement simple MA20–MA60 crossover strategies.  
   - Evaluate performance vs buy-and-hold, including drawdowns and hit ratios.

As I continue my journey toward **FinTech & Crypto Quant**, this repository will grow with more indicators, backtests and cross-asset analysis.

---

## 8. How to Run the Notebook

### Option A — Local environment

1. Clone the repository:

   ```bash
   git clone https://github.com/peizhang-felix/crypto-ma-analysis.git
   cd crypto-ma-analysis
