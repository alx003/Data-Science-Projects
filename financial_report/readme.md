# Financial Report Analysis

## Overview

This project analyzes company financial statement data to compare **profitability** and **leverage** across different industry types. Using balance sheet and income statement data, the analysis computes key financial ratios and answers business-oriented questions relevant to managerial decision-making.

The goal is to help stakeholders understand how financial structure and performance differ across industries, and to explore the relationship between leverage and profitability—particularly within real estate companies.

---

## Business Questions

The analysis focuses on answering the following questions:

1. **Which company type has the lowest profitability ratio?**
2. **Which company type has the highest leverage ratio?**
3. **What is the relationship between leverage and profitability in real estate companies?**
   Is it positive, negative, or is there no clear relationship?

---

## Datasets

Two datasets are used in this project:

### 1. `Balance_Sheet.xlsx`

Contains financial information from company balance sheets.

### 2. `Income_Statement.xlsx`

Contains financial information from company income statements.

### Shared Columns

Both datasets include the following columns:

* `Company`: Company ticker symbol
* `comp_type`: Industry classification

  * `tech` – Technology companies
  * `fmcg` – Fast-moving consumer goods companies
  * `real_est` – Real estate companies
* `Year`: Year of the financial data

All other columns contain statement-specific financial metrics (e.g., total liabilities, equity, revenue, costs).

---

## Methodology

### Data Preparation

* Loaded balance sheet and income statement data from Excel files
* Merged datasets on `Company`, `comp_type`, and `Year`
* Cleaned and aligned financial variables for ratio calculations

### Financial Ratios Computed

Two key financial ratios were calculated and stored in a DataFrame named `df_ratios`:

#### 1. Leverage Ratio

* **Definition:** Measures the extent to which a company uses debt to finance its assets
* **Example metrics:** Debt-to-equity ratio or equity multiplier
* **Stored as:** `leverage_ratio`

#### 2. Profitability Ratio

* **Definition:** Measures how efficiently a company generates profit from its operations
* **Example metrics:** Gross margin or operating margin
* **Stored as:** `profitability_ratio`

---

## Analysis

* Aggregated leverage and profitability ratios by company type
* Compared average ratios across industries
* Focused on real estate companies to examine the relationship between leverage and profitability using exploratory analysis and correlation

---

## Key Findings

* Identified the industry with the **lowest average profitability ratio**
* Identified the industry with the **highest average leverage ratio**
* Determined whether leverage and profitability in real estate companies exhibit a **positive, negative, or no clear relationship**

These findings provide insight into how financial structure differs by industry and how leverage may impact performance in capital-intensive sectors such as real estate.

---

## Technologies Used

* **Python**
* **pandas** – data manipulation and merging
* **numpy** – numerical calculations
* **matplotlib / seaborn** – data visualization
* **Jupyter Notebook** – exploratory analysis and reporting

---

## Conclusion

This project demonstrates practical financial data analysis by combining balance sheet and income statement data to compute meaningful ratios. The results highlight structural differences across industries and provide insight into the leverage–profitability relationship in real estate companies.

---
