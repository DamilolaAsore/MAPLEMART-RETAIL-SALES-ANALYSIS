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

| Column Name | Data Type | Distinct Value | Unique Value |  Valid Value% | Error Value% |  Empty Value% | Minimum | Maximum |
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

### Data Profile on Key Column on Products Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/PRODUCTS%20TABLE.png)

#### Basic Information
-	Table Name: Products Table
-	Number of Rows: 476
-	Number of Key Columns: 10
  
| Column Name | Data Type | Distinct Value | Unique Value | Valid Value% | Error Value% | Empty Value% | Minimum | Maximum |
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
-	Category: 0
-	Sub Category: 0
-	Suppliers: 0

### Data Profile on Key Column on Orders Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/ORDERS%20TABLE.png)

#### Basic Information
-	Table Name: Orders Table
-	Number of Rows: 36.414
-	Number of Key Columns: 13
  
| Column Name | Data Type | Distinct Value | Unique Value | Valid Value% |  Error Value% |  Empty Value% | Minimum | Maximum |
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
-	Sales Channel: 0
-	Shipping Method: 0
-	Tax Amount: 0
-	Discount Percentage: 0
-	Shipping Cost: 0

### Data Profile on Key Column on Customers Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/CUSTOMERS%20TABLE.png)

#### Basic Information
-	Table Name: Customers Table
-	Number of Rows: 15,000
-	Number of Key Columns: 11

| Column Name | Data Type | Distinct Value | Unique Value | Valid Value% | Error Value% |  Empty Value% | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Customer ID | Text | 14,712 | 14,712 | 100% | 0% | 0% | CAN-CUS-000001 | CAN-CUS-015000 |
| Customer First Name | Text | 676 | 31 | 100% | 0% | 0% | AARON | ZOE |
| Customer last Name | Text | 999 | 20 | 100% | 0% | 0% | ABBOTT | ZUNIGA |
| Gender | Text | 2 | 0 | 100% | 0% | 0% | FEMALE | MALE |
| Date of birth | Date | 10,217 | 6,737 | 100% | 0% | 0% | 07/08/1956 | 03/08/2008 |
| Cities | Text | 25 | 0 | 100% | 0% | 0% | BRANDON | WINNIPEG |
| States | Text | 10 | 0 | 100% | 0% | 0% | ALBERTA | SASKATCHEWAN |
| Registration Date | Date | 1,826 | 5 | 100% | 0% | 0% | 05/08/2021 | 05/08/2026 |
| Loyalty Level | Text | 5 | 0 | 100% | 0% | 0% | DIAMOND | STANDARD |
| Age | Whole Number | 53 | 0 | 100% | 0% | 0% | 18 | 70 |
| Full Name | Text | 13,414 | 12,406 | 100% | 0% | 0% | AARON BRAY | ZOE YANG |

#### Data Quality Checks
#### Missing Values:
-	Customer ID: 0
-	Customer First Name: 0
-	Customer Last Name: 0
-	Gender: 0
-	Date of Birth: 0
-	Cities: 0
-	States: 0
-	Registration Date: 0
-	Loyalty Level: 0
-	Age: 0
-	Full Name: 0

### Data Profile on Key Column on Employees Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/EMPLOYEES%20TABLE.png)

#### Basic Information
-	Table Name: Employees Table
-	Number of Rows: 519
-	Number of Key Columns: 14

