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
