# SQL-DATA-WAREHOURSE-PROJECT
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

## 🎯 Objectives

- Centralize disparate data into a unified warehouse.
- Design a star/snowflake schema using dimensional modeling.
- Build and automate ETL processes using SQL Server Integration Services (SSIS) or T-SQL.
- Provide clean, structured data for reporting in tools like Power BI or Excel.

## 🏗️ Architecture

- **Data Sources**: Flat files, Excel sheets, CRM, ERP systems
- **ETL Tool**: T-SQL Scripts and/or SQL Server Integration Services (SSIS)
- **Database**: SQL Server 2019 (or your version)
- **Reporting Tool**: Power BI (or Excel / SSRS)

## 🧱 Schema Design

A typical **star schema** is implemented with one or more fact tables and related dimension tables.

Example Schema:

Fact_Sales
├── SaleID (PK)
├── ProductID (FK)
├── CustomerID (FK)
├── DateKey (FK)
├── Quantity
├── TotalAmount

Dim_Product
├── ProductID (PK)
├── ProductName
├── Category
├── Brand

Dim_Customer
├── CustomerID (PK)
├── FullName
├── Region
├── Segment


## ⚙️ ETL Process

ETL is managed using:
- T-SQL stored procedures and scripts
- Optionally, SSIS packages for scheduled workflows

### ETL Stages:
1. **Extract**: Raw data pulled into staging tables.
2. **Transform**: Cleansing, type casting, surrogate key generation.
3. **Load**: Load into dimension and fact tables.

Example T-SQL snippet:
```sql
-- Load data from staging to Dim_Product
INSERT INTO Dim_Product (ProductID, ProductName, Category, Brand)
SELECT DISTINCT ProductID, ProductName, Category, Brand
FROM Staging_Products;```


##👤 About Me:
Hi, I'm Sibusiso, a passionate data professional with a strong background in Mathematical Sciences and experience in data analysis, data warehousing, and business intelligence. I enjoy designing efficient data systems that provide meaningful insights and empower organizations to make data-driven decisions.

##🔧 Skills & Tools:
SQL Server (T-SQL, SSIS)

Power BI

Excel for analytics

Dimensional modeling

ETL pipelines and data validation

Python (for data scripting and automation)

Feel free to connect with me on LinkedIn or reach out via email!

📌 Future Improvements
Automate daily ETL with SSIS or SQL Agent

Implement Slowly Changing Dimensions (SCD)

Add data lineage and audit logging

Use views or stored procedures for BI semantic layer


