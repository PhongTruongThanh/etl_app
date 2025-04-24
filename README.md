# **Financial Data ETL Pipeline**

This project is an **ETL pipeline** designed for processing and analyzing vast amounts of **financial data** sourced from various APIs. The goal is to collect, transform, and store data to help in financial market analysis, stock price trend prediction, and sentiment analysis of market news.

---

## **Table of Contents**

1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Data Sources](#data-sources)
4. [ETL Process](#etl-process)
5. [Processing Framework](#processing-framework)
6. [Data Warehouse Design](#data-warehouse-design)
7. [Business Results & Applications](#business-results-applications)
8. [Technologies Used](#technologies-used)

---

## **Project Overview**

This **ETL pipeline** automates the extraction, transformation, and loading of data from **financial APIs** to provide valuable insights into stock prices, market sentiment, and other crucial financial metrics. The processed data is stored in a **Data Warehouse** and used for real-time analysis and business decision-making.

The project handles a vast amount of data on a daily basis, providing actionable insights such as stock price trends, sentiment analysis, and trading volumes. These insights can be used for forecasting, portfolio management, and understanding broader market trends.

![ETL Tool Diagram](https://drive.google.com/uc?export=view&id=1EUY0zTvZbqC9UaXgvM7wCJDYkx73lpgU)
---

## **Problem Statement**

The primary challenge addressed by this project is the ability to analyze and visualize large-scale financial data in real-time. Financial analysts, traders, and decision-makers need accurate and timely insights into stock market performance, news sentiment, and sector trends. This involves several problems:

- **Data Integration**: Collecting data from multiple sources with different formats.
- **Data Transformation**: Normalizing and cleaning raw data to make it usable for analysis.
- **Scalability**: Processing millions of data points efficiently.
- **Timeliness**: Ensuring data is updated and available for analysis on a daily basis.
  
This project aims to solve these problems using an efficient ETL pipeline and data storage system.

---

## **Data Sources**

The project uses data from several key APIs:

1. **sec-api.io**: 
   - Provides data on companies listed on stock exchanges such as NYSE and NASDAQ.
   - Includes company details like sector, industry, and market category.

2. **Alpha Vantage**: 
   - Market status API: Provides real-time stock market updates.
   - News sentiment API: Fetches financial news articles along with sentiment scores to gauge market mood.

3. **Polygon.io**: 
   - Offers daily OHLC (Open, High, Low, Close) data for US stocks.
   - Provides trading volume and other metrics for stock performance analysis.

---

## **ETL Process**

### **Extract**:
- Data is automatically extracted from the APIs at scheduled intervals:
  - **sec-api.io** and **Alpha Vantage (market status)**: Extracted once a month as their data does not change frequently.
  - **Alpha Vantage (news sentiment)** and **Polygon**: Extracted daily to capture real-time stock market data.

### **Transform**:
- The data is cleaned and normalized:
  - Raw financial data is merged into a common format, making it ready for analysis.
  - Sentiment scores from news articles are computed based on predefined thresholds (e.g., bullish, bearish).

### **Load**:
- Data is stored in a **PostgreSQL** or **DuckDB** database:
  - Company data is loaded into the database once a month.
  - Daily stock data (OHLC) and sentiment analysis results are loaded daily into the system.

![Taskflow Diagram](https://drive.google.com/uc?export=view&id=1aq8p1LmotMVuU_ut0hRwjN2-ti6zsAqw)
![Taskflow Diagram 2](https://drive.google.com/uc?export=view&id=15pg1rb1NzD3eoAy8KSo2lkzHDC7v43CL)
---

## **Processing Framework**

The system uses the following tools and frameworks to process and manage data:

1. **Hadoop**:
   - Deployed as a **single-node cluster** for distributed storage using **HDFS**.
   - **YARN** is used for resource management, enabling the processing of large datasets.

2. **Apache Airflow**:
   - Manages the ETL pipeline by automating the extraction, transformation, and loading of data.
   - Airflow schedules and monitors workflows, ensuring that data processing runs smoothly without manual intervention.

3. **Python & Spark**:
   - **PySpark** is used for distributed data processing.
   - Python libraries such as **Pandas** and **SQLAlchemy** handle data transformation and database management.

---

## **Data Warehouse Design**

The **Data Warehouse** is structured using a **Galaxy Schema** to support various business requirements, such as stock price trends, market sentiment, and trading volumes.

1. **Fact Tables**:
   - **Stock Prices**: Contains OHLC data, trading volume, and other stock performance metrics.
   - **Market Sentiment**: Stores sentiment scores, sentiment labels, and associated news articles.
   
2. **Dimension Tables**:
   - **Companies**: Contains company details like sector, industry, and market category.
   - **Dates**: Used for time-based analysis of stock trends.

The database is designed using the **3NF** (Third Normal Form) to ensure efficient data storage and retrieval.

![Data Warehouse Schema](https://drive.google.com/uc?export=view&id=1KbMDfFyn1_-TwIqHeS4AcU4do-hsunMD)

---

## **Business Results Applications**

The ETL pipeline helps derive the following key business insights:

1. **Stock Price Trends**:
   - Track and predict stock price movements (up, down, or stable) over various timeframes (daily, weekly, monthly).
   
2. **Market Sentiment Analysis**:
   - Monitor overall market sentiment (bullish, bearish, or neutral) based on financial news.
   - Understand how specific news events impact stock prices.

3. **Trading Volume Analysis**:
   - Identify unusual trading volumes and correlate them with price fluctuations.
   
4. **Sector Performance**:
   - Analyze the performance of different sectors in the stock market and identify potential investment opportunities.

These insights are stored in a data warehouse, allowing users to query historical data and generate reports using visualization tools like **Power BI**. 
You can view the Power BI dashboard by clicking on the following link:

[Power BI Dashboard PDF](https://drive.google.com/uc?export=download&id=1TEuUNJVXYstVPzS4_m5TEi14rsKFfls6)

---

## **Technologies Used**

- **Data Sources**: sec-api.io, Alpha Vantage, Polygon.io
- **ETL Tools**: Apache Airflow, Python, PySpark
- **Data Storage**: PostgreSQL, DuckDB
- **Big Data Framework**: Hadoop (HDFS, YARN)
- **Business Intelligence**: Power BI
- **Cloud Platform**: Google Compute Engine (GCP)

---

## **Further Documentation**

For detailed information and development documentation click on this link:  
[ETL Documentation](https://wise-bard-bd3.notion.site/ETL-Document-1acaceae7fe680ff9853c1b8e6219d0a?pvs=4)

