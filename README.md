# TRENDIMART
## Project Overview
The TrendiMart Business Performance Dashboard is designed to provide a comprehensive, real-time view of key business metrics in a visually engaging and easy-to-understand format.
## Data Source
AI
## Tools used
SQL
## Data cleaning and preparation
I imported the data using the csv file and inspected it
## Objectives
1.	 Total Revenue
2.	Net Profit
3.	Total Customers
4.	Revenue per day
5.	Production Distribution
6.	Total unit sold
7.	Top Product
## Data Analysis
### 1.	 Total Revenue
```sql 
SELECT SUM(Revenue) AS TOTALREVENUE FROM [TRENDIMART -MySQL]
/* The Total Revenue of TRENDIMART is N317,100 */
```
### 2.	Net Profit
``` sql
SELECT SUM(Profit) AS NETPROFIT FROM [TRENDIMART -MySQL]
/*The NET PROFIT of the TRENDIMART is N100,000 */
```
### 3.	Total Customers
``` sql
SELECT COUNT(SN) AS TOTAL_CUSTOMERS FROM [TRENDIMART -MySQL]
/* TRENDIMART have a total of 50 Customers */
```
### 4.	Revenue per day
```sql
SELECT Date, SUM(Revenue) AS Revenue_per_day 
FROM [TRENDIMART -MySQL]
GROUP BY Date
/* These are the following revenue per day at TRENDIMART
2025-01-05	N87500, 2025-01-06	N25500, 2025-01-07	N27100, 2025-01-08	N44500,
2025-01-09	N19100, 2025-01-10	N58000, 2025-01-11	N17500, 2025-01-12	N12500,
2025-01-14	N3000, 2025-01-15	N12600, 2025-01-16	N600, 2025-01-17	N600, 
2025-01-18	N6200,2025-01-19	N600, 2025-01-20	N600, 2025-01-21	N600, 2025-01-22	N600 */
```

### 5.	Production Distribution
```sql
SELECT Product_Category, COUNT(Product_Category) as Product_Distribution
FROM [TRENDIMART -MySQL]
GROUP BY Product_Category
/* TRENDIMART Product category are as follow 
Electronics	18, Fashion	17, Groceries	15 */
```
### 6.	Total unit sold
```sql
SELECT SUM(Units_Sold) AS UNIT_SOLD FROM [TRENDIMART -MySQL]
/* The total unit sold in TRENDIMART is 1905 units of product */
```
### 7.	Top Product
```sql
SELECT TOP 5(Product_Name)
FROM [TRENDIMART -MySQL]

/* The top product is Smartphone X */
```


