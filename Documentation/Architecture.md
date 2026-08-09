\# 🏗 Architecture



\## 📌 Overview



The \*\*Automated KPI Reporting Dashboard\*\* follows a modular Business Intelligence architecture that separates data storage, data processing, workflow automation, and data visualization into independent layers.



This architecture improves maintainability, scalability, and performance while providing a clear end-to-end analytics workflow.



The solution integrates PostgreSQL, SQL, n8n, and Power BI to automate the generation of business KPIs from sales data.



\---



\## 🏛 Overall System Architecture



```text

&#x20;            Sales Dataset

&#x20;         (Excel / CSV Files)

&#x20;                   │

&#x20;                   ▼

&#x20;         PostgreSQL Database

&#x20;                   │

&#x20;                   ▼

&#x20;       SQL Queries \& Aggregations

&#x20;                   │

&#x20;                   ▼

&#x20;       n8n Workflow Automation

&#x20;                   │

&#x20;                   ▼

&#x20;        Power BI Data Model

&#x20;                   │

&#x20;                   ▼

&#x20;     Interactive KPI Dashboard

```



\---



\## 🗄 Database Architecture



Sales data is stored inside a PostgreSQL relational database.



The analytical model follows a \*\*Star Schema\*\*, which separates transactional data from descriptive business dimensions.



This design improves query performance, simplifies reporting, and supports scalable dashboard development.



\---



\## ⭐ Star Schema



```text

&#x20;                  dim\_customer

&#x20;                        │

&#x20;                        │

&#x20;                        │

dim\_product ───── fact\_sales ───── dim\_date

```



The \*\*fact\_sales\*\* table acts as the center of the model and is connected to all dimension tables through surrogate keys.



\---



\## 📊 Data Model



\### Fact Table



\#### `fact\_sales`



The central table containing transactional sales data.



Primary business fields include:



\- customer\_key

\- product\_key

\- date\_key

\- sales

\- quantity

\- profit



\---



\### Dimension Tables



\#### `dim\_customer`



Contains customer-related information.



Example attributes:



\- customer\_name

\- city

\- state

\- country

\- region



\---



\#### `dim\_product`



Contains product information.



Example attributes:



\- product\_name

\- category

\- sub\_category



\---



\#### `dim\_date`



Contains calendar information used for time-based analysis.



Example attributes:



\- full\_date

\- month\_name

\- month\_short\_name

\- year

\- quarter

\- week\_number



\---



\## 🔗 Table Relationships



The Power BI data model uses one-to-many (1:n) relationships.



```text

dim\_customer (1)

&#x20;       │

&#x20;       │

&#x20;       ▼

fact\_sales (N)



dim\_product (1)

&#x20;       │

&#x20;       ▼

fact\_sales (N)



dim\_date (1)

&#x20;       │

&#x20;       ▼

fact\_sales (N)

```



This structure enables efficient filtering and aggregation across all dashboard visuals.



\---



\## 🔄 Data Flow



The complete data flow consists of the following steps:



1\. Import the sales dataset.

2\. Store the data in PostgreSQL.

3\. Execute SQL queries to aggregate business data.

4\. Automate data processing through n8n.

5\. Load processed data into Power BI.

6\. Calculate KPIs using DAX.

7\. Present interactive visualizations in the dashboard.



\---



\## ⚙ n8n Workflow Architecture



The workflow is initiated manually.



After execution, multiple PostgreSQL queries run independently to retrieve the required datasets.



The workflow includes:



\- KPI Summary

\- Sales by Category

\- Sales by Region

\- Monthly Sales Trend

\- Top Products by Sales



Each query produces a dedicated dataset for a specific dashboard visualization.



\---



\## 📈 Power BI Architecture



The Power BI report consists of two report pages.



\### Page 1 – Sales Performance Dashboard



Contains:



\- KPI Cards

\- Sales by Category

\- Monthly Sales Trend

\- Regional Filter



\---



\### Page 2 – Tooltip Dashboard



Contains additional contextual information including:



\- Total Sales

\- Number of Orders

\- Average Order Value

\- Sales Trend

\- Top 3 Products



The page is configured as a report tooltip and is displayed when users hover over the category chart.



\---



\## 🛠 Technology Stack



| Layer | Technology |

|--------|------------|

| Data Source | Excel |

| Database | PostgreSQL |

| Data Processing | SQL |

| Workflow Automation | n8n |

| Data Modeling | Power BI |

| KPI Calculations | DAX |

| Documentation | Markdown |



\---



\## 🌍 Localization



The dashboard user interface has been localized into German.



Localized elements include:



\- KPI titles

\- Visual titles

\- Category names

\- Region names

\- Month names



Examples:



\- Mär

\- Mai

\- Okt

\- Dez



The technical table names, column names, and measures remain primarily in English for consistency and maintainability.



\---



\## 🚀 Future Improvements



Potential enhancements include:



\- Scheduled n8n workflows

\- Automatic data refresh

\- Power BI Service deployment

\- Automated PDF report generation

\- Email distribution of KPI reports

\- REST API integration

\- Cloud database support

\- Real-time data sources

\- Incremental data loading

\- Additional dashboard pages



\---



\## 📌 Design Principles



The architecture was designed with the following principles:



\- Separation of concerns

\- Modular components

\- Scalable data model

\- Reusable SQL logic

\- Automated workflow execution

\- Interactive business reporting



\---



\## 📄 Conclusion



The Automated KPI Reporting Dashboard demonstrates a complete Business Intelligence architecture, from data storage and SQL-based processing to workflow automation and interactive reporting.



By combining PostgreSQL, SQL, n8n, Power BI, and a Star Schema, the solution provides a scalable and maintainable foundation for automated KPI reporting and future Business Intelligence projects.

