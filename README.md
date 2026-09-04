# MAPLEMART-RETAIL-SALES-ANALYSIS
A Power BI project analyzing a retail business. The dataset encompasses details such as products, stores, customers, employees, orders, and transaction-level sales data to uncover actionable insights into sales performance, profitability, customer behavior and store operations to improve overall business performance.

## Table of Content

•	Project Overview

•	Project Scope

•	Project Objective

•	Document Purpose

•	Use Case

•	Skills Demonstrated

•	Data Source

•	Data Profiling

•	Data Modelling

•	Data Cleaning and Processing

•	Data Analysis and Insight

•	Data Visualization

•	Recommendation

•	Conclusion

##	Project Overview
This project aims to transform MapleMart’s raw retail data into a reliable and interactive business intelligence solution using Power BI. The analysis brings together information from products, customers, stores, employees, orders, and order transactions to provide a comprehensive view of the business. The project focuses on identifying sales trends, evaluating product and category performance, measuring profitability, understanding customer purchasing patterns, comparing sales channels and store performance, and monitoring key operational indicators. Through systematic data cleaning, validation, data modelling, DAX calculations, and dashboard development, the project delivers actionable insights that can help MapleMart make data-driven decisions, improve operational efficiency, identify areas of growth, and strengthen overall financial and retail performance.

##	Project Scope
This project covers MapleMart’s retail data from January 1, 2022 to August 5, 2026 across products, stores, customers, employees, orders, and order transactions. The analysis focuses on sales trends, product and category performance, profitability, customer segments, sales channels, store performance, and operational activity, using Power BI to transform the data into actionable business insights.

## Project Objective
The objectives of this analysis are to:
-	Identify the product categories that generate the highest revenue and gross profit.
-	Evaluate sales trends over time to identify periods of growth, decline, and changing sales patterns.
-	Compare sales performance across stores and store types to identify high- and low-performing locations.
- Analyze sales channels to understand the contribution of Online, In-store, and Click & Collect transactions.
-	Examine customer age groups to identify the customer segments contributing most to sales.
-	Evaluate gross profit and gross profit margin to understand the overall profitability of the business and identify areas for improvement.
-	Analyze order status and shipping methods to gain insight into operational performance.
-	Provide management with actionable, data-driven insights that can support strategic planning, improve operational efficiency, and strengthen MapleMart's overall business performance.

##	Document Purpose
This documentation serves as a guide for project stakeholders, providing insights into the project's objectives, data sources, data analysis, visualizations, and any other relevant information.

##	Use Case
The MapleMart retail analytics project provides a centralized view of sales, profitability, customer, product, store, and operational performance. The insights generated from the analysis can support different business functions by helping stakeholders understand performance, identify opportunities, and make data-driven decisions.
- **Senior Management:**
Senior management can use the dashboard to monitor overall business performance through key indicators such as Net Sales, Gross Profit, Gross Profit Margin, and sales trends. These insights can support strategic planning, performance evaluation, and identification of areas requiring management attention.
- **Sales and Commercial Team:**
Sales teams can use the analysis to evaluate sales performance across product categories, sales channels, stores, and store types. This can help identify strong-performing areas, underperforming segments, and opportunities to improve revenue generation.
- **Marketing Team:**
The marketing team can use customer age-group and sales-channel insights to better understand purchasing patterns and identify important customer segments. These findings can support more targeted marketing campaigns, promotional strategies, and customer engagement initiatives.
- **Product and Category Managers:**
Product and category managers can analyze revenue, gross profit, and profitability across product categories to identify high-performing and low-performing products and categories. This can support decisions around product focus, pricing, promotions, and category strategy.
- **Store and Operations Managers:**
Store and operations managers can use store and store-type performance analysis to compare locations and identify differences in sales performance. Order status and shipping-method analysis can also help highlight operational patterns and areas where processes may require improvement.
- **Finance and Business Analysts:**
Finance teams and business analysts can use the financial measures within the dashboard to monitor Net Sales, Total Cost, Gross Profit, and Gross Profit Margin. These metrics provide a consistent basis for evaluating financial performance and identifying opportunities to improve profitability.

## Skills Demonstrated

-	Data Connection in Power BI
-	Data Profiling
-	Data Cleaning and Transformation in Power Query
-	Data Modelling
-	Data Analysis
-	Data Visualization

  
##	Data Source
The data used for this project is a synthetic retail dataset developed to simulate the operations of a Canadian retail business, referred to in this project as MapleMart Retail. The dataset was designed to represent a realistic retail environment containing information about products, stores, customers, employees, orders, and individual order transactions.
The source data consists of six interconnected tables: Products, Stores, Orders, Order Items, Customers, Employees. Together, these tables provide a comprehensive view of MapleMart's retail operations, from product and customer information to individual sales transactions and store-level performance.
- **Products Table**
The Products table contains master information about the products available for sale at MapleMart. This table provides descriptive information that allows sales transactions to be analyzed by product, category, brand, supplier, price, and product status. It consists of 3,200 rows and 10 columns. The Product_ID serves as the primary identifier used to connect products to the Order Items table.
- **Stores Table**
The Stores table contains information about MapleMart's retail locations. It provides the descriptive attributes required to analyze sales performance across different stores and store formats. It consists of 270 rows and 8 columns. The Store ID connects the Stores table to the Orders table.
- **Orders Table**
The Orders table contains order-level information and represents the overall customer order. It connects customers, stores, employees, dates, sales channels, payment methods, shipping methods, and order-level financial information. It consists of 40,500 rows and 13 columns. The Order ID connects the Orders table to the Order Items table. Additional date attributes were created during the transformation process, including: Order Year, Order Month, Order Day, Delivery Year, Delivery Month and Delivery Day.
- **Order Items Table**
The Order Items table is the main transaction-level table in the analytical model. While the Orders table represents an overall order, Order Items contains the individual products included within each order. For instance, one order may contain several products and therefore have several Order Item records. The Order Items table is the primary source for Net Sales, Gross Sales, Discount Amount, Total Cost, Gross Profit and Gross Profit Margin, because this table contains individual sales transactions, it forms the foundation of the financial analysis. It consists of 142,558 rows and 9 columns. 
Additional calculated fields were created for financial analysis: Calculated Gross Sales, Calculated Discount Amount, Calculated Net Sales, Calculated Total Cost
- **Customers Table**
The Customers table contains information about MapleMart's customers. It provides demographic and identifying information that can be used to understand customer segments and purchasing behaviour. It consists of 15, 500 rows and 12 columns. The Customer ID connects the Customers table to the Orders table. Age Group was created to support customer segmentation. The final groups were: Under 18,  18–24, 25–34, 35–44,  45–54, 55–64,  65+
An Age Group Sort field was also created so that the groups would appear in logical age order rather than alphabetical order.
- **Employees Table**
The Employees table contains information about employees associated with MapleMart's operations. It consists of 550 rows and 12 columns. The Employees table provides supporting information for understanding employee-related order activity and workforce characteristics. The Employee ID connects employees to orders. Employment Status was standardized into categories including: Active, Resigned, On Leave

##	Data Profiling
Data profiling in Power BI involves examining and analyzing data characteristics to understand its structure, detect patterns, identify potential issues, and spot outliers. This process supports informed decisions regarding data cleaning and transformation. Power BI offers various tools for effective data profiling, including column quality, column distribution, and column profiling features.

- Data Profile on Key Column on Order Items Table

  ![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/ORDER%20ITEMS%20GITHUB.png)

