# 🚀 Azure Data Factory End-to-End Data Pipeline

## 📌 Overview

This project demonstrates an end-to-end data pipeline built using **Azure Data Factory**, integrating on-premises data with cloud storage in a scalable and production-like architecture.

The pipeline extracts data from a **SQL Server (on-premises)** and loads it into **Azure Data Lake Storage Gen2** in **Parquet format**, following modern data engineering practices.

---

## 🏗️ Architecture

```
SQL Server (On-Premises)
        ↓
Self-hosted Integration Runtime (SHIR)
        ↓
Azure Data Factory (ADF)
        ↓
Azure Data Lake Storage Gen2 (ADLS)
        ↓
Parquet Files (Optimized for Analytics)
```

---

## ⚙️ Technologies Used

* Azure Data Factory (ADF)
* Azure Data Lake Storage Gen2 (ADLS)
* SQL Server Express
* Self-hosted Integration Runtime (SHIR)
* GitHub (Version Control)
* Parquet File Format

---

## 🔄 Pipeline Description

The pipeline performs the following steps:

1. Connects to an on-premises SQL Server database using SHIR
2. Extracts data from a relational table (`address_table`)
3. Transforms data format into **Parquet**
4. Loads the data into Azure Data Lake Storage Gen2

---

## 📂 Project Structure (GitHub)

```
.
├── pipeline/
├── dataset/
├── linkedService/
├── integrationRuntime/
└── adf_publish/
```

* `main branch` → Development (ADF objects in JSON)
* `adf_publish branch` → ARM templates for deployment

---

## 🔐 Security & Configuration

* Credentials managed via Azure (Key Vault / secure inputs)
* SQL Authentication enabled
* Storage account configured for Data Lake Gen2

---

## ⚠️ Challenges & Solutions

### 1. SQL Server Connection Issue

* Problem: Unable to connect from ADF to local SQL Server
* Solution: Configured **Self-hosted Integration Runtime (SHIR)**

---

### 2. ADLS Gen2 Connection Error

* Problem: `EndpointUnsupportedAccountFeatures`
* Solution: Disabled **Soft Delete for Blobs**

---

### 3. Parquet Execution Failure

* Problem: Missing Java Runtime (JRE)
* Solution: Installed Java and configured environment variables

---

## ✅ Results

* Successful data ingestion from on-prem SQL Server
* Data stored in optimized **Parquet format**
* Fully automated pipeline via Azure Data Factory
* Version-controlled infrastructure using GitHub

---

## 📊 Future Improvements

* Parameterized pipelines (dynamic tables and paths)
* Trigger-based execution (scheduled pipelines)
* CI/CD integration with GitHub Actions or Azure DevOps
* Data quality validation layer
* Integration with Azure Synapse / Databricks

---

## 👨‍💻 Author

Wellington Martins
Data Engineer | Data Analyst

---

## 📬 Contact

* LinkedIn: https://www.linkedin.com/in/wellingtonmartinsdata/
* GitHub: https://github.com/WellingtonMartinsSantos

---

## ⭐ Project Value

This project simulates a real-world data engineering scenario, including:

* Hybrid data integration (on-prem → cloud)
* Data lake ingestion
* Performance-oriented storage (Parquet)
* Version control and deployment practices

---

**Feel free to fork, contribute, or reach out!**

