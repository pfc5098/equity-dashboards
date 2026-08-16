# Equity fundamentals dashboards

Per-ticker fundamental dashboards — a **depth** companion to the breadth-oriented
[daily stock scan](https://pfc5098.github.io/investment-scanner/).

Each ticker page shows six charts — balance sheet, income statement, and cash flow, each in a
**10-year annual** and **10-quarter trailing** view — with:

- grouped bars per metric, plus **Net Income** and **Free Cash Flow** trend lines
- an aligned **growth table** below every chart (YoY on annual, QoQ on quarterly) showing *every*
  metric for *every* period
- a dashed **Liabilities ÷ Assets** leverage line on a secondary axis (auto-extends past 100%
  for negative-equity issuers)
- **instant hover tooltips** on every bar, trend-line segment, and point

## Tickers

| | | |
|---|---|---|
| [NVDA](dashboards/nvda.html) | NVIDIA | AI compute |
| [GOOGL](dashboards/googl.html) | Alphabet | cloud & search |
| [LLY](dashboards/lly.html) | Eli Lilly | pharma |
| [CEG](dashboards/ceg.html) | Constellation Energy | nuclear power |
| [CRDO](dashboards/crdo.html) | Credo Technology | AI interconnect |

## Technical notes

Charts are **pre-rendered inline SVG**, generated deterministically in Python. There is no
charting library, no JavaScript beyond a ~20-line tooltip handler, no CDN, and no external
network request — each page is a single self-contained HTML file that opens by double-click.

Fiscal-year handling is per-issuer, so offset-fiscal-year names label correctly
(e.g. NVDA's January year-end renders as `Q1 FY27`, not a calendar quarter).

## Data

Financials are sourced from Alpha Vantage. **The raw vendor data series is not redistributed
here** — only the rendered charts. Figures are as-reported and were spot-checked against company
filings and press releases.

Where a company's reported basis differs from the vendor feed, or where GAAP figures are
distorted (e.g. mark-to-market on equity stakes, non-economic REIT depreciation, hedge marks at
independent power producers), the relevant page carries a note in its header.

---

*Personal research project, published as a work sample. **Not investment advice.***
