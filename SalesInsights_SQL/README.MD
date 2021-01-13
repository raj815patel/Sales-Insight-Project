## Sales Insights Data Analysis Project 
-Data being used from db_dump.sql 
### Data Analysis using SQL commands 
1. Show all customer records 

`SELECT * FROM sales.customers;`

2. Show total amount of customers

`SELECT COUNT(*) FROM sales.customers`

3. Show all transactions for Mumbhai market, market code for Mumbhai is Mark002

`SELECT * FROM sales.transactions 
WHERE market_code = 'Mark002`

4. Show unique product codes sold in Chennai 

`SELECT distinct product_code 
FROM sales.transactions 
where market_code='Mark001'`

5. Show all transactions where currency is US dollars 

`SELECT * FROM sales.transactions
WHERE currency = 'USD'`

6. Show transactions in 2020, JOIN by date table 

`SELECT sales.transactions.*, sales.date.*
FROM sales.transactions 
INNER JOIN sales.date 
ON sales.transactions.order_date = sales.date.date 
WHERE year = '2020'`

7. Show total revenue in the year 2020

`SELECT SUM(sales.transactions.sales_amount)
FROM sales.transactions 
INNER JOIN sales.date 
ON sales.transactions.order_date = sales.date.date 
WHERE year = '2020'`

8. Show total revenue in the year 2020, in the month April 

`SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="April" and (transactions.currency="INR\r" or transactions.currency="USD\r")`

9. Show total revenue in the year 2020 in Chennai 

`SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001"`

10. 
