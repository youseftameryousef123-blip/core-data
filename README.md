# Real Estate Market Analysis: Trends, Value & Market Insights in Egypt
### Data Analysis Case Study using Python, SQL, and Power BI

---

## Executive Summary

This project demonstrates a complete analytics workflow that transforms raw real estate listing data into actionable market insights.

The objective is to simulate how analysts support investment and purchasing decisions by preparing data, exploring pricing patterns, segmenting markets by location and property features, and presenting insights through an interactive dashboard.

The analysis focuses on understanding apartment pricing behavior, identifying high-value and undervalued areas, and supporting data-driven decisions for buyers, sellers, and investors across the Egyptian real estate market.

---

## Project Objectives

- Analyze apartment pricing patterns across Egyptian neighborhoods
- Identify key drivers of property value (finishing level, floor level, seller type)
- Detect overpriced and undervalued market segments
- Support targeted investment and purchasing decisions
- Present insights using interactive dashboards

---

## Dataset Overview

The project uses a structured apartment listings dataset containing:

- Apartment area (m²)
- Number of rooms and bathrooms
- Floor level and year built
- Listing price and price per m²
- Seller type (Developer, Broker)
- Finishing level (Basic, Finished, Super Lux, Ultra)
- Payment method (Cash, Installments, Cash or Installments)
- Location (neighborhood or compound name)

| Attribute | Details |
|---|---|
| Total Records | 4,784 apartment listings |
| Total Features | 13 columns |
| Geography | Egypt — multiple cities and neighborhoods |
| Unique Locations | 1,636 distinct areas |
| Price Range | 500,000 EGP — 98,380,000 EGP |
| Area Range | 35 m² — 534 m² |
| Average Price per m² | ~ 42,903 EGP/m² |

---

## Technologies & Tools

| Area | Tools |
|---|---|
| Data Preparation | Python (Pandas, NumPy) |
| Data Querying & Modeling | SQL (SQLite) |
| Data Analysis | Python (Pandas, Matplotlib, Seaborn) |
| Visualization | Power BI |
| Version Control | GitHub |

---

## Analysis Questions

The following 10 questions drive the entire analysis:

1. **Which neighborhoods are the most expensive and most affordable** based on average price per m²?
2. **Does finishing level significantly affect price per m²?** How much does Basic vs Ultra finishing differ?
3. **Do Developers charge more than Brokers** for similar properties?
4. **Are Off-Plan properties more expensive than Ready ones?** And what payment methods are associated with each?
5. **What factors correlate most with price?** (area, rooms, floor level, year built)
6. **How is the market distributed across price tiers?** (Budget / Mid-Range / Premium / Luxury)
7. **Are there undervalued neighborhoods** that offer high-quality properties at below-average prices?
8. **How have prices changed over the decades?** (Pre-2000 → 2000s → 2010s → 2020–2026 → Off-Plan)
9. **Are there price outliers?** Properties with unusually high or low price per m²?
10. **What is the relationship between apartment area and total price?** Is it linear?

---

## Methodology

### 1. Data Preparation (Python)
- Inspect data structure and column types
- Handle missing values (Floor Level: 333, Year Built: 180, Bathrooms: 21)
- Standardize price strings to numeric format
- Unify finishing level categories (Basic / Finished / Super Lux / Ultra)
- Flag and clean data quality issues in Seller Type column
- Engineer new features: Price Tier, Area Bracket, Property Status, Decade Built

### 2. Data Modeling (SQL)
- Design Star Schema: fact_listings + 4 dimension tables
- Load cleaned data into SQLite database
- Create 7 analytical views for direct use in Power BI

### 3. Exploratory Data Analysis (Python)
- Price distribution and outlier detection
- Price per m² analysis across locations
- Finishing level impact on price
- Seller type comparison (Developer vs. Broker)
- Year built and decade trend analysis
- Correlation matrix across numeric features

### 4. Market Segmentation
Location-based and feature-based segmentation is applied:

- **Location Tier** — neighborhoods ranked by average price per m²
- **Finishing Premium** — price uplift from Basic to Ultra finishing
- **Seller Type Gap** — pricing difference between seller categories
- **Property Status** — Ready vs. Off-Plan pricing comparison

### 5. Dashboard & Reporting (Power BI)
An interactive dashboard communicates insights including:

- Price heatmap by neighborhood
- Price per m² by finishing level
- Seller type distribution and pricing comparison
- Payment method breakdown
- Decade built vs. price trend
- Off-Plan vs. Ready comparison

---

## Key Performance Indicators (KPIs)

- Average price per m² overall and by location
- Finishing level price premium (Basic → Ultra)
- Seller type pricing gap (Developer vs. Broker)
- Off-Plan vs. Ready price difference
- Top 10 locations by listing volume
- Market share by price tier (Budget / Mid-Range / Premium / Luxury)
- Data completeness rate

---

## Project Workflow

```
Raw Data → Cleaning (Python) → Modeling (SQL) → Analysis (Python) → Dashboard (Power BI) → Recommendations
```

---

## Deliverables

- Cleaned dataset (`real_estate_FINAL.xlsx`)
- SQL schema and queries (`real_estate.db` + `schema.sql`)
- Python analysis scripts (`01_data_cleaning.py`, `02_sql_modeling.py`, `03_eda_analysis.py`)
- Power BI dashboard
- Business recommendations report

---

## Project Structure

```
project/
│
├── data/
│   ├── raw/                  # original dataset
│   └── cleaned/              # real_estate_FINAL.xlsx
│
├── sql/
│   ├── schema.sql            # database schema
│   └── real_estate.db        # SQLite database
│
├── notebooks/
│   ├── 01_data_cleaning.py
│   ├── 02_sql_modeling.py
│   └── 03_eda_analysis.py
│
├── charts/                   # all EDA charts (PNG)
├── dashboard/                # Power BI file (.pbix)
└── README.md
```

---

## Market Insights Goals

The analysis aims to support decisions such as:

- Identifying undervalued neighborhoods with high potential
- Understanding the true price premium of finishing level
- Comparing Developer vs. Broker pricing for similar properties
- Supporting buyers in benchmarking fair market prices
- Helping investors identify the best price-to-value areas

---

## Future Improvements

- Predictive pricing model using machine learning
- Rental yield and investment return analysis
- Expansion to more Egyptian governorates
- Real-time data updates via web scraping pipelines
- Adding view type analysis when data becomes available

---

## Team Members

| Name | Role | Email | LinkedIn |
|---|---|---|---|
| Yousef Tamer | Data Curator | [Email](mailto:youseftameryousef123@gmail.com) | [LinkedIn](https://www.linkedin.com/in/yousef-tamer-5ab124357) |
| Ahmed Abd Elhay | Data Modeling | [Email](mailto:aelgawit@gmail.com) | [LinkedIn](https://www.linkedin.com/in/ahmed-abd-elhay-b2811b3a8) |
| Hoda Ashraf | Data Analyst | [Email](mailto:hodashrafn3w20@gmail.com) | [LinkedIn](https://www.linkedin.com/in/hoda-ashraf-9797a329a) |
| Sama Hussien | Viz Wizard | [Email](mailto:semsemaa10a@gmail.com) | [LinkedIn](https://www.linkedin.com/in/sama-hussien-2b8384389) |
---

## Contributions & Support

If you find this project valuable, give it a ⭐ star and contribute via pull requests!

---

*© 2026 Data Core Team. All Rights Reserved.*
