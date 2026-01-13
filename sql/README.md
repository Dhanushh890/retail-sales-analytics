**Database: retail_db**
**Table: orders**

**Columns:**

Order ID, Order Date, Customer Name, Category, Sub-Category,
Product Name, Sales, Profit, Quantity, Region, Month, Year

**TOTAL SALES & TOTAL PROFIT**

SELECT 
    SUM(Sales) AS Total_Sales,
    SUM(Profit) AS Total_Profit
FROM orders;

**SALES BY CATEGORY**

SELECT 
    Category,
    SUM(Sales) AS Category_Sales
FROM orders
GROUP BY Category
ORDER BY Category_Sales DESC;

**PROFIT BY CATEGORY**

SELECT 
    Category,
    SUM(Profit) AS Total_Profit
FROM orders
GROUP BY Category
ORDER BY Total_Profit DESC;

**MONTHLY SALES TREND**

SELECT 
    Month,
    SUM(Sales) AS Monthly_Sales
FROM orders
GROUP BY Month
ORDER BY Month;

**SALES BY REGION**

SELECT 
    Region,
    SUM(Sales) AS Total_Sales
FROM orders
GROUP BY Region
ORDER BY Total_Sales DESC;

**SALES AND PROFIT TOGETHER (DASHBOARD READY)**

SELECT 
    Category,
    SUM(Sales) AS Total_Sales,
    SUM(Profit) AS Total_Profit
FROM orders
GROUP BY Category;
