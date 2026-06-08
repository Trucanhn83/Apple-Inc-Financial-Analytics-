# Apple Inc. (AAPL) — Financial Analysis Report (FY2025)

A financial analysis of **Apple Inc. (AAPL)** for fiscal year 2025, built with **Python** and **Excel**. The project evaluates Apple's fundamentals, estimates intrinsic value, and reviews short-term price momentum to reach an investment recommendation. *(Course project — DAB401.)*

## Overview

The analysis combines three perspectives:

- **Business analysis** — company background, operations, revenue mix, macroeconomic environment, and competitive position.
- **Ratio & valuation analysis** — profitability, liquidity, and leverage ratios; cost of equity via **CAPM** (β ≈ 1.2); **Free Cash Flow** (~$98.8B for FY2025); and intrinsic value per share through a **WACC-based DCF**.
- **Technical analysis** — one-year price trend, **Monte Carlo** simulation, **Facebook Prophet** forecast, and **SMA (20/50-day) crossover** signals.

## Key methods

| Area | What was done |
|------|---------------|
| Beta | Linear regression of AAPL daily returns vs. S&P 500 (10 years) |
| Cost of equity | CAPM: Rf = 2.69%, Rm = 13.85%, β ≈ 1.2 → ~16.16% |
| Valuation | FCF = CFO − CapEx; DCF with WACC ≈ 15.79% → intrinsic value ≈ $41.65/share |
| Forecasting | Monte Carlo (100 paths, 30 days) and Facebook Prophet (30-day horizon) |
| Signals | 20-day vs. 50-day SMA — Golden Cross / Death Cross |

## Tech stack

- **Python** — `pandas`, `numpy`, `yfinance`, `matplotlib`, `scikit-learn`/`statsmodels` (regression), `prophet` (forecasting)
- **Excel** — source financial data (Apple 2025 Annual Report), ratio calculations, and WACC sensitivity table
- Data sources: Apple Annual Report 2025, Yahoo Finance, U.S. Treasury yield curve, IDC, Counterpoint Research

## Conclusion

**Recommendation: HOLD.** Apple shows exceptional fundamentals — high ROE, strong and stable free cash flow, and a diversified hardware-plus-services ecosystem — and a confirmed technical uptrend. However, the calculated intrinsic value sits below the current market price, so the report advises holding existing positions rather than initiating a new purchase.

---

*For educational purposes only. Not investment advice
