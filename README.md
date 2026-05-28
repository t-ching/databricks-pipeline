# End-to-End Big Data Architecture & MLops Pipeline

## 📌 Project Overview
This portfolio project demonstrates a unified Data Engineering and Machine Learning workflow built inside **Databricks** using the **NYC Yellow Taxi dataset**. The notebook handles raw data ingestion, multi-tier data cleaning, aggregated analysis, and model tracking via **MLflow** in a single, streamlined pipeline.

---

## 🛠️ Architecture & Data Workflow
The pipeline implements a unified **Medallion Architecture** directly inside a single Databricks notebook environment:

### 1. Data Engineering Steps
* **Bronze Layer**: Loaded raw compressed `.csv.gz` files from distributed workspace storage straight into a managed Delta Lake table.
* **Silver Layer**: Cleansed anomalies by filtering zero-passenger records, removing negative fare values, and parsing raw datetime strings into explicit numeric time features (`pickup_hour`, `pickup_day`).
* **Gold Layer**: Aggregated business metrics to find the average fare amount and trip distance grouped by peak operating hours.

### 2. Machine Learning & MLops Tracking
* Converted processed Spark DataFrames into high-quality features for scikit-learn model training.
* Deployed **MLflow** context managers to track model parameters, run environments, and performance metrics.
* **Key Model Metric Achieved**: Root Mean Squared Error (RMSE) of **3.906** using a baseline `LinearRegression` configuration.

---

## 📸 Production Screenshot (Databricks Execution)

### MLflow Experiment Metrics
<img width="277" height="191" alt="image" src="https://github.com/user-attachments/assets/9add704b-2228-4e61-ba66-ac472051c88b" />

### Delta Table Audit History
<img width="983" height="155" alt="image" src="https://github.com/user-attachments/assets/f8776b25-a9a0-4ca1-8812-42b7b1a912e5" />

---

## 📂 Repository Structure
* `NYC Taxi.ipynb` - Unified notebook script containing ingestion, cleansing, BI, and ML steps.
* `README.md` - Technical project documentation and performance metrics.

---

## 🚀 Key Skills Demonstrated
* **Big Data Transformation**: Distributed dataframe querying using PySpark API wrappers.
* **Data Warehousing Patterns**: Multi-tier data reliability design patterns via Delta Lake.
* **MLops Implementation**: Reproducible training management via lifecycle tool tracking (MLflow).


