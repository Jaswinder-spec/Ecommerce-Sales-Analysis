# Online Retail Sales Analysis

## 📌 Project Overview
This project analyzes an online retail dataset of UK-based  registered non- store to identify key sales trends, customer behavior, and growth opportunities. 
## 📂 Dataset Information
- **Source:**href="https://archive.ics.uci.edu/dataset/352/online+retail">dataset</a>
- The dataset contains transactions from a UK-based online retail store, with fields like:
- `InvoiceNo`: Unique identifier for each transaction
- `StockCode`: Product identifier
- `Description`: Product description
- `Quantity`: Quantity of the product purchased
- `InvoiceDate`: Date of purchase
- `UnitPrice`: Price per product
- `CustomerID`: Unique identifier for customers
- `Country`: Country of the customer
- ### Files Included:
- `onlineretailcleaned`: The cleaned excel dataset in CSV format.
- `onlineretail.sql`: SQL queries to create the table, clean data, and analyze customer purchase behavior.
- `README.md`: A guide for using the project and understanding the analysis.
 ## 🛠 Data Cleaning Steps in Excel 
  -Firstly I checked the missed information and understands the data like what  i need to find and what business problems can be solved by using this data and  how this online retail store is performing by  using following steps:
  - removed duplicates
  - Checked for missing values in Customer ID and Description fields.
 - Removed rows where Customer ID was missing, as it’s crucial for customer segmentation
 - Changed Invoice Date column to Date format for proper  analysis.
 - Ensured Quantity and Unit Price were in Number format for accurate calculations.
 - Added a calculated column: Total sales = [Quantity] * [UnitPrice] and separate columns also like  Year and Month 
 -- saved the file in csv format so that it can be easily processed in Sql for queries and further information
- ## SQL Queries
The `sql_queries.sql` file contains the following key operations:
1. **Data Import**:  I have  imported the `onlineretailcleaned` in csv format  from excel for easy processing into a SQL table.
2. **Data Cleaning**: Ensured valid sales transactions for accurate reporting and removed negative values.
4. **Analysis Queries**: Queries to analyze customer purchase behavior, including:
   --Total Sales Per Country--
   --Top 10 Selling Products--
   --Customer Segmentation--
   -- Monthly Revenue Trend--
   --Total Purchase Per Customer-- Helps identify high-value customers.
   --Number of orders per customer-- Shows how often customers purchase.
   -- Average Order Value -- Gives insight into spending behavior per transaction.
   --Recency, Frequency, and Monetary (RFM) Analysis--
   --A-Recency: How recently did the customer purchase?
   --This query calculates how long it's been since each customer last made a purchase.--
   --B-Frequency: How often does the customer purchase?--
   --^-This shows how often each customer places an order.
   --C-Monetary: How much has the customer spent?
   --^This shows the total spending per customer.
   -- Above A to C will show  categories of customers like high ,churning, potential customers
--High-Value Customers: Recent, frequent, and high spenders.
--Churning Customers: Customers who haven’t purchased recently.
--Potential Customers: Customers who buy frequently but with low monetary value.
   --Top-Selling Products per Customer-- Shows which products are frequently bought by customers.
   --Seasonality Analysis (Monthly/Yearly Trends)-- Helps understand when customers are more likely to make purchases.
   --Identifying Repeat Customers--Identifies loyal customers.
 

  ## How to Run
1. Import the `onlineretailcleaned.csv` into your SQL Server (or any other database system you are using).
2. Run this  file in your SQL tool (e.g., SSMS or any SQL client) to create tables and perform analysis.

## Technologies Used:
- Excel
- SSMS (SQL Server Management Studio)
- GitHub for version control

