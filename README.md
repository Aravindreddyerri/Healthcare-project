<h1>
 <b>Healthcare Analytics Pipeline: End-to-End Medallion Architecture</b>
</h1>

<b> Overview </b>


This project showcases an end-to-end healthcare analytics pipeline built on Microsoft Azure. Azure Data Factory is used to ingest raw healthcare data from GitHub into the Bronze layer in Azure Data Lake Storage (ADLS), and Databricks is used to clean, transform, and curate the data through Silver and Gold layers using PySpark. The final Gold layer is stored in Azure SQL Database, which is then connected to Power BI for reporting and dashboard creation focused on patient demographics, billing analysis, hospital utilization, and length-of-stay trends.




<h1>
  
<b> Architecture Diagram </b>

</h1>

<img width="3104" height="2140" alt="image" src="https://github.com/user-attachments/assets/ea5de2e8-5f70-43e3-b15c-597cfc0507dd" />


The data follows a structured flow from raw ingestion to reporting:
## Pipeline Architecture
This project follows a Medallion architecture approach:

1. **Data Ingestion**
   - Azure Data Factory pipeline ingests healthcare data from GitHub into the Bronze layer in ADLS.

2. **Bronze Layer**
   - Raw healthcare data is stored in Azure Data Lake Storage for traceability and ingestion history.

3. **Silver Layer**
   - Databricks notebooks clean the raw data, standardize column types, and prepare structured data for downstream use.

4. **Gold Layer**
   - Business-ready transformations and aggregations are stored in Azure SQL DB for analytics and reporting.

5. **Visualization**
   - Power BI connects to the curated Gold layer to build interactive dashboards and trend analysis reports.

<b>Key Data Transformations</b>

The pipeline performs several critical transformations to convert messy raw data into valuable insights:

Data Cleaning: Standardized column names and data types, including date parsing and handling of inconsistent categorical values.

Feature Engineering: Calculated critical metrics such as Length of Stay (LOS), age group categorization, and High-Cost Billing flags.

Aggregation: Created summary tables by hospital, insurance provider, admission type, and medical condition to support executive and clinical dashboards.


<b>Power BI Insights</b>

<img width="811" height="463" alt="Screenshot 2026-05-05 at 1 39 58 PM" src="https://github.com/user-attachments/assets/80546eb6-39b0-4597-88b1-6942b7322512" />

The dashboard provides a comprehensive view of hospital operations, including:

Demographic Analysis: Age and gender distribution by blood type.

Financial Trends: Billing insights segmented by insurance provider and hospital.

Utilization Patterns: Yearly trends in patient length of stay.

Clinical Analytics: Billing trends categorized by admission type and medical condition.


<b> Technologies Used </b> 


Data Engineering: Databricks, PySpark, Parquet, Delta Lake,Azure Data Lake Storage(ADLS Gen 2),Azure Data Factory,Azure SQL DB

Data Visualization: Power BI.

Version Control: Git/GitHub.


