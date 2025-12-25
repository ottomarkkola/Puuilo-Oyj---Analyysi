## Puuilo Oyj –DCF Valuation (Python/yfinance + Excel)

This repository contains an end-to-end equity valuation project for **Puuilo Oyj**. Financial statement and market data are pulled with **Python (yfinance)** and exported to Excel. The **DCF valuation model (FCFF-based)** is built in Excel with transparent inputs, formulas, charts, and sensitivity analysis.

---

## Key results (Base case)

- **Fair value:** **15.76 € / share**
- **Current price:** **12.30 €** *(as of: 17.12.2025)*
- **Implied upside:** **+28.1%**
- **WACC:** **9.0%**
- **Terminal growth (g):** **2.0%**
- **Forecast horizon:** **2025–2030E + terminal value (2031→)**

> Note: Values depend heavily on WACC and terminal growth. See the **WACC × g sensitivity table** in the Excel model.

---

## What’s included

- **Python data export (yfinance → pandas → Excel)**
  - Income statement, balance sheet, cash flow statement
  - Key ratios and market data
  - Price history and price chart
  - Analyst estimates (where available)
- **Excel valuation model**
  - FCFF-based DCF (2025–2030E + terminal value)
  - WACC / CAPM calculation (inputs documented)
  - EV → Equity value bridge → **€/share**
  - **Sensitivity analysis (WACC × g)** using Excel Data Table

---

## Method overview

- **FCFF** = NOPAT + D&A − CAPEX − ΔNWC  
- **Enterprise Value (EV)** = PV(FCFF) + PV(Terminal Value)  
- **Equity Value** = EV − Net Debt  
- **Value per share** = Equity Value / Shares Outstanding

---

## Key assumptions (Base case)

- **Revenue growth:** 12% (2025–2028), 10% (2029–2030) — aligned with company strategy guidance
- **EBIT margin:** 17% — aligned with company profitability target until 2030
- **Tax rate:** 20% (used for NOPAT)
- **D&A:** modeled as historical share of revenue (~5%)
- **CAPEX:** modeled as historical share of revenue (~1–2%)
- **ΔNWC:** 2024 was an outlier due to inventory build-up; assumed to normalize (still slightly negative in forecasts)
- **Terminal growth (g):** 2% (inflation + small real growth)

---

## Data sources

- **yfinance (Yahoo Finance):** financial statements, ratios, price history (availability may vary for Nordic tickers)
- **Puuilo annual report / interim reports:** cross-checks (net debt, IFRS16 lease impact, inventory / working capital discussion)
- **Risk-free rate & equity risk premium:** documented in the Excel notes (update date/source in the model)

---






