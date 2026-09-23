# 🚀 SQL Data Warehouse & Analytics Project

A modern **Data Warehouse and Analytics solution built using SQL Server**, demonstrating end-to-end data engineering and analytics practices — from raw data ingestion and ETL to dimensional modeling and business insights.

This project is designed as a **portfolio project** to demonstrate practical skills in **SQL Development, Data Engineering, ETL, Data Modeling, and Data Analytics**.

---

## 📖 Project Overview

The project builds a modern data warehouse using the **Medallion Architecture**, consisting of:

- 🥉 **Bronze Layer** – Raw data ingestion from source CSV files
- 🥈 **Silver Layer** – Data cleansing, transformation, and standardization
- 🥇 **Gold Layer** – Business-ready dimensional models for analytics

The warehouse integrates data from two source systems:

- **ERP**
- **CRM**

The final data model enables analytical reporting and helps generate insights into:

- 👥 Customer Behavior
- 📦 Product Performance
- 📈 Sales Trends

---

## 🏗️ Data Architecture

The project follows the **Medallion Architecture** approach:

```text
                    ┌───────────────────┐
                    │    Source Data    │
                    │                   │
                    │   ERP CSV Files   │
                    │   CRM CSV Files   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │   🥉 Bronze Layer │
                    │                   │
                    │    Raw Data       │
                    │    Ingestion      │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │   🥈 Silver Layer │
                    │                   │
                    │ Data Cleaning     │
                    │ Transformation    │
                    │ Standardization   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │    🥇 Gold Layer  │
                    │                   │
                    │ Fact Tables       │
                    │ Dimension Tables  │
                    │ Business Logic    │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Analytics &       │
                    │ Reporting         │
                    │                   │
                    │ Customer Insights │
                    │ Product Analysis  │
                    │ Sales Trends      │
                    └───────────────────┘
```

---

## 🎯 Project Objectives

### Data Engineering

The primary objective is to develop a modern SQL Server data warehouse that consolidates sales data from multiple source systems and prepares it for analytical reporting.

Key objectives include:

- Integrating ERP and CRM data
- Building a structured data warehouse
- Implementing ETL pipelines
- Cleaning and standardizing raw data
- Resolving data quality issues
- Creating fact and dimension tables
- Developing an analytical data model
- Documenting the warehouse architecture

### Data Analytics

The analytical layer focuses on answering business questions related to:

- Customer purchasing behavior
- Product performance
- Sales performance
- Sales trends
- Customer segmentation
- Revenue analysis

---

## 🛠️ Technologies & Tools

| Technology / Tool | Purpose |
|---|---|
| **SQL Server** | Data warehouse and database |
| **SQL** | Data transformation and analytics |
| **SSMS** | Database development and management |
| **CSV** | Source datasets |
| **Draw.io** | Data architecture and modeling |
| **Git & GitHub** | Version control and project management |
| **Notion** | Project planning and documentation |

---

## 🔄 ETL Process

The project implements an ETL workflow to move data from source systems into the analytical warehouse.

### 1. Extract

Data is extracted from:

- ERP CSV files
- CRM CSV files

The raw data is loaded without significant modification into the **Bronze Layer**.

### 2. Transform

The Silver Layer performs data transformation tasks such as:

- Removing duplicate records
- Handling missing values
- Standardizing formats
- Cleaning inconsistent values
- Resolving data quality issues
- Converting data types
- Applying business rules
- Integrating ERP and CRM information

### 3. Load

Clean and transformed data is loaded into the **Gold Layer**, which contains business-ready fact and dimension tables optimized for analytical queries.

---

## 🗂️ Data Warehouse Layers

### 🥉 Bronze Layer

The Bronze Layer stores the raw data exactly as received from the source systems.

**Characteristics:**

- Raw data
- Minimal transformation
- Source-system representation
- Used as the foundation for downstream processing

---

### 🥈 Silver Layer

The Silver Layer contains cleaned and standardized data.

**Key activities:**

- Data cleansing
- Data validation
- Standardization
- Deduplication
- Data type conversion
- Source integration

---

### 🥇 Gold Layer

The Gold Layer contains business-ready analytical data.

It includes:

- Fact tables
- Dimension tables
- Business logic
- Aggregated information where required

The Gold Layer is designed to support reporting and analytical queries efficiently.

---

## ⭐ Data Modeling

The project uses a **dimensional data model** consisting of fact and dimension tables.

### Fact Tables

Fact tables contain measurable business events such as sales transactions.

Example metrics:

- Sales Amount
- Quantity
- Price
- Order Value

### Dimension Tables

Dimension tables provide descriptive information used to analyze facts.

Examples:

- Customer
- Product
- Date

A simplified model:

```text
                 ┌─────────────────┐
                 │  Dim Customer   │
                 └────────┬────────┘
                          │
                          │
┌─────────────────┐       │       ┌─────────────────┐
│   Dim Product   │───────┼───────│    Dim Date    │
└────────┬────────┘       │       └────────┬────────┘
         │                │                │
         │                ▼                │
         │       ┌─────────────────┐       │
         └──────►│   Fact Sales    │◄──────┘
                 └─────────────────┘
```

