# PROJECT-CAPSTONE-SALES-DATA

# Project Title: SALES PERFORMANCE ANALYSIS FOR A RETAIL STORE

## Table of contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparations](#data-cleaning-and-preparations)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Data Visualization](#data-visualization)
- [Results/Findings](#resultsfindings)
- [Recommendations](#recommendations)


### Project Overview
---
This project aims to provide explore sales data to uncover key trend such as; top-selling products, monthly sales trends and regional performance. Utilizing pivot tables, Excel formulas, SQL queries, and Power BI dashboards, this analysis provided actionable insights to optimize sales strategies and gain deeper understanding of the Retail store's performance.

### Data Sources 
---
The primary source dataset used here is "LITA Capstone Dataset_27027859 XLSX Worksheet (.xlsx)" and this is a source that was provided for by the Incubator Hub Data Analysis Instructors. The Dataset consists of 50,001 customer records with 8 variables, including OrderID, CustomerID, Product, Region,Orderdate, Quantity, UnitPrice. A duplicates of 41,214 was removed.

 ### Tools Used
 - Miscrosoft Excel [Download here](https://microsoft.com)
   1. Data Cleaning
   2. Formulas( Calculate metrics)
   3. Analysis(Pivot Table)
   4. Visualization(Graph)
- SQL- Structured Query Language
   1. Running Queries
   2. Validating queries
- PowerBI
   1. Creating Dahsboard for visualizations for interactive Presentations
- Github for Portofolio Building

### Data Cleaning and Preparations
---
We performed the forllowing tasks at this stage for the Data cleaning and Preparation;
   1. Data Loading and inspection
   2. Removal of Duplicates
   3. Dta Formatting
   4. Handling missing values
   5. checking column quality
   6. Tranform Data

### Exploratory Data Analysis
---
This involves the expoloring of the Data to examine and summarise the data to understand. The following questions were asked;
- percentage sales by month of the current year?
- what is the Highest sales by product, month and Region?
- Ranked products by total sales?
- What is the Average Sales per month,region and Product?
- Examined regional sales performance

![CAPSTONE PROJECT SALES DATA SQL](https://github.com/user-attachments/assets/2788c476-50d9-407a-b0ab-03a53a696587)


### Data Analysis
-----
Some interesting code/formulas worked with are;
- Formulas in Excel were used to calculate metrics such as average sales per product.
```EXCEL
=AVERAGEIF(C2:C50001,C2,H2:H50001)
```
![CAPSTONE PROJECT SALES DATA EXCEL](https://github.com/user-attachments/assets/1b551e25-f344-4ed7-bfa5-60038ec812ff)

- Pivot tables were used to analyse subscription patterns and identifying key segments.

![CAPSTONE PROJECT SALES DATA PIVOT TABLE](https://github.com/user-attachments/assets/58a7c8de-d2b2-4c3f-9001-d167b56cf8ae)

- SQL queries were used to validate data and investigate specific trends;
```SQL
select
      YEAR(OrderDate) AS SalesYear,
	  MONTH(OrderDate) AS SalesMonth,
	  SUM(SalesAmount) AS TotalSales

From
     [dbo].[SALESDATACAPSTONE]
Where
     Year(OrderDate) = YEAR(GETDATE())-----Filter from the current year
Group by
       YEAR(OrderDate),
	   MONTH(OrderDate)
Order by
        SalesYear,
		SalesMonth;
```

### Data Visualization
---
- PowerBI was used to create interactive dashboards and visualize key findings.
![CAPSTONE PROJECT SALES DATA VISUAL](https://github.com/user-attachments/assets/7c380e84-fe48-49ef-a31e-0bc540b2e4a3)

### Results/Findings
---
The summaries Results/findings are as follows;
1. The South Region made the highest sales in the region.
2. Top-selling Products: Shoes (35% of total sales), Shirts (25%), and Hats (20%) drove the 
    majority of sales.
3. Sales peaked during winter months (December, January, February) with a 25% increase in sales of 
   Jackets, Gloves, and Hats.

### Recommendations
---
Baseed on the analysis we recommend the following actions;
- Conduct quarterly inventory reviews to ensure optimal stock levels.
- Focus on expanding and promoting produts in other Regions for wider reach.
- Target marketing efforts in high-performing regions. 
- Enhance customer satisfaction through optimized inventory and promotions; Offer discounts on 
  slow-moving products and run seasonal promotions 

- 