| Column Name | Data Type | Distinct Value | Unique Value | Valid Value% | Error Value% | Empty Value% | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Employee ID | Text | 519 | 519 | 100% | 0% | 0% | MAP-EMP-00002 | MAP-EMP-00803 |
| Employee First Name | Text | 257 | 151 | 100% | 0% | 0% | AARON | YOLANDA |
| Employee last Name | Text | 317 | 210 | 100% | 0% | 0% | ADAMS | ZUNIGA |
| Employee Full Name | Text | 517 | 515 | 100% | 0% | 0% | AARON | YOLANDA |
| Date of birth | Date | 513 | 507 | 100% | 0% | 0% | 27/08/1966 | 19/07/2008 |
| Gender | Text | 2 | 0 | 100% | 0% | 0% | FEMALE | MALE |
| Job Title | Text | 8 | 0 | 100% | 0% | 0% | ASSISTANT MANAGER | WAREHOUSE ASSOCIATE |
| Department | Text | 5 | 0 | 100% | 0% | 0% | CUSTOMER SERVICE | SALES |
| Employment Type | Text | 3 | 0 | 100% | 0% | 0% | CONTRACT | PART-TIME |
| Salary | Decimal Number | 519 | 519 | 100% | 0% | 0% | 38214.98 | 129929.84 |
| Hire Date | Date | 504 | 489 | 100% | 0% | 0% | 20/08/2006 | 21/03/2023 |
| Store ID | Text | 228 | 62 | 100% | 0% | 0% | MAP-STR-0001 | MAP-STR-0250 |
| Employment Status | Text | 3 | 0 | 100% | 0% | 0% | RESIGNED | ACTIVE |
| Age | Whole Number | 43 | 0 | 100% | 0% | 0% | 18 | 60 |

#### Data Quality Checks
#### Missing Values:
-	Employee ID: 0
-	Employee First Name: 0
-	Employee Last Name: 0
-	Gender: 0
-	Date of Birth: 0
-	Employment Status: 0
-	Store ID: 0
-	Hire Date: 0
-	Salary:0
-	Age: 0
- Full Name: 0
-	Employment Type: 0
-	Job Title: 0
-	Department: 0

### Data Profile on Key Column on Stores Table
![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/MAPLEMART%20GITHUB%20IMAGES/STORES%20TABLE.png)

#### Basic Information
-	Table Name: Stores Table
-	Number of Rows: 222
-	Number of Key Columns: 8

| Column Name | Data Type | Distinct Value | Unique Value |  Valid Value% | Error Value% |  Empty Value% | Minimum | Maximum |
|---|---|---:|---:|---:|---:|---:|---|---|
| Store ID | Text | 222 | 222 | 100% | 0% | 0% | MAP-STR-0001 | MAP-STR-0250 |
| Store Name | Text | 25 | 0 | 100% | 0% | 0% | MAPLEMART BRANDON | MAPLEMART WINNIPEG |
| Store Type | Text | 5 | 0 | 100% | 0% | 0% | WAREHOUSE | SUPERSTORE |
| Province | Text | 10 | 0 | 100% | 0% | 0% | ALBERTA | SASKATCHEWAN |
| City | Text | 25 | 0 | 100% | 0% | 0% | BRANDON | WINNIPEG |
| Opening Date | Date | 221 | 220 | 100% | 0% | 0% | 29/09/2006 | 07/06/2025 |
| Manager Name | Text | 204 | 203 | 100% | 0% | 0% | ABIGAIL MONTGOMERY | ZACHARY ROBINSON |
| Store Status | Text | 2 | 0 | 100% | 0% | 0% | ACTIVE | CLOSED |

#### Data Quality Checks
#### Missing Values:
-	Store ID: 0
-	Store Name: 0
-	Manager Name: 0
-	Store Status: 0
-	Opening Date: 0
-	Province: 0
-	City: 0
-	Store Type: 0

##	Data Modelling
Data modelling in Power BI involves organizing and structuring data to establish meaningful relationships between various tables. A well-designed data model is crucial for creating accurate and insightful reports.

