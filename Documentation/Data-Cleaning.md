# Data Overview & Preparation

## Data Source
The dataset used for this dashboard was sourced from **Kaggle** and represents a **SaaS sales analytics domain modeled on an AWS-style product portfolio**. It contains historical transactional data capturing customer purchases across multiple products, regions, and industries. The dataset is well-suited for business intelligence use cases as it reflects real-world SaaS sales patterns such as recurring customers, regional performance variation, discounting, and profitability differences.

**Why this source matters:**  
Using a Kaggle dataset allows for realistic, production-like analysis while maintaining transparency and reproducibility. The SaaS-focused structure aligns well with modern cloud-based product businesses and supports meaningful revenue and profitability analysis.

---

## Data Scope
The dataset provides a broad yet manageable analytical scope, enabling both high-level insights and granular exploration:

- **Total Orders:** 5,009  
  Represents individual completed sales transactions, forming the foundation for volume and demand analysis.

- **Total Revenue:** $2.30M  
  Indicates the overall scale of business activity captured in the dataset.

- **Total Customers:** 9,994  
  Reflects a wide customer base, enabling customer-level and segmentation analysis.

- **Regions Covered:** Americas, Europe & Middle East, Asia Pacific & Japan  
  Allows comparative geographic analysis and regional performance evaluation.

- **Industries:** Finance, Energy, Manufacturing, Healthcare, Technology  
  Enables vertical-based analysis to understand sector-specific performance and specialization.

**Why scope definition is important:**  
Clearly defining data scope ensures stakeholders understand the coverage, limitations, and representativeness of the analysis, preventing overgeneralization of insights.

---

## Data Preparation & Cleaning

### Data Quality Assessment
An initial data quality review was conducted to evaluate the reliability and readiness of the dataset for analysis. This assessment identified common real-world data issues such as missing values, inconsistent naming conventions across categorical fields, formatting inconsistencies in numeric and currency columns, and the presence of duplicate or invalid records.

**Analytical Importance:**  
Early validation helps prevent misleading insights and ensures that downstream metrics and visuals are built on accurate, trustworthy data.

---

### Data Cleaning Operations
To address the identified issues, the following cleaning steps were performed using Power Query:

- **Null Value Handling:**  
  Missing values were either excluded or logically imputed based on business relevance to avoid skewed metrics.

- **Standardization of Categorical Fields:**  
  Region, country, product, and industry names were standardized to ensure consistent grouping and filtering.

- **Numeric and Currency Validation:**  
  Sales, profit, and discount fields were validated and formatted to maintain numerical accuracy and consistency.

- **Duplicate & Invalid Record Removal:**  
  Redundant or erroneous transactions were removed to preserve data integrity.

**Why this matters:**  
Clean data ensures that KPIs such as revenue, profit, and customer counts accurately reflect business performance rather than data artifacts.

---

### Calculated Fields
To support deeper analysis and reduce repeated computation at the visualization layer, several calculated fields were created:

- **Average Order Value (AOV):**  
  Helps evaluate deal size and pricing effectiveness.

- **Revenue per Customer:**  
  Measures customer value and supports segmentation and monetization analysis.

- **Profit Margin:**  
  Normalizes profitability and enables comparison across products, regions, and industries.

**Analytical Benefit:**  
Derived metrics enhance analytical depth while maintaining consistent logic across the dashboard.

---

### Data Modeling Approach
The dataset was structured using a **dimensional (star schema) modeling approach**, which is a best practice for analytical and BI workloads:

- **Fact Table:**  
  Sales transactions containing measurable metrics such as sales, profit, discounts, and order counts.

- **Dimension Tables:**  
  Products, Customers, Regions, and Industries providing descriptive context for slicing and filtering.

**Why this approach was chosen:**  
This structure improves query performance, simplifies DAX calculations, ensures consistent filter behavior, and supports scalable, flexible analytics as the dashboard evolves.
