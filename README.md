# Risk Parity Portfolio Construction

A comprehensive analysis of risk parity strategies using 18 years of market data (2007-2025), examining the value of adding gold to traditional stock-bond allocations.

## Key Findings

**Best Performance**: Stock-Bond-Gold risk parity achieved **0.98 Sharpe ratio** vs 0.60 for S&P 500

**Crisis Protection**: Limited 2008 crisis losses to **2.9%** vs 43.9% for S&P 500, with positive returns during 2020 COVID (+0.4%) and 2025 tariff crises (+2.7%)

**Alpha Generation**: Significant alpha across all factor models, with 0.53% monthly alpha (6.4% annualized)

## Strategies Compared

### Risk Parity
- **Stock-Bond RP**: SPY + TLT
- **Stock-Gold RP**: SPY + GLD  
- **Stock-Bond-Gold RP**: SPY + TLT + GLD

### Benchmarks
- 60-40 Portfolio, Equal Weight, Leveraged Individual Assets, S&P 500

All strategies volatility-targeted to 10% for fair comparison.

## Results Summary

| Strategy | Return | Sharpe | Max Drawdown |
|----------|--------|--------|--------------|
| **Stock-Bond-Gold RP** | **10.5%** | **0.98** | **-20.2%** |
| Stock-Bond RP | 10.3% | 0.95 | -24.2% |
| 60-40 Portfolio | 8.7% | 0.76 | -29.9% |
| S&P 500 | 11.7% | 0.60 | -55.2% |

## Repository Contents

```
├── data/                    # ETF price data (SPY, TLT, GLD)
├── final_code.ipynb        # Complete analysis code
├── Risk Parity Report.pdf  # Full research report
└── README.md
```

## Methodology

- **Risk Allocation**: Inverse volatility weighting with full covariance adjustment
- **Volatility Targeting**: 10% annual target with dynamic leverage
- **Financing Costs**: Risk-free rate + 1% spread
- **Rebalancing**: Daily weight updates based on 60-day rolling volatility

## Key Insights

1. **Gold matters**: Adding gold to stock-bond risk parity significantly improves crisis resilience
2. **Risk beats capital allocation**: Risk parity outperformed traditional 60-40 and equal weight strategies
3. **Crisis alpha**: Automatic rebalancing provides protection during market stress
4. **Efficient leverage**: Risk parity required less leverage than individual volatile assets

## Usage

1. Clone repository
2. Run `final_code.ipynb` for complete analysis
3. See `Risk Parity Report.pdf` for detailed methodology and findings

## Requirements

Standard Python stack: `pandas`, `numpy`, `matplotlib`, `scipy`

---

*Research for educational purposes. Past performance doesn't guarantee future results.*
