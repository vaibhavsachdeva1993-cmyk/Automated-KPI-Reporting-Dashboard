\# 🗄 SQL Queries



\## 📌 Overview



The \*\*Automated KPI Reporting Dashboard\*\* uses SQL queries to retrieve, aggregate, and prepare business data stored in a PostgreSQL database for visualization in \*\*Power BI Desktop\*\*.



The SQL layer performs the core analytical calculations before the data is imported into Power BI, ensuring efficient reporting while minimizing the amount of processing required within the dashboard.



All queries are executed automatically through an \*\*n8n\*\* workflow and generate the analytical datasets required for KPI cards, charts, filters, and tooltip visualizations.



\---



\## 🎯 Purpose



The SQL queries were designed to transform raw transactional sales data into meaningful analytical datasets for Business Intelligence reporting.



The primary objectives are:



\- Retrieve sales data from PostgreSQL

\- Aggregate business metrics

\- Calculate key performance indicators (KPIs)

\- Prepare optimized datasets for Power BI Desktop

\- Provide data for interactive dashboard visualizations

\- Reduce calculation complexity inside Power BI

\- Ensure consistent business logic across all reports



\---



\## 🗄 Database Tables



The SQL queries operate on a \*\*Star Schema\*\* data model consisting of one fact table and three dimension tables. This schema is optimized for analytical processing, enabling efficient aggregations and high-performance reporting.



\### Fact Table



\- `fact\_sales`



\### Dimension Tables



\- `dim\_customer`

\- `dim\_product`

\- `dim\_date`



The relationships between these tables are established using the following surrogate keys:



\- `customer\_key`

\- `product\_key`

\- `date\_key`



\---



\## 🔗 Data Model Relationships



```text

&#x20;              dim\_customer

&#x20;                    │

&#x20;                    │

dim\_product ─── fact\_sales ─── dim\_date

```



The relationships enable SQL queries to combine transactional sales data with descriptive customer, product, and calendar information, producing business-ready datasets for reporting and dashboard visualizations.



\---



\## 📊 KPI Queries



\### Total Sales



\*\*Purpose\*\*



Calculates the total revenue generated from all sales transactions.



\*\*Used for\*\*



\- KPI Card

\- Tooltip Dashboard



\---



\### Order Count



\*\*Purpose\*\*



Calculates the total number of completed sales transactions.



\*\*Used for\*\*



\- KPI Card

\- Tooltip Dashboard



\---



\### Average Order Value



\*\*Purpose\*\*



Calculates the average revenue generated per order.



\*\*Used for\*\*



\- KPI Card

\- Tooltip Dashboard



\---



\## 📈 Analytical Queries



\### Sales by Category



\*\*Purpose\*\*



Aggregates total sales by product category.



Business categories include:



\- Technology

\- Furniture

\- Office Supplies



\*\*Dashboard Visualization\*\*



\- Bar Chart



\---



\### Sales by Region



\*\*Purpose\*\*



Aggregates sales by customer region to support regional performance analysis.



\*\*Dashboard Visualization\*\*



\- Regional Analysis

\- Interactive Filters



\---



\### Monthly Sales Trend



\*\*Purpose\*\*



Calculates monthly sales totals to analyze revenue development over time.



\*\*Dashboard Visualization\*\*



\- Line Chart



\---



\### Top Products by Sales



\*\*Purpose\*\*



Identifies the highest-performing products based on total sales.



\*\*Dashboard Visualization\*\*



\- Tooltip Dashboard



\---



\## ⚙ Query Design Principles



The SQL layer was designed according to the following principles:



\- Modular query structure

\- Read-only analytical queries

\- Business-oriented aggregations

\- Reusable query logic

\- Efficient query execution

\- Clear separation of data processing and visualization

\- Maintainable and scalable query design



Each SQL query is responsible for producing a dedicated analytical dataset, making the solution easier to understand, maintain, and extend.



\---



\## 🔄 Integration with n8n



The SQL queries are executed automatically through an \*\*n8n\*\* workflow.



Workflow sequence:



1\. Manual workflow execution

2\. Connection to PostgreSQL

3\. Execution of analytical SQL queries

4\. Retrieval of aggregated datasets

5\. Import of the processed datasets into Power BI Desktop

6\. Visualization of the results in the dashboard



\---



\## 📊 Integration with Power BI



The SQL query results are imported into \*\*Power BI Desktop\*\* and used to populate individual dashboard components.



| SQL Dataset | Dashboard Component |

|--------------|---------------------|

| KPI Summary | KPI Cards |

| Sales by Category | Bar Chart |

| Sales by Region | Regional Analysis |

| Monthly Sales Trend | Line Chart |

| Top Products by Sales | Tooltip Dashboard |



This approach keeps the dashboard responsive by performing the majority of analytical processing within the database before visualization.



\---



\## 🚀 Future Improvements



Potential enhancements include:



\- Parameterized SQL queries

\- SQL Views for reusable business logic

\- Stored Procedures

\- Materialized Views

\- Incremental data loading

\- Database indexing optimization

\- Query performance optimization

\- Query execution monitoring

\- Automated workflow schedules

\- Cloud database integration



\---



\## 📌 Summary



The SQL layer forms the analytical foundation of the \*\*Automated KPI Reporting Dashboard\*\*.



Using PostgreSQL, business data is transformed into optimized analytical datasets that support KPI calculations, interactive dashboard visualizations, and business reporting.



Combined with workflow automation through \*\*n8n\*\* and visualization in \*\*Power BI Desktop\*\*, the solution provides a scalable, maintainable, and efficient Business Intelligence reporting architecture. Its modular SQL design ensures consistent business logic, simplifies maintenance, improves scalability, and provides a solid foundation for future analytical enhancements and reporting requirements.

