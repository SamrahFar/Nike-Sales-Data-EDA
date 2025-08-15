# Project Report: Nike Sales Data Cleaning & EDA

---

## Executive Summary

This project delivers a thorough, reproducible workflow for cleaning and exploring Nike's uncleaned sales dataset. The aim is to transform raw, inconsistent data into a reliable foundation for analysis, uncover key patterns, and enable actionable insights for the business and future modeling.

---

## Project Objectives

- **Data Quality:** Address missing, incorrect, and inconsistent values for robust analytics.
- **Feature Engineering:** Create new variables and flags to enrich analysis and modeling potential.
- **Outlier Management:** Identify and visualize outliers for key fields.
- **Exploratory Data Analysis (EDA):** Provide visual and statistical summaries to inform business decisions.

---

## Dataset Overview

- **Source:** Nike_Sales_Uncleaned.csv  
- **Records:** 2,500  
- **Features:** Sales, product line, region, date, units sold, MRP, discount, revenue, profit, size, etc.

---

## Data Cleaning Steps

1. **Missing Values:**  
   - Impute missing dates (forward fill).
   - Impute missing MRP (mean per product line).
   - Impute missing size (mode per product line).
   - Fill missing discounts (zero).

2. **Incorrect/Negative Values:**  
   - Negative units treated as returns, split into "Units_Sold_Positive" and "Units_Returned".
   - Negative profit flagged as "Loss".

3. **Consistency:**  
   - Standardized region names, date formats, and discount formats.

---

## Feature Engineering

- **Outlier Flags:**  
  IQR-based outlier detection for MRP, Revenue, Profit, Loss.
- **Units Returned:**  
  New feature to capture negative sales.
- **Size Categories:**  
  Numerical binning for product sizes.
- **Loss Column:**  
  Tracks negative profits for further analysis.

---

## Exploratory Data Analysis

- **Distribution Analysis:**  
  - Product line counts and size relationships.
  - Histograms and boxplots for sales, profit, loss, revenue, and MRP.
- **Sales Insights:**  
  - Total sales by product line.
  - Correlation analysis for numerical features.
- **Size Category:**  
  - Identification of sales patterns by size group.

---

## Key Findings

- **Data Issues:**  
  - High prevalence of missing values in Units_Sold, MRP, Discount_Applied, and Order_Date.
  - Data inconsistencies in region and size formats.
- **Outliers:**  
  - Significant outliers in revenue, profit, and MRP require careful treatment in modeling.
- **Sales Patterns:**  
  - Training and Basketball product lines lead in total sales.
  - Most sales concentrated in certain size categories.

---

## Recommendations

- **Modeling:**  
  Use cleaned dataset for predictive analytics, e.g., sales forecasting, customer segmentation.
- **Business:**  
  Target top-selling product lines and optimize sizes based on demand.
- **Further Analysis:**  
  Explore regional trends, channel performance, and discount effectiveness.

---

## Reproducibility & Best Practices

- **Notebook Structure:**  
  Clear markdown headers, code comments, visualizations, and conclusions for transparency.
- **Code Quality:**  
  All steps are well-documented and explained for easy reuse.
- **Versioning:**  
  Raw and cleaned datasets can be versioned for traceability.

---

## Next Steps

- Extend analysis with time series modeling or machine learning.
- Automate cleaning and reporting for future datasets.
- Integrate additional data sources (e.g., customer demographics, inventory).

---

**Prepared by:**  
Samrah Far  
Nike Sales EDA Project  
2025-08-15
