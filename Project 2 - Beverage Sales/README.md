# 📊 Beverage Sales Analysis Dashboard


## 📑 Table of Contents

1. [Project Overview](#project-overview)  
2. [Data Sources](#data-sources)  
3. [Tools & Technologies](#tools--technologies)  
4. [Data Cleaning & Preparation](#data-cleaning--preparation)  
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
6. [Data Analysis & Modeling](#data-analysis--modeling)  
7. [Results & Findings](#results--findings)  
8. [Recommendations](#recommendations)  
9. [Limitations](#limitations)  
10. [References](#references)


## 📝 Project Overview

This project analyzes beverage sales performance across U.S. states, retailers, and brands using Power BI.

The dashboards provide insights into revenue, units sold, pricing, and key influencers, enabling stakeholders to make informed business decisions.

Two interactive dashboards were developed:
- Beverage Sales Dashboard (Overview): Revenue trends, state-level distribution, retailer performance, and product sales.
- Beverage Sales Performance Dashboard: Brand-level analysis, regional breakdown, key influencers, and advanced revenue insights.


## 📂 Data Sources

- Dataset: [Include dataset link if public, otherwise state "proprietary / simulated dataset"]
- Time Period Covered: Jan 2022 – Dec 2022
- Granularity: State-level, Retailer-level, and Product-level


## 🛠 Tools & Technologies

- Power BI → Dashboard creation, DAX measures, interactive visuals
- Excel / CSV → Data source format
- DAX → Custom measures and calculated columns
- Python (optional) → Data preprocessing & exploratory checks

## 🔧 Data Cleaning & Preparation

Steps taken before visualization:
- Checked for missing values in sales, revenue, and product attributes
- Standardized state names, retailer names, and product categories
- Added derived columns:
  - Customer gender & age group (based on names)
  - Region classification (Indian Zones / U.S. zones depending on context)
- Created a date dimension using DAX (CALENDARAUTO)


## 🔍 Exploratory Data Analysis

Initial exploration focused on:
- Revenue distribution across states & regions
- Sales contribution by brands (Coca-Cola, Diet Coke, Sprite, etc.)
- Retailer-level revenue segmentation
- Average pricing and volume sold


## 📊 Data Analysis

Key measures created in Power BI (DAX):
```Power BI (DAX)
Total Revenue = SUM(Sales[Revenue])
Units Sold = SUM(Sales[Quantity])
Average Price = DIVIDE([Total Revenue],[Units Sold])
Revenue by Month = FORMAT(Orders[OrderDate], "mmm")
% Revenue by Retailer = DIVIDE([Retailer Revenue],[Total Revenue])
```

## 📈 Results & Findings

- Coca-Cola leads with $1.9M in revenue and ~4M units sold.
- Sodapop dominates retailer sales with $9.1M in revenue.
- Sales peak in July (0.97M) and December (0.98M).
- Regional differences highlight concentration of sales in the Midwest and South.
- FizzySip customers show higher spending influence in revenue analysis.


## 💡 Recommendations

- Increase marketing efforts for underperforming products (e.g., Fanta).
- Leverage regional insights to focus campaigns in high-potential states.
- Partner with high-revenue retailers (e.g., Sodapop) for exclusive promotions.
- Adjust pricing strategies in regions with lower per-unit revenue.


## ⚠️ Limitations

- Dataset covers only one year (2022), limiting long-term trend analysis.
- Customer demographics (gender/age) are estimated and not directly verified.
- Retailer categorization may not reflect full distribution network.


## 📚 References

- Power BI Official Documentation → https://learn.microsoft.com/en-us/power-bi/
- DAX Guide → https://dax.guide/
- Dataset Source → [Insert dataset source link or description]
