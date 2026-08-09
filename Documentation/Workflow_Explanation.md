\# ⚙ Workflow Architecture



\## 📌 Overview



The \*\*Automated KPI Reporting Dashboard\*\* uses \*\*n8n\*\* as the workflow orchestration layer to automate the execution of SQL queries against a PostgreSQL database.



Instead of manually executing individual SQL statements, the workflow runs multiple analytical queries in parallel and prepares dedicated datasets for visualization in \*\*Power BI Desktop\*\*.



The workflow follows a modular architecture in which each PostgreSQL node is responsible for generating the analytical dataset required by a specific dashboard visualization.



\---



\## 🎯 Workflow Objective



The workflow automates the preparation of analytical business data for reporting purposes.



Its primary objectives are:



\- Execute predefined SQL queries

\- Calculate key business KPIs

\- Aggregate sales information

\- Prepare datasets for Power BI Desktop

\- Reduce manual reporting effort

\- Ensure consistent KPI calculations

\- Improve reporting efficiency through workflow automation



\---



\## 🏛 Workflow Architecture



```text

&#x20;               Manual Trigger

&#x20;                     │

&#x20;                     ▼

&#x20;         Execute Workflow Button

&#x20;                     │

&#x20;     ┌───────────────┼────────────────┐

&#x20;     │               │                │

&#x20;     ▼               ▼                ▼

&#x20;KPI Summary   Sales by Category   Sales by Region

&#x20;     │

&#x20;     ├──────────────────────────────┐

&#x20;     ▼                              ▼

Monthly Sales Trend        Top Products by Sales

```



Each PostgreSQL node executes independently and generates a dedicated analytical dataset for its associated dashboard visualization. This modular architecture improves scalability, simplifies maintenance, and enables each dashboard component to retrieve only the data required for its respective analysis.

