# Risk Parity Portfolio Analysis

This repository contains code and data for analyzing risk parity investment strategies compared to traditional portfolios and leveraged single-asset approaches. The research examines how different risk parity implementations perform across various market regimes, with particular focus on crisis periods.

## Overview

Risk parity is an investment approach that allocates portfolio exposure based on risk contribution rather than capital allocation. The strategy was popularized by Bridgewater Associates' All Weather Fund in the 1990s and has since gained significant traction in institutional portfolio management.

This research explores three simple risk parity implementations:
- Stock-Bond Risk Parity (SPY + TLT)
- Stock-Gold Risk Parity (SPY + GLD)
- Stock-Bond-Gold Risk Parity (SPY + TLT + GLD)

All strategies are calibrated to target 10% annualized volatility for direct performance comparison against the S&P 500 and leveraged individual assets.

## Repository Structure

```
.
├── final_report.ipynb       # Main analysis notebook with results and visualizations
├── README.md                # This file
└── data/                    # Data directory
    ├── price_data.csv       # Daily ETF price data (SPY, TLT, GLD)
    ├── collect_data.ipynb   # Notebook used to collect and process the price data
    ├── F-F_Research_Data_Factors.CSV        # Fama-French 3-factor data
    ├── F-F_Research_Data_5_Factors_2x3.csv  # Fama-French 5-factor data
    └── F-F_Momentum_Factor.CSV              # Momentum factor data
```

## Key Features

- **Risk Parity Implementation**: Full covariance matrix-based risk parity with volatility targeting
- **Crisis Analysis**: Performance during 2008 Financial Crisis, 2020 COVID Crash, and 2025 Tariff Crisis
- **Factor Regression**: Analysis of alpha across multiple factor models (CAPM, FF3, FF5, FF5+Momentum)
- **Market Regime Comparison**: Performance in bull vs. bear markets
- **Dynamic Weight Analysis**: Evolution of portfolio allocations over time

## Main Findings

1. Risk parity strategies delivered superior risk-adjusted returns compared to traditional approaches
2. Significant downside protection during crisis periods (drawdowns limited to 15-20% vs. 50%+ for S&P 500)
3. Three-asset risk parity (Stock-Bond-Gold) showed better crisis resilience than two-asset approaches
4. Risk parity strategies generated significant alpha across different factor models
5. More consistent year-to-year returns compared to S&P 500

## Usage

To reproduce the analysis:

1. Clone this repository
2. Make sure you have the required dependencies installed (see Requirements section)
3. Run `final_report.ipynb` to generate all results and visualizations

## Data Sources

- ETF price data (SPY, TLT, GLD) collected using `collect_data.ipynb`
- Fama-French factor data obtained from Kenneth French's data library
- Crisis period definitions included in the code

## Requirements

- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- SciPy
- Statsmodels

## Citation

If you use this code or research in your work, please cite:

```
@misc{risk_parity_analysis,
  author = {Matthew Casertano},
  title = {Risk Parity Portfolio Construction: A Comparative Analysis of Multi-Asset Allocation Strategies},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/matthewcasertano/risk-parity-analysis}
}
```

## License

MIT License

## Contact

For questions or feedback, please open an issue on this repository or contact mcaserta@caltech.edu.
