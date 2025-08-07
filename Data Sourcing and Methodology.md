# Gen Z CPI Index – Item-Level Data Documentation

## 1. Overview / Purpose

This document outlines the structure, source, and metadata for item-level **price** and **weight** data used to calculate the **Gen Z Consumer Price Index (CPI)** from 2020 to 2025.
---

## 2. Data Sources

| Source              | Description                               | Reference/URL                                      
| ------------------- | ----------------------------------------- | -------------------------------------------------- 
| BLS CPI-U           | Baseline CPI index for comparison         | https://www.bls.gov/cpi
| Custom Gen Z Basket | Gen Z-specific weights and item selection | User-constructed; based on survey data and consumption patters                  
| Price Data (CSV)    | Item prices across 2020–2025              | `Gen Z CPI Index.csv`                              
| Weight Data (CSV)   | Item weights by year, 2020–2025           | `Gen Z CPI Index.csv`                              

https://nielseniq.com/global/en/landing-page/spend-z/
https://www.deloitte.com/global/en/issues/work/genz-millennial-survey.html
https://www.mckinsey.com/featured-insights/generation-z
https://www.askattest.com/blog/research/gen-z-media-consumption
https://www.statista.com/topics/11087/gen-z-online-shopping-behavior/#statisticChapter
https://www.britopian.com/data/gen-z-trends-2023/
https://www.mintel.com/insights/consumer-research/the-future-of-consumer-behaviour-in-the-age-of-gen-z/
---

## 3. Schema Definition

| Field Name    | Description                           | Example            | Data Type |
| ------------- | ------------------------------------- | ------------------ | --------- |
| `Item`        | Specific item name                    | Spotify            | String    |
| `Category`    | Broader CPI category                  | Tech/Entertainment | String    |
| `Weight_2020` | Gen Z weight in 2020 (normalized 0–1) | 0.03               | Float     |
| `Weight_2021` | Gen Z weight in 2021                  | 0.03               | Float     |
| `...`         | Weights for each year                 | ...                | Float     |
| `Price_2020`  | Item price in 2020                    | 9.99               | Float     |
| `Price_2021`  | Item price in 2021                    | 9.99               | Float     |
| `...`         | Prices for other years                | ...                | Float     |

---

## 4. Item-Level Table by Category

### Apparel

| Item              | Prices (2020–2025) | Weights (2020–2025) |
| ----------------- | ------------------ | ------------------- |
| Shein Graphic Tee | $7.50 → $11.00     | 0.053 → 0.0245      |
| Nike Sneakers     | $88.38 → $110.00   | 0.0426 → 0.0392     |

**Notes/Sources**: Prices from brand websites and online retailers via wayback machine and BLS data estimating average (~3%) inflation. Weights based on trend analysis, fashion industry reports, and Gen Z survey preferences. 
https://www.reuters.com/graphics/USA-TRUMP/TARIFF-SHEIN/lbpgzlrjzvq/
https://www.cnbc.com/2025/05/21/nike-price-increases-tariffs.html?msockid=3d4d7e6979aa6d0f0ffd684578216cce


### Education

| Item                                       | Prices (2020–2025) | Weights (2020–2025) |
| ------------------------------------------ | ------------------ | ------------------- |
| Chegg Subscription                         | $14.95 → $15.95    | 0.021 → 0.0196      |
| Public In-State College Tuition (Semester) | $5,280 → $5,950    | 0.021 → 0.0245      |

**Notes/Sources**: Tuition from state university listings and IPEDS; Chegg from official subscription pages.
https://www.chegg.com/study
https://educationdata.org/average-cost-of-college
https://research.collegeboard.org/trends/college-pricing
https://nces.ed.gov/programs/digest/d23/tables/dt23_330.20.asp
https://nces.ed.gov/programs/digest/d20/tables/dt20_330.20.asp

### Food

