# Supply Chain Management using Azure Databricks

This project focuses on optimizing supply chain operations by analyzing large-scale data from multiple sources and providing actionable insights through interactive dashboards. It is built entirely on **Azure** cloud services, leveraging **Azure Data Factory**, **Azure Databricks**, and **Azure Data Lake Storage (ADLS)**.  
Data processing and transformations are implemented using **PySpark** and **Spark SQL** within Databricks notebooks, following a robust **Medallion Architecture (Bronze–Silver–Gold)** to ensure data quality and consistency across all stages.

---

## 🎥 Project Demo

[Watch the demo video on Google Drive](https://drive.google.com/file/d/1EXMnPEq3ECIJe3sxeN4NYe1KJfKFNnHS/view?usp=sharing)

> If the above link doesn’t render as a preview, you can also copy the link into your browser to view.

---

## Project Overview

-  **Data Source**: Ingested quarterly (every 3 months) via **Azure Data Factory (ADF)** using event-triggered pipelines.
-  **Storage**: Leveraging **Medallion Architecture** with Bronze, Silver, and Gold layers using Azure Data Lake Storage (ADLS).
-  **Processing**: Data cleaning, transformation, and feature engineering using **Pyspark** in **Databricks**.
-  **Analysis**: Final dashboards built on top of **Gold Layer** datasets using **Databricks Dashboards**.
-  **Version Control**: Code is maintained and tracked via **GitHub** for collaboration and safety.

---

## Tech Stack

- **Azure Data Factory (ADF)** – Data ingestion and scheduling
- **Azure Databricks** – Data engineering, processing, and dashboarding
- **Azure Data Lake Storage (ADLS)** – Data storage using Medallion Architecture (Bronze, Silver, Gold)
- **GitHub** – Version control and CI/CD (optional)
- **Spark SQL / PySpark** – Data transformations and feature engineering

---

## Data Architecture: Medallion Pattern

1. **Bronze Layer**  
   Raw data ingested from source and saved as external tables.
   
2. **Silver Layer**  
   Cleaned and feature-engineered datasets using Databricks notebooks.
   
3. **Gold Layer**  
   Aggregated and analytical datasets prepared for dashboards and reporting.

---

## Pipeline Flow

1. **Data Ingestion**  
   - Triggered quarterly using ADF
   - Data loaded into the Bronze layer (ADLS)

2. **Processing & Feature Engineering**  
   - External tables created in Databricks
   - Data cleaned, transformed, and saved to Silver

3. **Aggregation & Reporting**  
   - Aggregations performed for business KPIs
   - Saved to Gold layer and visualized through dashboards

---

## Dashboards

- Real-time metrics on delivery route optimization
- Customer-level order fulfillment insights
- Warehouse-to-customer distance visualizations

> Built using Databricks Dashboard features connected to Gold layer datasets.

---

## Scheduling

- **Event-based triggers** used in ADF to automate ingestion.
- Pipelines designed for seamless quarterly updates without manual intervention.

---

## Project Structure 

/notebooks

├── ingestion/  
├── cleaning/  
├── feature_engineering/  
├── aggregation/  
└── dashboard/
