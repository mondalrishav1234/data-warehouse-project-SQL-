# Data Warehouse and Analytics Project

Welcome to my **Data Warehouse and Analytics Project** repository! 🚀

This project demonstrates the development of a modern data warehouse and analytics solution using **SQL Server**. The project covers the complete data workflow, including data ingestion, data cleaning, transformation, data modeling, and analytical reporting.

The main goal of this project is to gain practical experience with **SQL, ETL processes, data warehousing, data modeling, and data analytics** while following industry-oriented practices.

---

## 🏗️ Data Architecture

The data architecture of this project follows the **Medallion Architecture**, consisting of three layers:

1. **Bronze Layer**: Stores raw data as received from the source systems. The source data is provided as CSV files and loaded into SQL Server without major transformations.

2. **Silver Layer**: Contains cleaned, standardized, and transformed data. Data quality issues are identified and handled in this layer.

3. **Gold Layer**: Contains business-ready data organized into a **star schema** with fact and dimension tables for reporting and analytical queries.

### Architecture Flow

**Source CSV Files → Bronze Layer → Silver Layer → Gold Layer → Analytics & Reporting**

---

## 📖 Project Overview

This project covers the following major areas:

1. **Data Architecture**
   Designing a modern data warehouse using the Bronze, Silver, and Gold layered architecture.

2. **ETL Pipelines**
   Extracting data from source files, transforming it through different processing stages, and loading it into the data warehouse.

3. **Data Modeling**
   Designing fact and dimension tables using a star schema optimized for analytical queries.

4. **Data Quality**
   Identifying and resolving issues such as missing values, inconsistent formats, duplicate records, and invalid data.

5. **Analytics & Reporting**
   Writing SQL queries to analyze customer behavior, product performance, and sales trends.

### Skills Demonstrated

* SQL Development
* Microsoft SQL Server
* ETL Processes
* Data Warehousing
* Data Cleaning
* Data Transformation
* Data Modeling
* Star Schema
* Data Analytics
* Analytical SQL Queries
* Git & GitHub
* Technical Documentation

---

## 🛠️ Tools & Technologies

The project uses the following tools and technologies:

* **Microsoft SQL Server** — Database and data warehouse platform
* **SQL Server Management Studio (SSMS)** — Database management and SQL development
* **SQL** — Data extraction, transformation, modeling, and analytics
* **CSV Files** — Source data
* **Draw.io** — Data architecture, data flow, ETL, and data model diagrams
* **Git & GitHub** — Version control and project management

---

## 🚀 Project Requirements

### Building the Data Warehouse — Data Engineering

#### Objective

Develop a modern data warehouse using **SQL Server** to consolidate sales data and provide a reliable foundation for analytical reporting and business decision-making.

#### Specifications

* **Data Sources:** Import data from two source systems, ERP and CRM, provided as CSV files.
* **Data Quality:** Identify, clean, and resolve data quality issues before the data is used for analysis.
* **Integration:** Combine data from both source systems into a unified and user-friendly analytical data model.
* **Architecture:** Implement Bronze, Silver, and Gold layers following the Medallion Architecture.
* **Data Modeling:** Build fact and dimension tables using a star schema.
* **Scope:** Focus on the latest available dataset; historical data tracking is not required.
* **Documentation:** Document the architecture, data flow, data model, and important project decisions.

---

### 📊 BI: Analytics & Reporting

#### Objective

Develop SQL-based analytical queries to generate meaningful insights into:

* **Customer Behavior**
* **Product Performance**
* **Sales Trends**

The analytical layer will help answer important business questions and demonstrate how a data warehouse can transform raw data into useful information.

---

## 📂 Repository Structure

```text
data-warehouse-project/
│
├── datasets/                           # Raw ERP and CRM datasets
│
├── docs/                               # Project documentation and diagrams
│   ├── etl.drawio                      # ETL process diagram
│   ├── data_architecture.drawio        # Data warehouse architecture
│   ├── data_catalog.md                 # Dataset and column descriptions
│   ├── data_flow.drawio                # Data flow diagram
│   ├── data_models.drawio              # Data models and star schema
│   ├── naming-conventions.md           # Naming conventions
│
├── scripts/                            # SQL scripts
│   ├── bronze/                         # Raw data loading scripts
│   ├── silver/                         # Data cleaning and transformation
│   ├── gold/                           # Analytical models and views
│
├── tests/                              # Data quality and validation tests
│
├── README.md                           # Project documentation
├── LICENSE                             # Project license
├── .gitignore                          # Git ignored files
└── requirements.txt                    # Project requirements
```

---

## 📈 Project Workflow

The project follows a structured data engineering workflow:

```text
CSV Source Data
      ↓
Data Ingestion
      ↓
Bronze Layer
      ↓
Data Cleaning & Transformation
      ↓
Silver Layer
      ↓
Data Modeling
      ↓
Gold Layer
      ↓
Analytical SQL Queries
      ↓
Business Insights
```

---

## 🎯 Project Goals

Through this project, I aim to develop practical knowledge of:

* Designing a data warehouse from raw data
* Working with Microsoft SQL Server
* Understanding ETL workflows
* Writing advanced SQL queries
* Cleaning and transforming real-world datasets
* Designing fact and dimension tables
* Understanding star schema architecture
* Performing analytical data exploration
* Building business-oriented metrics
* Documenting a complete data engineering project
* Using Git and GitHub for project version control

---

## 👨‍💻 About Me

Hi! I'm **Rishav Mondal**, a **Computer Science and Engineering undergraduate** interested in software development, data, and modern technology.

I have experience and learning exposure in **Python, SQL, C, C++, HTML, CSS, JavaScript, and web development**, and I am continuously strengthening my skills through practical projects.

This Data Warehouse project is part of my hands-on learning journey to develop stronger skills in **SQL, data engineering, data modeling, and analytics**.

### Connect With Me

* **GitHub:** [Rishav Mondal](https://github.com/mondalrishav1234)
* **LinkedIn:** [Rishav Mondal](https://www.linkedin.com/in/rishav-mondal-459520246/)

---

## 🛡️ License

This project is intended for **educational and portfolio purposes**.

The project structure and learning approach are based on the reference material used while studying data warehousing and analytics. The implementation, documentation, learning notes, and project work are being developed as part of my own learning journey.

---

