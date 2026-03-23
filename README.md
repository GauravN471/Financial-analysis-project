# 💰 Financial P&L Analytics — Excel Power Pivot Report Suite

![Excel](https://img.shields.io/badge/Excel-Power_Pivot-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-ETL-green?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-Calculated_Columns-blue?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Finance_%26_Reporting-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> **"Built a multi-dimensional P&L reporting suite in Excel — delivering Gross Margin %, Net Sales, and profitability breakdowns across markets, fiscal years, and quarters to support strategic finance decisions."**

---

## 🎯 Executive Summary

AtliQ Hardwares' finance team lacked a structured, repeatable way to view Profit & Loss performance across global markets, time periods, and regions — decisions were being made from disconnected spreadsheets with no consistent GM% benchmarking. I built a connected Excel reporting suite using Power Query for ETL, Power Pivot for data modelling, and DAX calculated columns — delivering four finance reports that give leadership a consistent, drillable view of profitability from Gross Sales down to Net Profit.

---

## 🛠 Tech Stack

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Primary reporting environment |
| **Power Query (M)** | ETL — data extraction, cleaning, fiscal calendar generation |
| **Power Pivot** | In-memory data model — relationships between fact and dimension tables |
| **DAX** | Calculated columns for GM%, fiscal month/quarter derivation |
| **Pivot Tables + Slicers** | Dynamic report filtering by market, year, month, region |
| **Conditional Formatting** | Visual GM% performance flags — above/below threshold highlighting |
| **SUMIFS / AVERAGEIFS** | Supporting calculations outside the data model |

---

## 📂 Report Suite — View All 4 Reports

| Report | Description | Link |
|---|---|---|
| 📊 **P&L by Market** | Net Sales, COGS, Gross Margin % across all global markets | [View PDF](https://github.com/GauravN471/Financial-analysis-project/blob/main/P%20%26%20L%20by%20market.pdf) |
| 📅 **P&L by Month** | Monthly revenue and profitability trends — seasonality analysis | [View PDF](https://github.com/GauravN471/Financial-analysis-project/blob/main/P%20%26%20L%20by%20month.pdf) |
| 📆 **P&L by Year** | Year-over-year performance summary — FY growth benchmarking | [View PDF](https://github.com/GauravN471/Financial-analysis-project/blob/main/P%20%26%20L%20by%20year.pdf) |
| 🌏 **GM% by Quarter** | Quarterly Gross Margin % by sub-region — ANZ, India, NA, ROA, SE | [View PDF](https://github.com/GauravN471/Financial-analysis-project/blob/main/GM%25%20by%20quarter.pdf) |

> 📥 Download the full Excel workbook: [Finance Analytics Project.7z](https://github.com/GauravN471/Financial-analysis-project/blob/main/Finance%20analytics%20project.7z)

---

## 🧹 Data Cleaning & Transformation

**1. Fiscal calendar engineering in Power Query**
AtliQ operates on a September–August fiscal year. I generated a custom date table in Power Query deriving fiscal month numbers (Sept = Month 1), fiscal year labels, and quarter mappings — ensuring all P&L period comparisons align to business cycles rather than calendar year.

**2. Multi-table data model in Power Pivot**
Raw data arrived as separate flat files for sales transactions, targets, and market mappings. I built a star-schema-style data model in Power Pivot — linking fact tables (sales, deductions) to dimension tables (market, product, date) via defined relationships, enabling cross-table DAX calculations without VLOOKUP chains.

**3. GM% calculated column via DAX**
Gross Margin % was derived as a DAX calculated column: `GM% = DIVIDE([Gross Margin], [Net Sales], 0)` — applied consistently across all pivot views so the metric is calculated the same way regardless of which dimension a user filters by.

**4. Regional and sub-regional normalization**
Market names and sub-region labels were standardized in Power Query to remove inconsistencies in source data — ensuring "India" and "INDIA" merged as one category and sub-zones (ANZ, NA, ROA, SE) grouped correctly in the GM% by Quarter report.

---

## 💡 Business Insights — The "So What?"

- **Identified significant GM% variance across sub-regions** — with India and ANZ showing structurally different margin profiles quarter-over-quarter, indicating that a single global pricing strategy was creating margin compression in some markets while leaving others over-priced relative to competition.

- **Revealed a consistent revenue spike in Q3 (March–May) and Q4 (June–Aug) across fiscal years** — confirming that AtliQ's sales cycle is heavily back-loaded, which has direct implications for working capital planning, procurement timing, and sales team incentive structures.

- **Found that markets contributing the highest Net Sales were not always the highest GM% contributors** — high-volume markets were running on thinner margins than smaller markets, suggesting that volume-based discounting was eroding profitability in key accounts without proportional revenue benefit.

---

## 📋 Business Recommendations

1. **Regional Pricing Review** — Sub-regions with consistently below-average GM% (visible in the quarterly report) should trigger a pricing and discount audit — even a 1–2% GM% recovery across those markets materially improves overall profitability.
2. **Back-loaded Revenue Risk** — Q3/Q4 revenue concentration creates cash flow risk if those quarters underperform. Finance should model a downside scenario and set Q1/Q2 targets that reduce full-year dependency on the back half.
3. **Volume vs Margin Discipline** — High-volume, low-margin markets should be evaluated on contribution margin, not just Net Sales — some may be destroying value net of distribution and support costs.
4. **Automate Refresh Cycle** — The current model is manually refreshed. Connecting Power Query to a live data source and scheduling monthly refreshes would make this a live finance reporting tool rather than a point-in-time analysis.

---

## 🗂 Repository Structure
```
Financial-analysis-project/
├── README.md
├── Finance analytics project.7z    ← Full Excel workbook (Power Pivot model)
├── P & L by market.pdf             ← Report 1: P&L across global markets
├── P & L by month.pdf              ← Report 2: Monthly trends
├── P & L by year.pdf               ← Report 3: Year-over-year summary
└── GM% by quarter.pdf              ← Report 4: Regional GM% by quarter
```

---

## 👤 Author

**Gaurav Nikam** — Data Analyst | Excel · Power BI · SQL · Bloomberg Terminal
📧 gauravnikam471@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/-471-gaurav-nikam)
