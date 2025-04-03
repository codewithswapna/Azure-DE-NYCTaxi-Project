# 🚖 NYC Taxi — Azure Data Engineering Project  

## 👤 Author: Kamsali Swapna  

## 📌 Introduction  
In the era of big data, efficient data engineering pipelines are the backbone of insightful analytics. This project presents an end-to-end **Azure Data Engineering solution** for NYC taxi data, leveraging **Azure Data Factory, Databricks, Data Lake, PySpark, and Delta Lake**.  

### 🔹 Key Highlights:  
✔ Scalable data pipeline using **Medallion Architecture** (Bronze, Silver, Gold)  
✔ Optimized storage & analytics using **Delta Lake**  
✔ End-to-end orchestration via **Azure Data Factory**  
✔ **Power BI** integration for real-time reporting  

---

## 🎯 Learning Objectives  
✅ Understand real-time **data integration** in Azure Data Factory  
✅ Gain hands-on experience with **Databricks & PySpark** for data processing  
✅ Implement **Delta Tables (Delta Lake)** for optimized storage  
✅ Apply **Medallion Architecture** for structured data workflows  
✅ Prepare for **real-world Data Engineering interview questions**  

---

## 🛠️ Technologies Used  
| Technology       | Purpose |  
|-----------------|--------------------------------|  
| **Azure Data Factory** | Orchestrating data pipelines |  
| **Azure Data Lake** | Scalable and secure data storage |  
| **Azure Databricks** | Big data processing & analytics |  
| **PySpark** | Distributed data processing |  
| **Delta Lake** | ACID transactions & optimized storage |  
| **Power BI** | Data visualization & reporting |  

---

## 📌 Problem Statement  
The NYC taxi dataset contains **massive volumes of raw trip records** that require cleaning and processing for meaningful insights. Traditional ETL workflows face challenges like **scalability, data consistency, and real-time processing**.  

**Solution:**  
✅ Build a **scalable & efficient** data pipeline using **Azure Data Factory, Databricks, PySpark, and Delta Lake**.  
✅ Implement **Medallion Architecture** (Bronze, Silver, Gold) for structured processing.  
✅ Enable **fast processing & reliable storage** for **reporting & machine learning**.  

---

## 📊 Project Architecture  

### 🏗️ End-to-End Data Pipeline: Ingestion, Transformation & Reporting  

#### **🔹 Ingestion Layer**  
📌 **Source**: NYC Taxi API (trip records)  
📌 **Azure Data Factory**: Ingests raw data into **Azure Data Lake Gen2**  

#### **🔹 Transformation Layer (Databricks & PySpark)**  
- **Bronze Layer (Raw Data)**: Stored in **Parquet format**  
- **Silver Layer (Transformed Data)**: Cleaned & structured  
- **Gold Layer (Serving Data)**: Optimized using **Delta Lake**  

#### **🔹 Security**  
🔐 **Azure Key Vault** manages authentication & data access  

#### **🔹 Reporting Layer**  
📊 **Power BI**: Visualizing insights  

---

## 🚀 Methodologies  

### **Phase 1: Data Ingestion (Bronze Layer)**  
📥 **Raw data ingestion** from the **NYC Taxi website** using **Azure Data Factory (ADF)**.  
✅ Data stored in **Azure Data Lake Gen2 (Parquet format)**.  
✅ **Dynamic pipeline** pulls **monthly data** using API.  

### **Phase 2: Data Transformation (Silver Layer)**  
📌 **Azure Databricks & PySpark**: Cleaning & structuring data.  
📌 Secure access using **Azure Service Principal**.  

### **Phase 3: Data Modeling & Serving (Gold Layer)**  
📌 **Delta Lake** ensures **ACID transactions, versioning & time travel**.  
📌 Data is connected to **Power BI** for reporting.  

---

## ⚠️ Challenges & Solutions  

**❌ Issue:** Formatting error in month numbers during API calls.  
**🔍 Discovery:** The pipeline failed for months **10, 11, 12** due to incorrect URL formatting.  
**✅ Solution:** Introduced **If Condition** in **Azure Data Factory**:  
✔ **Months ≤ 9** → Keep **leading zero** (e.g., `01.parquet`)  
✔ **Months > 9** → Remove leading zero (e.g., `10.parquet`)  

This **dynamic logic** ensured smooth API calls for all **12 months**! 🚀  

---
