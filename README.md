# supermarket-sales-Analytical-Pipeline
End-to-end data engineering pipeline using Azure Databricks, Delta Lake, and ADLS to ingest, transform, and analyze supermarket sales data with optimized bronze-silver-gold architecture.


### 🚀 **Project Overview**

This project focuses on **supermarket sales analysis**, ingesting raw sales data, performing data cleansing and transformation, and creating optimized gold tables for business intelligence. It enables actionable insights on product performance, branch-level trends, and payment method distributions.

The dataset simulates **daily transactions from multiple branches and product lines**, with rawness and mismatched values included to emulate real-world complexity.

---

### 🔷 **Project Requirements**

#### Data Ingestion
1. Ingest raw CSV data from ADLS into a **Bronze Delta table**.
2. Apply appropriate schema during ingestion.
3. Enable SQL-based analysis on ingested raw data.

---

#### Data Transformation
1. Perform data quality checks (nulls, negative totals, duplicate InvoiceIDs).
2. Clean, standardize, and normalize data into a structured model.
3. Partition Silver table by **branch** for optimized downstream querying.

---

#### Analysis
1. Aggregate product sales summary data.
2. Create Gold Delta tables with **Z-Ordering on productline** for BI performance.
3. Enable SQL-based ad hoc and dashboard analysis.

---

### 📊 **Business Intelligence**
> **Power BI Dashboard (future extension):**  
> Develop interactive dashboards to track:
> - Total sales trends  
> - Product line contributions  
> - Branch-level performance KPIs  
> - Payment method distributions

---

### 🔧 **Tools Used**

- **Azure Databricks** (PySpark, Spark SQL)  
- **Azure Data Lake Storage Gen2 (ADLS)**  
- **Delta Lake**  
- **Power BI (planned)**  
- **VSCode & GitHub** for version control

---

### 🏗️ **Solution Architecture**

This project follows the **Azure Databricks Modern Analytics Architecture**, implementing **Bronze, Silver, and Gold layers** to systematically refine data for business value.

<p align="center"><img src="diagrams/architecture.png" width="60%"></p>

| Layer | Description |
|---|---|
| **Bronze** | Raw data landing zone storing ingested CSV data with schema enforcement |
| **Silver** | Cleaned and transformed data with partitioning by branch for optimized querying |
| **Gold** | Aggregated product sales summary table with Z-Ordering for performance in BI tools |

---

### 🔍 **Analysis using Spark SQL**

One of the key highlights is the ability to **analyze data at each layer using Spark SQL**, enabling powerful ad hoc insights and reporting.

The [`analysis`](notebooks/03_analysis_analyze_supermarket_sales.py) notebook contains all SQL queries and transformations performed on the gold data.

---

### ✅ **Project Outcomes**

✔️ Built a **production-grade ETL pipeline** with orchestrated tasks  
✔️ Implemented **data quality validation and schema standardization**  
✔️ Partitioned and optimized data storage for cost-effective querying  
✔️ Created **analysis-ready gold tables** for seamless BI integration

---

### 🔬 **Future Enhancements**

- Integrate with **Power BI dashboards** for live business reporting  
- Enable **streaming ingestion pipelines** for real-time sales analysis  
- Implement **ML models for sales forecasting** and customer segmentation

---



### 💻 **Setup Instructions**

1. Clone the repository:

```bash
git clone https://github.com/yourusername/supermarket-sales-analytical-pipeline.git
```

2. Import notebooks into Azure Databricks workspace.

3. Update storage account names and secrets in the setup notebook.

4. Run notebooks sequentially or orchestrate them as a Databricks Job pipeline for automated execution.

