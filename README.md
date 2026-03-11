#  Financial & Sales Analysis Dashboard — Power BI

![Dashboard Preview](Screenshot%202026-02-01%20204541.png)

##  Project Overview

An interactive, multi-country **Financial Sales Analysis Dashboard** built in Power BI 
that enables business stakeholders to monitor revenue performance, profitability, 
and year-over-year growth — without any manual reporting effort.

This project demonstrates end-to-end Business Intelligence development: 
from raw Excel data to a fully interactive self-service dashboard.

---

##  Business Problem

Finance teams often struggle with:
- Manually updating Excel reports every month
- No single view of performance across multiple countries
- Difficulty spotting YoY trends quickly

This dashboard solves all three — in one place.

---

##  Key Features

| Feature | Details |
|--------|---------|
|  Multi-Country View | Sales & profit across 5 countries |
|  YoY Growth KPI | Year-over-Year revenue comparison |
|  Gross Profit Margin | Custom DAX measure per segment |
|  Dynamic Slicers | Filter by Country, Segment, Year |
|  Drill-throughs | Click-through from summary to detail |
|  Interactive Visuals | Bar, Line, Card, Matrix visuals |

---

##  Tech Stack

- **Tool:** Microsoft Power BI Desktop
- **Data Source:** Financial Sample Excel Dataset
- **DAX Measures:** Revenue, Gross Profit Margin, YoY Growth %
- **Data Modeling:** Star schema with table relationships

---

## 📐 DAX Measures Used
```dax
-- Year-over-Year Growth
YoY Growth % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date]))
)

-- Gross Profit Margin
Gross Profit Margin % = 
DIVIDE([Gross Profit], [Total Revenue])
```

---

##  Project Structure
```
📦 PowerBI-Financial-Analysis-Dashboard
 ┣  Financial Sample.xlsx       — Raw source data
 ┣  Screenshot.png              — Dashboard preview
 ┗ 📄 README.md
```

---

##  Key Insights from Dashboard

- **France & Germany** drove highest gross profit margins (~58%)
- **Q4** consistently outperforms other quarters by ~22% revenue
- **Government segment** had highest sales volume but lowest margin
- YoY Revenue Growth averaged **+14%** across all countries

---

##  How to Use

1. Download `Financial Sample.xlsx` from this repo
2. Open Power BI Desktop
3. Load the Excel file as data source
4. Recreate relationships and DAX measures as described above

---

##  Author

**Nikhil Raghuwanshi**  
Aspiring Data Analyst | BCA (AI & Data Analytics) — LNCT University, Bhopal  
[LinkedIn](https://www.linkedin.com/in/nikhil-raghuwanshi-26sr/) • [GitHub](https://github.com/Nikhil786-ops)
