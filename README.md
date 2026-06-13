# Apple Inc. — Financial Analysis (2025)

A full financial analysis of **Apple Inc. (NASDAQ: AAPL)** for FY2025 — combining business/industry analysis, ratio and valuation analysis (CAPM, FCF, WACC/DCF), and quantitative technical analysis (Monte Carlo, Prophet, moving-average trading signals), ending in an investment recommendation.

> Project for **DAB401 – Financial Analysis**.

---

## 1. Overview

The project evaluates Apple from three angles — **business**, **valuation**, and **technical** — to reach a reasoned investment view. It blends fundamental analysis (financial ratios, intrinsic value) with market data and forecasting models pulled live via `yfinance`.

## 2. Data Sources

- **Apple Inc. 2025 Annual Report (10-K)** — financial statements and FCF inputs (Excel template).
- **`yfinance`** — AAPL and S&P 500 historical prices / daily returns.
- **U.S. Department of the Treasury** — 10-year Treasury yield (risk-free rate).
- **IDC & Counterpoint Research** — smartphone market-share figures.

## 3. Project Structure

```
.
├── Apple_analysis_0873760.ipynb                    # Main notebook (code + charts)
├── Apple_analysis_0873760_.html                    # HTML export of the notebook
├── Final_Report_0873760.pdf                        # Written report (16 pages, TOC)
├── Apple-Inc-Financial-Analysis-Presentation.pptx  # Presentation (21 slides)
├── AAPL_Financial_Template_Filled_0873760_final.xlsx  # Filled financial template
│       ├── Apple_FCF_FY2025
│       ├── Financial_Statements
│       └── Financials-2025-Clean
└── README.md
```

## 4. Analysis Sections

**A. Business Analysis** — company overview, current operations, macroeconomic environment, and industry/competition (Apple ~20.0% global smartphone share; ~62% of the premium >$600 segment).

**B. Ratio & Valuation Analysis**
- *Profitability (FY2025):* Gross margin 46.91%, operating 31.97%, net 26.92%, ROA 31.18%, ROE 151.91%, EPS 7.46.
- *Liquidity:* Current 0.893, Quick 0.859, Cash 0.217 (below 1, but offset by strong FCF).
- *Additional:* P/E 34.07, dividend payout 13.77%, D/E 3.87, sustainable growth 131%.
- *CAPM & Cost of Equity:* Beta ≈ 1.2 (10-yr regression of AAPL vs S&P 500); Rf = 2.69%, Rm = 13.85% → **Cost of Equity ≈ 16.16%**.
- *Free Cash Flow:* CFO $111,482M − CapEx $12,715M = **FCF $98,767M (FY2025)**.
- *Valuation (WACC/DCF):* **WACC ≈ 15.79%** → intrinsic firm value ≈ $625,307M → **intrinsic value ≈ $41.65/share**, with a WACC sensitivity analysis showing value's strong inverse dependence on the discount rate.

**C. Technical Analysis**
- 1-year stock price trend (near historical highs).
- **Monte Carlo simulation** (100 paths, 30-day horizon) — likely $270–$310 range, wide $210–$360 spread.
- **Facebook Prophet** 30-day forecast — bullish trend toward ~$290–$300 with widening confidence interval.
- **Moving averages (20 & 50-day SMA)** — Golden Cross / Death Cross trading signals.

**D. Investment Recommendation** — **HOLD**: strong fundamentals (FCF ~$98.8B, ROE ~152%) and a short-term uptrend with no major sell signals, but intrinsic value under the high WACC sits below market price, so no immediate buy is advised.

## 5. Key Takeaways

- Apple shows **exceptional profitability** (ROE 152%) and **stable Free Cash Flow** (~$98.8B), supporting dividends, buybacks, and R&D.
- Liquidity ratios are below 1 but **manageable** given strong cash generation.
- Valuation is **highly sensitive to the discount rate** — at WACC ≈ 15.79% the DCF implies the stock is richly priced.
- Technical signals lean **bullish/short-term up**, reinforcing a **HOLD** rather than buy/sell.

> ⚠️ Forecasts (Monte Carlo, Prophet) and live `yfinance` data are time-dependent; re-running the notebook on a different date will produce different figures. This analysis is educational and **not investment advice**.

## 6. Requirements

- Python 3.x

```bash
pip install pandas numpy matplotlib scipy yfinance prophet openpyxl
```

## 7. How to Run

1. Open `Apple_analysis_0873760.ipynb` (Jupyter Notebook / JupyterLab / VS Code).
2. Ensure internet access is available (the notebook pulls live data via `yfinance`).
3. Keep `AAPL_Financial_Template_Filled_0873760_final.xlsx` in the project folder if a cell reads from it; update the path if needed.
4. Run the cells in order from top to bottom.

## 8. Tech Stack

`pandas` · `numpy` · `matplotlib` · `scipy` (linregress for Beta) · `yfinance` (market data) · `prophet` (time-series forecasting) · `openpyxl` / Excel (financial template)

## Contributors

Truc Anh Nguyen

