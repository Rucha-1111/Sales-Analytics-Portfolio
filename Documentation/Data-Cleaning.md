# Data Overview & Preparation

## Data Source
- **Platform:** Kaggle
- **Domain:** SaaS Sales Analytics (AWS-style product portfolio)
- **Data Type:** Historical transactional sales data

## Data Scope
- **Total Orders:** 5,009
- **Total Revenue:** $2.30M
- **Total Customers:** 9,994
- **Regions Covered:** Americas, EMEA, APJ
- **Industries:** Finance, Energy, Manufacturing, Healthcare, Technology

## Data Preparation & Cleaning

### Data Quality Assessment
Initial validation identified missing values, inconsistent naming conventions, and formatting issues.

### Data Cleaning Operations
- Handled null values through exclusion or logical imputation
- Standardized region and country naming
- Validated numeric and currency fields
- Removed duplicate or invalid records

### Calculated Fields
- **Average Order Value (AOV)**
- **Revenue per Customer**
- **Profit Margin**

### Data Modeling Approach
The dataset follows a dimensional (star schema) design:
- **Fact Table:** Sales transactions
- **Dimension Tables:** Products, Customers, Regions, Industries

This structure improves query performance and supports flexible analytics.
