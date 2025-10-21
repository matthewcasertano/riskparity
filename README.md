# Risk Parity Investment Strategy (2007–2025)

I conducted this analysis to explore **risk parity as a portfolio design framework** — not merely as a diversification trick, but as a philosophy for balancing *risk* rather than *capital*. Using 18 years of daily data (2007–2025), I tested how allocating risk evenly across **stocks (SPY)**, **bonds (TLT)**, and **gold (GLD)** affects long-term returns, drawdowns, and factor-adjusted performance.

---

## Motivation: Beyond 60/40

The **risk parity approach** was popularized by **Bridgewater Associates** in the early 1990s through its flagship *All Weather* strategy, which sought to create portfolios resilient across all economic environments. Bridgewater demonstrated that allocating risk evenly across asset classes — rather than concentrating it in equities — can deliver smoother and more consistent returns over time.

Traditional portfolios like the **60/40 stock–bond mix** appear diversified in capital but are overwhelmingly dominated by equity *risk*. In some market regimes, over **90%** of total variance can come from stocks.

**Risk parity** starts with a simple idea: instead of allocating dollars, allocate **risk contributions** evenly across assets. By doing so — and scaling the combined portfolio to a target volatility — you can achieve more stable returns through structural diversification.

This approach is rooted in the theory of **leverage aversion** (Asness, Frazzini & Pedersen, 2012): investors constrained or unwilling to use leverage overpay for risky assets and underprice safe ones. Risk parity exploits this imbalance by levering safer, higher risk-adjusted-return assets to parity with riskier ones.

---

## Methodology

* **Assets:** SPY (equities), TLT (bonds), GLD (gold)
* **Risk Allocation:** Inverse volatility weighting with full **covariance adjustment**
* **Volatility Target:** 12% annualized, achieved via dynamic leverage
* **Financing Cost:** Risk-free rate + 1% spread
* **Rebalancing:** Daily, using 60-day rolling volatilities

The test covers **Jan 2007 – May 2025**, including multiple crisis regimes: 2008 GFC, 2020 COVID, and 2025 tariff shocks.

---

## Strategies Tested

| Category               | Description                                              |
| ---------------------- | -------------------------------------------------------- |
| **Stock–Bond RP**      | SPY + TLT, equal risk allocation                         |
| **Stock–Gold RP**      | SPY + GLD, equal risk allocation                         |
| **Stock–Bond–Gold RP** | SPY + TLT + GLD (full covariance risk parity)            |
| **Benchmarks**         | S&P 500, 60/40, Equal Weight, Vol-targeted single assets |

---

## Results Summary

| Strategy               | Return    | Sharpe   | Max Drawdown |
| ---------------------- | --------- | -------- | ------------ |
| **Stock–Bond–Gold RP** | **12.0%** | **0.93** | **−24.1%**   |
| Stock–Bond RP          | 11.8%     | 0.89     | −28.7%       |
| Stock–Gold RP          | 11.1%     | 0.84     | −22.7%       |
| Equal Weight           | 8.6%      | 0.88     | −22.7%       |
| 60–40                  | 8.7%      | 0.76     | −29.9%       |
| S&P 500                | 11.7%     | 0.60     | −55.2%       |

**Crisis Protection:**

* **2008 GFC:** RP(S–B–G) −3.9% vs S&P −43.9%
* **2020 COVID:** RP(S–B–G) −0.7% vs S&P −9.0%
* **2025 Tariffs:** RP(S–B–G) +2.3% vs S&P −5.9%

**Factor Alpha:**

* CAPM α ≈ **0.61%/month**, *p* ≈ 0.013
* FF3 α ≈ **0.49%/month**, *p* ≈ 0.034
* FF5+Mom α ≈ **0.40%/month** (positive, not significant at 5%)

---

## Interpretation

1. **Risk parity works.** Equalizing risk exposure produces higher Sharpe ratios and smaller drawdowns without sacrificing long-run returns.
2. **Leverage, when disciplined, is a tool — not a sin.** Scaling balanced portfolios to a target volatility unlocks consistent compounding.
3. **Diversification across uncorrelated assets** produces resilience through all market conditions.
4. **Alpha comes from balance, not prediction.** The outperformance persists even after controlling for standard equity and factor exposures.

---

## Repository Structure

```
├── data/                    # ETF price data (SPY, TLT, GLD)
├── final_code.ipynb         # Full analysis notebook
├── Risk Parity Report.pdf   # Detailed results & charts
└── README.md                # This file
```

---

## How to Run

1. Clone this repository.
2. Open and run `final_code.ipynb` in Jupyter or VS Code.

**Dependencies:** `pandas`, `numpy`, `matplotlib`, `scipy`, `statsmodels`

---