| Item                      | Prices (2020–2025) | Weights (2020–2025) |
| ------------------------- | ------------------ | ------------------- |
| Chick-fil-A Sandwich Meal | $7.50 → $10.50     | 0.053 → 0.0441      |
| Chipotle Base Entrée      | $7.50 → $11.50     | 0.0372 → 0.0245     |
| DoorDash Order            | $22.00 → $32.00    | 0.0372 → 0.0490     |
| Starbucks Pink Drink      | $4.45 → $5.95      | 0.0319 → 0.0245     |

**Notes/Sources**: Menu prices sampled nationwide and aquired through wayback machine sampling, national averages, and BLS out of home YoY changes. Weights estimated from food delivery usage, restaurant app statistics, and Gen Z digital purchase trends.

### Housing

| Item           | Prices (2020–2025) | Weights (2020–2025) |
| -------------- | ------------------ | ------------------- |
| 1-Bedroom Rent | $1,225 → $1,553    | 0.213 → 0.2451      |
| Wi-Fi Plan     | $78.00 → $86.00    | 0.053 → 0.0490      |

**Notes/Sources**: Rent prices from Zillow Rental Index and FMV yearly estimates; Wi-Fi costs from major ISPs and BLS Internet services and electronic information providers

https://ipropertymanagement.com/research/average-rent-by-year
https://www.zillow.com/research/data/
https://www.xfinity.com
https://www.in2013dollars.com/Internet-services-and-electronic-information-providers/price-inflation

### Personal Care

| Item                  | Prices (2020–2025) | Weights (2020–2025) |
| --------------------- | ------------------ | ------------------- |
| CeraVe Cream 16 oz    | $15.50 → $18.50    | 0.0372 → 0.0392     |
| Calm App Subscription | $62.50 → $70.00    | 0.0266 → 0.0294     |

**Notes/Sources**: CeraVe prices from online and store vendors (amazon. walmart). Calm app pricing page, and mobile usage behavior data.
https://www.calm.com

### Recreation

| Item                 | Prices (2020–2025)  | Weights (2020–2025) |
| -------------------- | ------------------- | ------------------- |
| Budget Travel Flight | $225.00 → $285.00   | 0.0319 → 0.0392     |
| Concert Ticket       | $94.67 → $140.00    | 0.0319 → 0.0490     |

**Notes/Sources**: Prices based on Hopper and Expedia airfare averages, as well as Ticketmaster, SeatGeek, and event price trackers.

### Tech/Entertainment

| Item                    | Prices (2020–2025) | Weights (2020–2025) |
| ----------------------- | ------------------ | ------------------- |
| Netflix Plan Standard   | $12.99 → $17.99    | 0.0851 → 0.0784     |
| iPhone Base Model       | $799.00 → $899.00  | 0.0745 → 0.0686     |
| Spotify Premium         | $9.99 → $11.99     | 0.0319 → 0.0392     |
| Xbox Game Pass Ultimate | $14.99 → $19.99    | 0.0213 → 0.0343     |

**Notes/Sources**: Data collected from Apple, Microsoft, Netflix, Spotify, and subscription change logs.

### Transportation

| Item                | Prices (2020–2025) | Weights (2020–2025) |
| ------------------- | ------------------ | ------------------- |
| Uber Ride 10 Miles  | $19.00 → $25.00    | 0.0426 → 0.0588     |
| Public Transit Pass | $80.00 → $105.00   | 0.0319 → 0.0049     |
| Regular Gasoline    | $2.19 → $3.13      | 0.0213 → 0.0147     |

**Notes/Sources**: Uber pricing based on national fare estimates; transit passes from city transit websites; fuel data from U.S. Energy Information Administration (EIA).
 https://www.eia.gov/petroleum/gasdiesel/
---

## 5. Assumptions & Methodology

* **Normalization**: All weights are normalized annually to sum to 1.0.
* **Inflation Formula**: Laspeyres CPI = Σ(Base Year Weight × Current Year Price) / Σ(Base Year Weight × Base Year Price).
* **Data Sourcing**: Prices collected from online vendors, brand websites, public APIs, or approximated using BLS data and Gen Z usage reports.
* **Weight Estimation**: Based on Gen Z-specific consumption habits (e.g., brand preference surveys, digital behavior, academic reports) and yearly google trends.

---
