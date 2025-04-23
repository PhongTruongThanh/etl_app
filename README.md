


# 📊 ETL App

## 🧠 Overview

**Final ETL App** is a fully automated end-to-end ETL system designed to collect, transform, and store financial market data from multiple APIs. It enables robust market analysis, stock trend evaluation, sentiment analytics, and industry performance tracking.

Built with modern cloud and data engineering tools such as **Google Cloud Platform (GCP)**, **Apache Airflow**, **DuckDB**, **Hadoop**, and **Spark**, this system powers business intelligence tools like **Power BI** to support strategic decision-making in financial contexts.

---

## ❓ Problem Statement & Objectives

In the financial world, real-time and reliable data is crucial for tracking market trends, investment decisions, and risk management. However, manually gathering and processing this vast amount of dynamic information is both labor-intensive and error-prone.

**Final ETL App** addresses these challenges by:

- ✅ Automatically extracting data from multiple trusted financial APIs  
- ✅ Transforming and cleaning large volumes of raw data  
- ✅ Structuring the data into an analytics-friendly warehouse format  
- ✅ Serving the data to visualization and AI tools to generate valuable insights  

---

## 📥 Input Data Sources

This project integrates four key financial APIs:

- **sec-api.io**  
  → Public company listings, financial identifiers, sector and industry classification

- **Alpha Vantage**  
  → Market Status: Global exchange statuses  
  → News Sentiment: Analyzes financial news articles and computes sentiment scores

- **Polygon.io**  
  → Daily OHLC (Open, High, Low, Close) stock prices and trading volumes

> **Volume**: ~10,000 stock rows & 500 news articles per day; ~28,000 company records per month

---

## 🏗️ Data Warehouse Architecture

- **Model**: Galaxy Schema (variant of Star Schema with multiple fact tables and shared dimensions)  
- **Storage Engine**: DuckDB – lightweight, analytical OLAP database  

### Schema Includes:

**Dimensions**:  
- `dim_companies`  
- `dim_time`  
- `dim_exchanges`  
- `dim_industries`

**Facts**:  
- `fact_ohlc`  
- `fact_sentiment`  
- `fact_volume`  
- `fact_sector_analysis`

---

## ⚙️ System Design & ETL Flow

### 1. Extraction  
- Automated via Python + Airflow DAGs  
- Scheduled fetches from APIs (daily, monthly)

### 2. Transformation  
- Cleaning and formatting with Python  
- Schema mapping and data enrichment  
- **Spark** for scalable data operations

### 3. Loading  
- Loaded into DuckDB  
- Stored in 3NF-compliant structured tables

### 4. Orchestration & Deployment  
- **Airflow** for DAG management  
- Deployed on **Google Compute Engine**  
- Remote access via **VSCode + SSH**  
- Optional raw data storage in **Hadoop HDFS**

### 5. Data Access & Visualization  
- Flask API + Gunicorn expose endpoints  
- Integrated with **Power BI** for dashboarding

---

## 📈 Business Results & Applications

Final ETL App delivers:

- 📊 Daily updated insights on stock performance and volume trends  
- 🧾 Financial news sentiment monitoring  
- 🏢 Sector-based analysis for investment decision-making  
- 🤖 Data provisioning for machine learning and BI platforms  

---

## 💻 Tech Stack

- **Programming**: Python, SQL  
- **Data Storage**: DuckDB, HDFS  
- **Processing**: Spark  
- **Scheduling**: Apache Airflow  
- **Cloud**: Google Cloud Platform (Compute Engine)  
- **Visualization**: Power BI  

---

## 👥 Who is this for?

This project is ideal for:

- Financial Analysts  
- Data Engineers  
- BI Developers  
- Quantitative Researchers  
- Organizations building data-driven investment strategies

---

# Docs link: 
https://wise-bard-bd3.notion.site/ETL-Document-1acaceae7fe680ff9853c1b8e6219d0a?pvs=4
