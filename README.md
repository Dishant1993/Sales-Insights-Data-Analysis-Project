# Sales-Insights-Data-Analysis-Project
Sales Insights Data Analysis Project

In this Project, I have Integrated SQL with Power BI to create an interactive Dashboard to the Sales Director of the company to help him understand the Sales number which is helping him to generate his revenue.

Problem Statement: Bhavin Patel Sales Director of Atliq Hardware he’s facing Issues for tracking sales in a dynamic growing market his team is giving him Excel file which are 69 in total from that he cant understand the sales and revenue of the organization. He wants simple insights which means he wants a simple dashboard that he can go and look at the real data. Which he can look daily on his system

Steps Performed:
1️⃣ Data Discovery
2️⃣ Data Wrangling
3️⃣ Data Cleaning
4️⃣ Data Analysis 

Tools Used: 
1️⃣ AIMS Grid: Project Planning tool
2️⃣ MYSQL
3️⃣ Microsoft Power BI

Solution: Dashboards covering sales order insights with the latest data available. The sales team will be able to make a better decision and prove 10 % cost savings of total spend. Sales Analyst stop data gathering manually to save 20% of their business time and reinvest its value-added activity.

SQL queries for data analysis

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`
