🚀 Walmart Sales Data Analysis - SQL Insights
This project dives into the Walmart sales data from Kaggle using SQL to uncover key insights, trends, and metrics. The queries help derive actionable business intelligence, supporting decision-making processes.

📋 Project Overview
In this analysis, SQL is utilized to answer critical business questions, such as:

How do sales trends vary across different stores?
Which products are the top performers in various categories?
Seasonal patterns and their impact on revenue.
How effective are promotions and discounts in boosting sales?
Correlations between sales and holiday seasons.
🔍 Key SQL Queries
1. Sales by Store and Date Range
Identify which stores are performing the best during specific time periods.

sql
Copy code
SELECT store, SUM(sales) AS total_sales
FROM walmart_sales
WHERE date BETWEEN '2023-01-01' AND '2023-06-30'
GROUP BY store
ORDER BY total_sales DESC;
2. Top-Selling Products Across All Stores
This query finds the most popular products based on total units sold.

sql
Copy code
SELECT product, SUM(quantity) AS total_quantity
FROM walmart_sales
GROUP BY product
ORDER BY total_quantity DESC;
3. Monthly Sales Trend Analysis
Observe how sales are distributed over each month to detect seasonality.

sql
Copy code
SELECT EXTRACT(MONTH FROM date) AS month, SUM(sales) AS monthly_sales
FROM walmart_sales
GROUP BY month
ORDER BY month;
4. Impact of Promotions on Sales
Check if sales significantly increased during promotional events.

sql
Copy code
SELECT date, promotion, SUM(sales) AS total_sales
FROM walmart_sales
GROUP BY date, promotion
ORDER BY total_sales DESC;
🛠️ Tools & Technologies
SQL Database: PostgreSQL / MySQL / SQLite
Dataset: Walmart Sales Data from Kaggle
Code Editor: SQL Workbench / DBeaver / MySQL Workbench
💡 Insights and Findings
Store X consistently outperformed others during holiday seasons, indicating effective marketing strategies.
Product Y was the top seller across multiple stores, regardless of season.
Sales peaked during promotions but dropped sharply post-event, suggesting limited customer retention.
Winter months showed the highest revenues, aligning with holiday shopping trends.
🧑‍💻 How to Use
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/walmart-sales-analysis.git
Import the dataset into your SQL environment.
Run the provided SQL queries to reproduce the analysis and customize as needed.
🤝 Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to enhance the project.

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.

📧 Contact
For questions, feel free to reach out at:
Email: rrohanmj@gmail.com
GitHub: your-Rohanp2398