![](https://github.com/DamilolaAsore/MAPLEMART-RETAIL-SALES-ANALYSIS/blob/main/DATA%20MODELLING.png)

Active relationships were established between tables using common fields (keys), and the relationships diagram was reviewed to ensure that all connections were correctly defined. In Power BI, an active relationship serves as the default link between tables, which is used for filtering and calculations. When a relationship is created between two tables, Power BI automatically assumes it to be active unless specified otherwise. Active relationships are typically used for most calculations and visualizations.


##	Data Cleaning and Processing
The retail sales dataset was prepared for analysis and dashboard development in Microsoft Power BI. The dataset consists of six related tables:
1.	PRODUCTS
2.	STORES
3.	ORDERS
4.	ORDER_ITEMS
5.	CUSTOMERS
6.	EMPLOYEES
   
The objective of the cleaning process was to improve the accuracy, consistency, completeness, and reliability of the data before data modelling, DAX calculations, analysis, and dashboard development.
The cleaning process was performed primarily in Power Query within Power BI.

**1.	PRODUCTS**

The Products table was checked for:
-	Missing Product IDs
-	Duplicate Product IDs
-	Missing Product Names
-	Placeholder values
-	Invalid selling prices
-	Negative numerical values
-	Stock outliers
-	Inconsistent category/subcategory values
-	Blank values
  
Product IDs were reviewed to ensure that they could function as the unique identifier for products.
Product names containing missing or placeholder values were investigated rather than being automatically treated as valid product names.
Numerical fields such as Unit Cost, Selling Price and Stock were checked for inappropriate negative values and unreasonable values.
The category and subcategory fields were standardized to improve consistency during analysis.

**2.	STORES**

The Stores table was checked for:
-	Duplicate Store IDs
-	Missing Store IDs
-	Missing store names
-	Inconsistent store types
-	Invalid dates
-	Missing province/city information
-	Inconsistent Store Status values
  
Store IDs were retained as the unique identifier used to connect the Stores table with transactional data.

**3.	ORDERS**

##### ORDERS — Duplicate Order ID Cleaning

Duplicate Order IDs were identified in the Orders table.
The duplicate records were not necessarily exact duplicates because some duplicate Order IDs contained different information.
Therefore, simply removing identical rows was not sufficient.
The Orders table was:
1.	Sorted by Order ID in ascending order.
2.	Sorted by Delivery Date in descending order.
3.	Duplicate Order IDs were then removed.
   
This approach retained the record with the latest Delivery Date for each duplicated Order ID.
The purpose was to maintain one order-level record per Order ID while retaining the most recent delivery information.

 ##### ORDERS — Date Cleaning
 
The Order Date and Delivery Date fields were checked for:
-	Blank values
-	Null values
-	Invalid dates
-	Inconsistent date formats
-	Dates that could not support year/month/day analysis
  
Rows containing unusable date information were removed where the missing date prevented reliable time-based analysis.
This was particularly important because the dashboard required analysis by:
- Year
-	Month
-	Day
-	Monthly trends
-	Year-over-year performance
  
After cleaning, additional date-related fields were created, including:
-	Order Year
-	Order Month
-	Order Day
-	Delivery Year
-	Delivery Month
-	Delivery Day
  
These fields supported time-based analysis in Power BI.

##### ORDERS — Sales Channel Cleaning

The Sales Channel field originally contained values such as:
-	Click & Collect
- In-Store
-	Online
  
These values were standardized to ensure that the same sales channel was represented consistently throughout the dataset.
The standardized terminology was selected to make the dashboard easier for business users to understand.

##### ORDERS — Shipping Method Cleaning

Shipping methods were reviewed and standardized.
The dataset contained methods including:
-	Canada Post
-	FedEx
-	Purolator
-	Store Pickup
-	UPS
  
These were retained as valid shipping methods because they represent different delivery/logistics options.
Store Pickup was treated as a legitimate fulfilment method rather than a conventional courier service.

##### ORDERS — Payment Method Cleaning

Payment methods were reviewed for consistency.
Payment methods included options such as:
-	Credit Card
-	Debit Card
-	Google Pay
-	Apple Pay
  
The values were retained because they represent legitimate payment channels.
Credit Card and Debit Card were treated as separate payment methods because they represent different financial instruments and may be useful for payment-method analysis.

 ##### ORDERS — Discount Percentage Cleaning
 
The Discount Percentage field was checked for:
-	Negative values
-	Values above the logical maximum
-	Blank values
-	Invalid percentages
  
Negative discount percentages were identified and removed because a discount cannot logically be negative.
Values exceeding the logical percentage range were also investigated and treated as invalid rather than being accepted as genuine discounts.

This cleaning was important because Discount Percentage is used in the calculation of:
Gross Sales → Discount Amount → Net Sales
Invalid discount values could therefore distort revenue and profitability calculations.

##### ORDERS — Shipping Cost Cleaning

The Shipping Cost field was checked for negative values.
Negative shipping costs were identified.
Because shipping cost represents an expense incurred for fulfilment, negative values were considered invalid for the analysis.
The invalid negative values were removed during the cleaning process.

##### ORDERS — Tax Amount Validation

The Tax Amount field was checked for missing values and invalid numerical values.
No significant blank-value issue was identified in this field during the cleaning process.
The field was retained for financial analysis.

##### ORDERS — Order Total Validation

The Order Total field was examined for:
-	Negative values
-	Extremely large values
-	Blank values
-	Potential outliers
  
Negative Order Total values were identified and treated as invalid for the primary sales analysis.
Large values were investigated as potential outliers rather than automatically deleted solely because they were large.
This distinction was important because a large transaction can be legitimate in a retail dataset.

**4.	ORDER_ITEMS**

##### ORDER_ITEMS — Duplicate Cleaning

Duplicate Order Item records were identified during validation.
Duplicate records were investigated to distinguish between:
- Exact duplicates
-	Legitimate repeated products within different transactions
- Records associated with the same order
-	Records that represented genuinely duplicated transactional rows
  
Records identified as duplicates were removed where they represented redundant records.
The purpose was to prevent the same transaction from being counted more than once in revenue, quantity, cost, and profit calculations.

 ##### ORDER_ITEMS — Missing Order IDs
 
Order IDs in the Order Items table were compared with Order IDs in the Orders table.
This validation was necessary because every order item should normally correspond to an existing order.
Records with Order IDs that could not be matched to the Orders table were identified as unmatched/invalid transactional records.
These records were reviewed during the cleaning process so that unmatched transactions would not incorrectly contribute to the sales model.

##### ORDER_ITEMS — Product ID Validation

Product IDs in Order Items were compared against Product IDs in the Products table.
This validation was performed to identify transactional records referring to products that did not exist in the Products dimension.
This is an important referential-integrity check because Product ID is used to connect transaction-level sales with product attributes such as:
-	Product Name
-	Category
-	Subcategory
-	Brand
-	Product Status
-	Unit Price
  
Unmatched Product IDs were identified and addressed during cleaning.

##### ORDER_ITEMS — Quantity Validation
The Quantity field was reviewed for:

-	Blank values
-	Zero values
-	Negative quantities
-	Unusually large quantities
  
Negative quantities were treated as invalid for normal sales transactions unless specifically representing a return transaction.
The Returned field was considered when interpreting transaction records.

##### ORDER_ITEMS — Unit Price Validation

Unit Price was validated against Unit Cost and expected selling-price ranges.
An IQR-based outlier analysis was performed.
The calculated values included approximately:
-	Q1 = 216.23
-	Q3 = 661.16
-	IQR = 444.93
-	Upper Bound = 1,328.56
  
Values above the statistical upper bound were treated as potential outliers.
However, an outlier was not automatically considered an error. The purpose of this analysis was to identify records requiring investigation.

##### ORDER_ITEMS — Unit Price vs Unit Cost Validation

Unit Price was compared with Unit Cost to identify transactions where products were apparently sold below cost.
The validation produced approximately:

-	45,425 records below cost
-	80,399 records classified as above cost
  
This check was performed because selling below cost can have a significant effect on profitability.
The results were treated as a validation finding rather than automatically deleting all below-cost transactions, because below-cost sales can sometimes occur legitimately due to promotions, clearance sales, discounts, or other commercial decisions.

 ##### ORDER_ITEMS — Discount Percentage Cleaning
 
The Discount Percentage field was checked for invalid values.
Negative discount values were identified and removed.
This ensured that item-level discount calculations would not produce misleading results.

 ##### ORDER_ITEMS — Line Total Validation
 
The Line Total field was validated using the transactional components:
-	Quantity
-	Unit Price
-	Discount Percentage
  
The expected relationship was conceptually:
Gross Line Sales = Quantity × Unit Price
Discount Amount = Gross Line Sales × Discount Percentage
Net Line Sales = Gross Line Sales − Discount Amount
This validation helped confirm whether the transaction-level sales figures were mathematically reasonable.

**5.	CUSTOMERS**

##### CUSTOMERS — Duplicate Cleaning

Duplicate Customer records were identified and removed where they represented duplicate customer records.
Customer ID was treated as the principal identifier for customer-level analysis.
This prevented customers from being counted multiple times in customer-related analysis.

##### CUSTOMERS — Name 
First Name and Last Name fields were standardized.
A combined customer name was created from the first and last names where appropriate.

##### CUSTOMERS — Gender Cleaning

The Gender field was reviewed for inconsistent representations.
Values were standardized so that the same gender category would not appear under multiple spellings or formats.

##### CUSTOMERS — Age and Date of Birth Validation

Age was checked against Date of Birth.
Invalid age values were identified, including:

-	Negative ages
-	Zero values where inappropriate
-	Blank ages
-	Extremely high ages
  
Values such as 150 and 200 were identified as unrealistic for the intended customer analysis.
Date of Birth was used as the more reliable basis for age-related analysis where appropriate.
An Age Group field was created to make customer segmentation easier.

**6.	EMPLOYEES**
   
###### EMPLOYEES — Name Validation

The Full Name field was checked for missing values.
Approximately 20 records contained 0 instead of a valid employee name.
These values were treated as invalid placeholders rather than legitimate employee names.

##### EMPLOYEES — Age Validation

Employee Age was calculated/validated using Date of Birth.
An Age Group field was created to support employee demographic analysis.
This reduced reliance on potentially inconsistent manually entered age values.

##### EMPLOYEES — Salary Cleaning

Salary was checked for:
- Negative values
- Zero values
-	Blank values
-	Extreme outliers
  
An unusually high salary value of 999,999 was identified.
An IQR analysis identified approximately 9 records containing this extreme value.
Because this value appeared repeatedly and was far outside the normal salary distribution, it was treated as a data-quality outlier and reviewed accordingly.

 ##### EMPLOYEES — Hiring Date Validation
 
Hiring Date was checked against the current/project timeline.
Approximately 19 future hiring dates were identified.
Future hiring dates were treated as invalid because an employee cannot have a hiring date occurring after the relevant reporting period unless the dataset explicitly represents future hires.

 ##### EMPLOYMENT STATUS Cleaning
 
Employment Status values were reviewed and standardized.
The main valid categories included:
-	Active
-	Resigned
-	On Leave
  
Standardization ensured that employees could be reliably grouped according to their current employment status.

##### Missing and Blank Values
Blank and null values were systematically investigated across the six tables.
The decision for each blank depended on the business meaning of the column.
Not every blank was automatically replaced with zero or a text value.
For example:
•	Missing identifiers can compromise relationships.
•	Missing dates can compromise time-series analysis.
•	Missing numerical values can distort financial calculations.
•	Missing descriptive values may sometimes be acceptable.
Where a record could not be reliably used for the intended analysis because of critical missing information, it was removed.

Data Type Standardization
Data types were reviewed in Power Query.
Fields were assigned appropriate data types, including:
•	IDs → Text
•	Names → Text
•	Categories → Text
•	Dates → Date
•	Quantity → Whole Number
•	Stock → Whole Number
•	Prices → Decimal Number
•	Costs → Decimal Number
•	Percentages → Decimal Number
•	Boolean/return indicators → Appropriate logical/text type
Correct data types were essential for accurate Power BI calculations and visualizations.

 Outlier Detection
Outlier analysis was performed on important numerical fields.
The purpose was not to delete every unusual value.
Instead, outlier detection was used to distinguish between:
1.	Genuine extreme business transactions
2.	Data-entry errors
3.	Placeholder values
4.	Statistically unusual but potentially valid observations
The IQR method was used for selected fields, including Unit Price and Salary.

 Financial Validation
Financial fields were cross-checked to ensure that the sales model was mathematically consistent.
The major components included:
Gross Sales
Quantity × Unit Price
Discount Amount
Gross Sales × Discount Percentage
Net Sales
Gross Sales − Discount Amount
Total Cost
Quantity × Unit Cost
Gross Profit
Net Sales − Total Cost
Gross Profit Margin
Gross Profit ÷ Net Sales
These calculations formed the foundation of the financial KPIs used in the Power BI dashboard.

Final Data Validation
After cleaning, the dataset was reviewed again to confirm:
•	Duplicate records had been addressed.
•	Invalid negative values had been removed.
•	Critical blank values had been addressed.
•	Invalid dates had been removed.
•	Data types were correct.
•	IDs were suitable for relationships.
•	Transaction records could be linked to the relevant dimension tables.
•	Financial calculations produced reasonable results.
•	Time-based analysis worked correctly.
•	The data was suitable for Power BI modelling.

 Why the Cleaning Process Was Necessary
The cleaning process was necessary because unclean data could produce:
•	Incorrect revenue
•	Incorrect costs
•	Incorrect profit
•	Incorrect product rankings
•	Incorrect store performance
•	Incorrect customer counts
•	Incorrect employee analysis
•	Incorrect monthly trends
•	Incorrect yearly comparisons
•	Broken relationships
•	Duplicate transaction counts
•	Misleading dashboard KPIs
The objective was therefore not simply to make the dataset "look clean," but to ensure that the data was analytically reliable.

 Key Cleaning Decisions
The major decisions made during the project were:
1.	Duplicate transaction records were investigated before removal.
2.	Duplicate Order IDs were resolved by retaining the record with the latest Delivery Date.
3.	Invalid negative financial values were removed where they were logically impossible.
4.	Unrealistic demographic values were identified and corrected/removed.
5.	Future employee hiring dates were identified as invalid.
6.	Extreme numerical values were investigated using outlier analysis.
7.	Product and Order Item IDs were checked for referential integrity.
8.	Missing dates that prevented reliable time analysis were removed.
9.	Sales channels, shipping methods, payment methods, and categorical fields were standardized.
10.	Financial calculations were validated using Quantity, Unit Price, Unit Cost, and Discount Percentage.
11.	Blank-year records were investigated when they caused discrepancies between KPIs and trend visuals.
12.	The cleaned dataset was prepared for Power BI data modelling and dashboard development.

 Data Quality Principles Applied
The cleaning process followed five major data-quality principles:
Accuracy
Values were checked to ensure they represented reasonable business information.
Completeness
Missing and blank values were identified and addressed.
Consistency
Categories, dates, identifiers, and text fields were standardized.
Validity
Values were checked against logical and business rules.
Integrity
Relationships between transactional and reference tables were validated.

Final Outcome
The six-table retail dataset was transformed from a raw dataset into a structured analytical dataset suitable for Power BI.
The cleaned data provided a reliable foundation for:
•	Data modelling
•	Relationship creation
•	DAX calculations
•	Sales analysis
•	Product performance analysis
•	Store performance analysis
•	Customer analysis
•	Employee analysis
•	Profitability analysis
•	Time-series analysis
•	KPI development
•	Interactive dashboard development
The cleaning stage was therefore completed before proceeding to the modelling and visualization stages.