---

## 📊 Analytics & Reporting

The project includes SQL-based analytical queries designed to provide actionable business insights.

### 👥 Customer Analysis

Example questions:

- Who are the highest-value customers?
- How frequently do customers purchase?
- What is the total revenue generated by each customer?
- Which customers contribute the most to sales?

### 📦 Product Analysis

Example questions:

- Which products generate the highest revenue?
- Which products have the highest sales volume?
- Which products are performing poorly?
- What are the most popular products?

### 📈 Sales Analysis

Example questions:

- What are the monthly sales trends?
- What is the total revenue?
- What is the average order value?
- How does sales performance change over time?
- Which periods generate the highest sales?

---

## 📁 Project Structure

```text
SQL-Data-Warehouse-Project/
│
├── datasets/
│   ├── source_erp/
│   └── source_crm/
│
├── docs/
│   ├── requirements.md
│   ├── data_catalog.md
│   ├── architecture.md
│   └── data_model.md
│
├── scripts/
│   ├── bronze/
│   │   └── load_bronze.sql
│   │
│   ├── silver/
│   │   └── transform_silver.sql
│   │
│   └── gold/
│       └── create_gold.sql
│
├── tests/
│   └── data_quality_checks.sql
│
├── analytics/
│   ├── customer_analysis.sql
│   ├── product_analysis.sql
│   └── sales_analysis.sql
│
├── diagrams/
│   ├── architecture.drawio
│   └── data_model.drawio
│
└── README.md
```

---

## 📋 Project Requirements

### Data Sources

The project uses two source systems:

```text
ERP
 │
 ├── Customer Data
 ├── Product Data
 └── Sales Data

CRM
 │
 ├── Customer Information
 └── Related Business Data
```

The datasets are provided as CSV files.

---

### Data Quality

Before analytical reporting, the data is processed to identify and resolve issues such as:

- Missing values
- Duplicate records
- Invalid values
- Inconsistent formats
- Incorrect data types
- Data inconsistencies between ERP and CRM

---

### Data Integration

ERP and CRM data are integrated into a unified analytical model.

The objective is to provide users with a **single source of truth** for sales analysis.

---

### Data Historization

The project focuses on the **latest available dataset**.

Historical tracking and Slowly Changing Dimensions are outside the current project scope.

---

## 📚 Documentation

Project documentation is available in the `docs/` directory.

Important documentation includes:

- Business requirements
- Data architecture
- Data model
- Data catalog
- ETL process
- Data quality rules
- Analytical requirements

---

## 🔗 Useful Resources & Tools

All tools used in this project are available for free.

- **SQL Server Express** – Database server
- **SQL Server Management Studio (SSMS)** – SQL development environment
- **Draw.io** – Architecture and data modeling diagrams
- **GitHub** – Version control and collaboration
- **Notion** – Project planning and documentation

---

## 💡 Skills Demonstrated

This project demonstrates practical experience in:

### SQL Development

- SELECT queries
- JOINs
- CTEs
- Subqueries
- CASE statements
- Aggregations
- Window Functions
- Stored Procedures
- Views
- Data Transformation

### Data Engineering

- ETL pipelines
- Data ingestion
- Data cleansing
- Data transformation
- Data integration
- Data warehouse architecture

### Data Modeling

- Fact tables
- Dimension tables
- Star schema
- Dimensional modeling
- Data relationships

### Data Analytics

- Customer analysis
- Product analysis
- Sales analysis
- KPI development
- Trend analysis
- Business reporting

---

## 🎓 Learning Outcomes

By completing this project, the following practical skills are demonstrated:

- Designing a modern data warehouse
- Working with SQL Server
- Building ETL pipelines
- Handling real-world data quality problems
- Integrating multiple data sources
- Creating dimensional data models
- Writing analytical SQL queries
- Generating business insights
- Documenting data architecture and models

---

## 🚀 Future Enhancements

Potential improvements for future versions include:

- 📊 Power BI dashboard
- 🔄 Automated ETL scheduling
- ☁️ Cloud data warehouse implementation
- 📈 Advanced sales forecasting
- 🤖 Predictive customer analytics
- 🔍 Automated data quality monitoring
- 📜 Historical data tracking
- ⚡ Incremental data loading
- 🏗️ CI/CD for SQL pipelines

---

## 👨‍💻 Author

**Kartik Sarwan**

Frontend Engineer → Data Analytics / Data Engineering Portfolio Project

### Core Skills

`SQL` • `SQL Server` • `ETL` • `Data Warehousing` • `Data Modeling` • `Data Analytics` • `Python` • `Tableau` • `Power BI`

---

## ⭐ Project Purpose

This repository was created as a **portfolio project** to demonstrate the complete lifecycle of a modern data warehouse — from raw source data to cleaned, integrated, modeled, and analytics-ready data.

If you find this project useful, consider ⭐ **starring the repository**.
