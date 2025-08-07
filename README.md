# Gen-Z-CPI-Project
This project builds a custom Consumer Price Index (CPI) tailored to Gen Z consumption habits, applying end-to-end data analytics and engineering workflows. 
---
# Gen Z vs. BLS Consumer Price Index (CPI) Analysis

This project explores the differences between traditional CPI (as measured by the U.S. Bureau of Labor Statistics) and a custom **Gen Z CPI**, reflecting generational spending priorities. Visualized using Power BI, the project highlights how inflation impacts Gen Z differently based on their unique consumption patterns from 2020-2025.

---

## Overview

The Consumer Price Index (CPI) is commonly used to track inflation—but does it reflect how younger generations experience it? Does the CPI properly track the bundle of goods that Gen Z buys? This project aims to answer that question by:

* Comparing **BLS CPI-U** and a **custom Gen Z CPI** index from 2020 to 2025.
* Analyzing **year-over-year inflation trends**.
* Visualizing **category weight changes** over time (e.g., housing, food, tech).
* Identifying top inflation contributors for Gen Z.

---

## Files

| File Name                             | Description                                                                      |
| ------------------------------------- | -------------------------------------------------------------------------------- |
| `BLS CPI U.csv`                       | Official CPI-U index and YoY inflation rates from the Bureau of Labor Statistics |
| `CPI GenZ.csv`                        | Gen Z CPI values and calculated YoY changes from 2020–2025                       |
| `Gen Z CPI Index.csv`                 | Raw category-level price and weight data used to build the Gen Z CPI             |
| `Gen Z CPI.pbix`                      | Power BI dashboard file for full visual exploration                              |
| `README.md`                           | This documentation                                                               |

---

## Visualizations

The Power BI dashboard includes:

* **Normalized CPI Index (2020–2025):** Line chart comparing BLS CPI-U vs. Gen Z CPI.
* **Year-over-Year Inflation Rates:** Bar chart showing annual inflation changes for both indexes.
* **Sankey-style Weight Flow:** Category weights over time to show shifting spending patterns.
* **2025 Category Breakdown:** Pie chart of Gen Z's 2025 expenditure distribution.

---

## Key Insights

* **Housing and Tech/Entertainment** dominate Gen Z's CPI weight, together making up \~50% of their consumption basket in 2025.
* While BLS and Gen Z CPI indices trend similarly, Gen Z experiences **greater volatility** in inflation impact due to differing category weights.
* Traditional CPI underrepresents inflation sensitivity for younger consumers focused on rent, streaming, and personal tech.

---

## How It Works

1. **Category weights** and **price levels** were collected for common CPI categories (2020–2025).
2. A **Laspeyres-like index** was constructed to represent Gen Z’s consumption pattern.
3. Yearly CPI values were **normalized to 2020 = 1.00** for comparability.
4. Power BI was used to connect, transform, and visualize the data across all files.

---

## Tools Used

* Microsoft Power BI
* Excel
* Google BigQuery

---
