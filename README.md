# DataAnalysis_Visualization_SQL_Tableau
Data Analysis Using SQL
1. Installed MySQL on my computer
2. Import SQL database files for data analysis

SQL Queries:
1. Show all customer records:

    __SELECT * FROM customers;__
   
3. Show total number of customers:
 
    __SELECT count(*) FROM customers;__
   
5. Show transactions for Chennai Market:

    __SELECT * FROM transactions where market_code ='Mark001';__
   
7. Show transaction where currency is US:
 
    __SELECT * FROM transactions where currency='USD';__

8. Show transaction in 2020 join by date table:
 
    __SELECT transactions.*,
   date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;__

9. Show totalll revenue in year 2020:
    
    __SELECT SUM(transactions.sales_amount) FROM transaction INNER JOIN date ON
   transaction.order_date=date.date where date.year=2020 and transaction.currency='INR\R' OR
   transaction.currency ='USD\r';__

11. Show total revenue in year 2020, january month:
    
    __SELECT SUM(transactions.sales_amount)FROM transaction INNER JOIN date ON
     transaction.order_date=date.date where date.year=2020 and date.month_name='January' and
    transaction.currency='INR\R' OR transaction.currency ='USD\r';__
    
