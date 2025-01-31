[Link to Dashboard](https://app.powerbi.com/view?r=eyJrIjoiN2Y3NjVhNDEtZmU2ZC00ZTY1LWFmMDUtN2Q3OWY2Mzg5Y2MxIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)


# AtliQ-Sales-Insights

AtliQ Hardware
- Is a company which supplies computer hardware and peripherals to many clients across India.
- The company has a head office in Delhi and regional offices throughout India.

# Why sales insights

Sales analysis is essential for several reasons:

1. **Performance Evaluation**: It helps evaluate the performance of your sales team or individual salespeople. By analyzing sales data, you can identify top performers, areas for improvement, and training needs.

2. **Identifying Trends**: Sales analysis helps in identifying trends in customer behavior, such as seasonal fluctuations, product preferences, or geographic patterns. Understanding these trends can inform marketing strategies, inventory management, and product development.

3. **Forecasting**: By analyzing past sales data, you can make more accurate forecasts for future sales. This is crucial for inventory management, production planning, and budgeting.

4. **Optimizing Pricing Strategies**: Sales analysis can reveal insights into the effectiveness of different pricing strategies. By analyzing sales data alongside pricing information, you can determine the optimal price points for your products or services.

5. **Customer Insights**: Analyzing sales data allows you to gain insights into your customers' preferences, demographics, and purchasing behavior. This information can be used to tailor marketing messages, improve customer service, and develop targeted promotional campaigns.

6. **Identifying Opportunities**: Sales analysis can uncover opportunities for growth, such as new market segments, untapped geographical areas, or potential partnerships with other businesses.

7. **Cost Management**: By analyzing sales data alongside cost data, you can assess the profitability of different products, sales channels, or customer segments. This information is valuable for optimizing resource allocation and improving overall profitability.

In summary, sales analysis is crucial for optimizing sales performance, understanding customer behavior, making informed business decisions, and driving overall business growth.

# Business Issue

The market is growing dynamically and the sales director is finding it difficult to track the sales, needing more accurate insights about the company sales, and then take the necessary decisions.

I used SQL queries in MySQL Workbench to take a look into the data and Power BI for ETL and visualizations to create the insights.

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

 Show total number of customers
       `SELECT count(*) FROM customers;`

 Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

 Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

 Show transactions where currency is US dollars

    SELECT * from transactions where currency="USD"`

 Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

 Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

 Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


# Report

# Home
![Screenshot 2024-04-27 173315](https://github.com/mallela-sridhar-reddy/AtliQ-sales-insights/assets/115725595/59545f0f-be42-497b-9cda-82e1e22145b8)

# Revenue View
![Screenshot 2024-04-27 173331](https://github.com/mallela-sridhar-reddy/AtliQ-sales-insights/assets/115725595/facdfbcc-2dff-4e67-a0ce-ecd8fa859b1e)


# Profit View
![Screenshot 2024-04-27 173414](https://github.com/mallela-sridhar-reddy/AtliQ-sales-insights/assets/115725595/25aa85a6-1649-431b-89c3-7b09890551ac)


# Performance Insights
![Screenshot 2024-04-27 173436](https://github.com/mallela-sridhar-reddy/AtliQ-sales-insights/assets/115725595/23ddd661-c36a-4a21-acdc-ce9d614f350f)
