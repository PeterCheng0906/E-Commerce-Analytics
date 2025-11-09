# E-Commerce Profitability & Fulfillment Analytics  
### Unlocking Multi-Platform Profit Drivers Using RStudio

---

## Project Overview
This project analyzes **multi-platform e-commerce sales data** to uncover the structural drivers of profitability across pricing strategies, product categories, and fulfillment models.  
It combines **data preparation**, **descriptive analytics**, and **predictive modeling** to answer core business questions around how pricing, catalog mix, and operational structure influence e-commerce performance across domestic and international markets.

---

## Dataset Credit
**Dataset:** [*E-Commerce Sales Dataset – "Unlock Profits with E-Commerce Sales Data"*](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data)  
**Author:** *Anil Kumar (Anil)*  

---

## Background
E-commerce retailers operate across multiple platforms (Amazon, Flipkart, Myntra, Ajio, etc.) with heterogeneous pricing, fulfillment, and fee structures.  
This project uses public SKU-level sales and pricing data to evaluate profitability patterns, fulfillment efficiency, and international sales dependencies — providing actionable insights for dynamic pricing and market diversification.

---

## Project Objectives
The analysis aims to **analyze and predict e-commerce profitability** across platforms, fulfillment methods, and international markets using transactional, pricing, and inventory data.

Specifically, it seeks to:

1. **Identify the most profitable product categories** and fulfillment strategies (Amazon FBA vs. Merchant Fulfilled).  
2. **Compare platform and market performance** in terms of margin, sales volume, and operational reliability.  
3. **Quantify key profitability drivers** — price ratio, catalog identity, and fulfillment efficiency.  
4. **Provide actionable recommendations** for pricing, inventory allocation, and cross-market fulfillment.

---

## Business Question
> Which **product categories**, **sales platforms**, and **fulfillment methods** generate the highest profit margins?  
> How do factors such as **pricing structure**, **catalog mix**, and **operational performance** shape profitability across domestic and international markets?

---

## Methodology

### **Prepare**
- Import and merge multiple CSVs  
- Harmonize schemas, standardize currency, and parse dates  

### **Process**
- Remove duplicates, handle missing values, and derive analytical features (`profit`, `profit_margin`, `month`)  

### **Analyze**
- Explore descriptive and diagnostic trends  
- Run regression and tree-based models to identify profit drivers  
- Perform clustering of SKUs and temporal (month-based) patterns  

### **Share**
- Visualize results using `ggplot2` and correlation heatmaps (`ggcorrplot`)  
- Prepare publication-ready tables with `gt`  

### **Act**
- Generate actionable insights for dynamic pricing, catalog prioritization, and fulfillment strategy  

---

## Workflow in RStudio

All analysis was conducted in **RStudio**, organized into two distinct environments:

### Data Preparation Environment
*File: `E-Commerce_Preparation.Rmd`*  
Used for cleaning, validation, and schema consistency checks.

**Packages:**
- `tidyverse` — data wrangling and manipulation (`dplyr`, `tidyr`, `stringr`, `readr`)  
- `readr` — efficient import of large CSV files  
- `janitor` — cleaning and standardizing variable names and table structures  
- `lubridate` — handling and transforming date-time variables  
- `skimr` — quick exploratory summaries  

> These packages ensure a clean, well-structured dataset ready for downstream modeling and visualization.

---

### Analysis & Visualization Environment
*File: `E-Commerce_Analysis_&_Visualization.Rmd`*  
Used for feature analysis, visualization, and predictive modeling.

**Core Wrangling & Plotting**
- `tidyverse` — data wrangling and plotting  
- `lubridate` — managing time-series variables  
- `ggplot2`, `forcats` — category-based and multi-facet visualizations  

**Modeling & Evaluation**
- `broom` — tidy model outputs and coefficient summaries  
- `caret` — unified regression/classification framework  
- `glmnet` — regularized GLMs (LASSO/Ridge)  
- `rpart`, `rpart.plot` — decision tree modeling and visualization  
- `randomForest` — ensemble learning for feature importance  

**Diagnostics & Visualization**
- `ggcorrplot` — correlation heatmaps for feature diagnostics  

**Reporting**
- `gt` — summary tables for report-ready outputs  

---

## Repository Structure
```text
E-Commerce-Analytics/
├── data/
│   ├── raw_data.zip
│   ├── processed.zip
│   └── Archive_unused.zip
├── scripts/
│   ├── E-Commerce_Proposal.Rmd
│   ├── E-Commerce_Preparation.Rmd
│   └── E-Commerce_Analysis_&_Visualization.Rmd
├── outputs/
│   ├── E-Commerce-Proposal.html
│   ├── E-Commerce-Proposal.pdf
│   ├── E-Commerce-Preparation.html
│   ├── E-Commerce-Analysis---Visualization.html
│   └── E-Commerce Project.pptx
└── README.md
```

---

## Analytical Highlights

- **Structural Profitability:**  
  Price ratios (`selling_price / cost_price`) and catalog identity are the strongest drivers of profit — independent of seasonality.  

- **Fulfillment Comparison:**  
  Amazon FBA shows higher reliability and order volume, while Merchant Fulfillment maintains flexibility in low-margin categories.  

- **Predictive Modeling Results:**  
  Random Forest outperformed all models, confirming that profitability depends on internal structure, not external cycles.  

- **International Insights:**  
  Revenue is heavily concentrated among a small number of high-value clients, creating growth potential through diversification.  

---

## Recommendations

1. **Adopt dynamic pricing models** based on MRP thresholds identified by decision trees.  
2. **Expand Amazon-based fulfillment** for high-volume, high-margin SKUs.  
3. **Broaden international buyer base** to reduce dependency risks.  
4. **Standardize catalog pricing policies** across marketplaces.  
5. **Leverage predictive insights** for pre-season inventory planning.  

---

## Author
**Peter Cheng**  
M.A. German Studies & M.S. Data Science (Stanford University)  
[cyf0906@stanford.edu]  
California, USA  

---

> *This repository is for academic and portfolio demonstration purposes.  
> Dataset © 2023 by Anil Kumar (Anil) via Kaggle.*

---
