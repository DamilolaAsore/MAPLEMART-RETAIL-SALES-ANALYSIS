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

### Data Profile on Key Column on Order Items Table
  ![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/ORDERS%20ITEMS%20TABLE.png)

#### Basic Information
-	Table Name: Order Items Table
- Number of Rows: 142,558 
-	Number of Key Column: 8

| Column Name | Data Type | Distinct Value | Unique Value | % Valid Value | % Error Value | % Empty Value | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Order Item ID | Text | 106,972 | 106,972 | 100% | 0% | 0% | ITEM_0000122 | ITEM-O141557 |
| Order ID | Text | 984 | 968 | 100% | 0% | 0% | ORD-2026-000022 | ORD-2026-040000 |
| Product ID | Text | 29 | 1 | 100% | 0% | 0% | MAP-PROD-000096 | MAP-PROD-040000 |
| Quantity | Whole Number | 5 | 0 | 100% | 0% | 0% | 1 | 5 |
| Unit Price | Decimal Number | 3,304 | 351 | 100% | 0% | 0% | 6.685 | 3090.97 |
| Unit Cost | Decimal Number | 2,929 | 7 | 100% | 0% | 0% | 8.15 | 1799.97 |
| Discount Price | Percentage | 4 | 0 | 100% | 0% | 0% | 5 | 20 |
| Line Total | Decimal Number | 48,079 | 16,981 | 100% | 0% | 0% | 6.35 | 33527.07 |

#### Data Quality Checks 
#### Missing Values: 
-	Order Items ID: 0
-	Quantity: 0
-	Order ID: 0
-	Product ID: 0
-	Units: 0
-	Unit Price: 0
-	Unit Cost: 0
-	Line Total: 0

### Data Profile on Key Column on Product Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/PRODUCTS%20TABLE.png)

#### Basic Information
-	Table Name: Product Table
-	Number of Rows: 476
-	Number of Key Columns: 10
  
| Column Name | Data Type | Distinct Value | Unique Value | % Valid Value | % Error Value | % Empty Value | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Product ID | Text | 476 | 476 | 100% | 0% | 0% | MAP-PROD-000001 | MAP-PROD-002985 |
| Product Name | Text | 476 | 476 | 100% | 0% | 0% | Acer 4K Smart TV | Wilson Yoga Mat |
| Category | Text | 5 | 0 | 100% | 0% | 0% | Electronics | Sports & Outdoors |
| Sub Category | Text | 64 | 0 | 100% | 0% | 0% | 4K Smart TV | Yoga Mat |
| Brand | Text | 36 | 0 | 100% | 0% | 0% | ACER | WILSON |
| Unit Cost | Decimal Number | 475 | 474 | 100% | 0% | 0% | 8.15 | 1799.31 |
| Unit Price | Decimal Number | 466 | 465 | 100% | 0% | 0% | 447.59 | 1827.19 |
| Suppliers | Text | 12 | 0 | 100% | 0% | 0% | ATLANTIC DISTRIBUTION | WESTERN CANADA WHOLESALE |
| Product Status | Text | 4 | 0 | 100% | 0% | 0% | ACTIVE | SEASONAL |
| Stock | Whole Number | 438 | 416 | 100% | 0% | 0% | 0 | 4974 |
#### Data Quality Checks
#### Missing Values:
-	Product ID: 0
-	Product Name: 0
-	Unit Price: 0
-	Unit Cost: 0
-	Stock: 0
-	Product Status: 0
-	Brand: 0
-	Category:0
-	Sub Category: 0
-	Suppliers: 0

### Data Profile on Key Column on Orders Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/ORDERS%20TABLE.png)

#### Basic Information
-	Table Name: Orders Table
-	Number of Rows: 36.414
-	Number of Key Columns: 13
| Column Name | Data Type | Distinct Value | Unique Value | % Valid Value | % Error Value | % Empty Value | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Order ID | Text | 36,414 | 36,414 | 100% | 0% | 0% | ORD-2026-000001 | ORD-2026-040000 |
| Customer ID | Text | 13,627 | 3,304 | 100% | 0% | 0% | CAN-CUS-000001 | CAN-CUS-015000 |
| Store ID | Text | 250 | 0 | 100% | 0% | 0% | MAP-STR-0001 | MAP-STR-0250 |
| Employee ID | Text | 394 | 0 | 100% | 0% | 0% | MAP-EMP-00001 | MAP-EMP-00802 |
| Order Date | Date | 1,461 | 0 | 100% | 0% | 0% | 06/08/2022 | 05/08/2026 |
| Delivery Date | Date | 1,470 | 0 | 100% | 0% | 0% | 07/08/2022 | 15/08/2026 |
| Order Status | Text | 5 | 0 | 100% | 0% | 0% | CANCELLED | SHIPPED |
| Sales Channel | Text | 3 | 0 | 100% | 0% | 0% | CLICK & COLLECT | IN-STORE |
| Shipping Method | Text | 5 | 0 | 100% | 0% | 0% | UPS | STORE PICKUP |
| Payment Method | Text | 6 | 0 | 100% | 0% | 0% | APPLE PAY | PAYPAL |
| Discount Percentage | Percentage | 6 | 0 | 100% | 0% | 0% | 0 | 25 |
| Shipping Cost | Decimal Number | 2,922 | 283 | 100% | 0% | 0% | 0 | 34.45 |
| Tax Amount | Decimal Number | 7,817 | 358 | 100% | 0% | 0% | 2.89 | 72.49 |
| Order Total | Decimal Number | 33,883 | 31,483 | 100% | 0% | 0% | 20.01 | 2499.81 |

#### Data Quality Checks
#### Missing Values:
-	Order ID: 0
-	Store ID: 0
-	Employee ID: 0
-	Customer ID: 0
-	Order Date: 0
-	Delivery Date: 0
-	Payment Method: 0
-	Order Total: 0
-	Sales Channel:0
-	Shipping Method:0
-	Tax Amount: 0
-	Discount Percentage:0
-	Shipping Cost:0

### Data Profile on Key Column on Customer Table
![](

