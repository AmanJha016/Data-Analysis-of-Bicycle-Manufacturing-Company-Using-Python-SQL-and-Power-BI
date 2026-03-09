# Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-Power-BI

## Overview

This project goes through the Production and Inventory Analysis of the Microsoft AdventureWorks Database. Adventure Works is a fictional bicycle manufacturing company, this database contains standard transactions data from an Enterprise Resource Planning System. It contains data from the following scenarios of the company: Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Admin. 
This analysis focuses on the Manufacturing and Inventory part of the data. Microsoft Power BI has been used to create an interactive dashboard while pulling data from SQL Server.

## Data Source

[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Data Model

Defining an effective data structure in a dashboard is important, incorporating a star schema model gives an efficient design and makes the data refresh faster. The image below shows the tables used in the process:-

<img width="620" height="435" alt="DataModel" src="https://github.com/user-attachments/assets/85923f34-d211-4956-99a7-f64bc8c36cde" />

### Tables used in the model: -

- Production Location - Has Production assembly data, 1.e. Parts used to manufacture each product are defined here with an assembly location category
- Production Product - Data related to products, their physical details, price, etc.
- Production ProductCategory - Products and their defined categories
- Production ProductSubcategory - Products and their subcategories
- Production ProductInventory - Inventory data of the produced products
- Production ScrapReason - Waste Data related to manufacturing
- Production WorkOrder - Production transactions and related data
- Production WorkOrderRouting - Production work order scheduling data and details
- Sales SalesOrderDetail - Transactional Sales Data

## Built With

•[Python](https://www.python.org/)
•[Power BI](https://powerbi.microsoft.com/en-us/)
•[SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

## Analysis

### Main Page

This dashboard analyses manufacturing and inventory operations, the dashboard is made to have an app-like navigational interface. The main page includes leads to two areas namely Production Overview and Inventory Overview. Each then breakdown details and KPIs on their own page afterward.

<img width="937" height="525" alt="Main Page" src="https://github.com/user-attachments/assets/b5bef511-38cb-4f6d-8f9c-3c3d3e7ca642" />


### Production Overview

<img width="935" height="527" alt="Production Overview Page" src="https://github.com/user-attachments/assets/aa55637f-f1f3-402f-be33-9a6d717bde23" />


The dashboard is made according to the fiscal year terms, a custom date table was created using DAX, to automatically generate Fiscal year segregations. An assumption is made that the fiscal year starts on October 1st and ends on September 30th.  

This page gives information about the manufacturing overview of the company, Measures were created in Power BI in order to have custom KPIs. All the charts and KPIs are described below: -

<img width="1757" height="423" alt="Production Overview KPI" src="https://github.com/user-attachments/assets/82013f1d-b434-4ac8-aa45-899e38a1f01a" />


### Charts on the page

* Cumulative Multiline chart showing Production totals helps compare the fiscal year production trends and helps remove bottlenecks in manufacturing. *

![Cumulative_Monthly_totals_by_fiscal_year](https://github.com/user-attachments/assets/fe083849-bea0-475d-ae82-a4213c35d862)


* Donut Chart showing Actual cost distribution over different parts of the assembly line. Helps determine which parts cost more and where improvement is needed so that production costs are reduced. *

![Actual Cost of production by Assembly location](https://github.com/user-attachments/assets/4b63dc0f-a3d7-46a6-8bee-a18f64f04cb3)


* Waste cost by year line chart. A simple chart showing how much money is the company wasting on discarded products and what is the trend. *

![Waste cost by the Year](https://github.com/user-attachments/assets/46b6eb58-38b7-4c58-ad05-5a626f6a6654)


### Category Analysis

After looking at the overview of the manufacturing department, one can navigate to the Product Category Page for a more detailed analysis. Which will help identify specific issues in the manufacturing system. 

This section consists of 4 charts that show an in-depth analysis of the Production components and help determine specific issues.

<img width="934" height="520" alt="Production Category Analysis" src="https://github.com/user-attachments/assets/8e4f0a01-3ed3-4c79-a144-245745073a73" />


*Pareto Charts*

A Pareto chart is a Bar graph, the length of the chart represents frequency or cost, the longest bars are arranged on the left and the shortest to the right which amplifies the importance of the category with the highest bar. A line overlaps over the bar graph showing the percent contribution of the specific bar chart towards the total and the line accumulates the percent showing how many categories are important and consume most of the process. There are 2 Pareto Charts on this page, first is for the components required to manufacture a bike showing where most of the production is occupied and the other one is for the finished bike products showing categories of bikes produced.

![Pareto_Charts](https://github.com/user-attachments/assets/6a0d8b7c-5370-4416-969d-2aa604e06a7c)


*Waste Cost - Product Matrix Visual*

The Matrix visual shows the reason where exactly the waste is costing money to the company and due to which reasons. The first column provides the reason for waste, while the other two columns are divided into two categories Bikes (Actual bikes wasted in production) and Components (Components of bikes wasted in production). The Cost is conditionally formatted showing which portion is costing more and the reason for it. There are subtotals on rows and columns and grand total for total waste money.

![Waste_Cost_Matrix](https://github.com/user-attachments/assets/d2cc37c2-ef9a-436e-b1a5-8e0bd16e3b3e)


*Bar chart*

A simple bar chart showing how many Product categories are produced on time.

![On_time_production_by_category](https://github.com/user-attachments/assets/b6f3739a-df61-4e4f-bfec-a963ddff8024)


### Inventory Overview

Another major component of the dashboard is the Inventory overview, although there is no data regarding the distribution supply chain in the database this analysis is done assuming the is one location.

Main Page

The overview includes 3 KPI's, 3 Filters to slice the data, and 2 charts.

<img width="935" height="521" alt="Inventory data overview" src="https://github.com/user-attachments/assets/c80c8e4b-ca79-4c8f-a1b3-bc8850ba2f33" />


*KPIs*
<img width="1862" height="202" alt="Inventory Overview KPI" src="https://github.com/user-attachments/assets/ac3c546f-2492-4b22-93ca-1f57ab9b0752" />


*Area Charts*

Area charts showing how much Inventory quantity and Inventory value does the company hold by the Assembly location category are shown in the area chart. This shows which part of the manufacturing is holding most of the money and if the company is making the right choices of investing in those parts. There is a button on top of the chart so the end-user can choose if he wants to view the quantity or value on the chart.

*Inventory Turnover Multiline chart*

Comparing inventory turnover on different fiscal years can show important data. It can help show the trends in previous years of how the inventory has been used and can help plan the production process in a better way.

![Inventory_tunrover_chart](https://github.com/user-attachments/assets/4b1e308a-07e1-4673-9ff5-762c666edab8)

