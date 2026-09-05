# Sales Performance & Business Insights | Power BI

## Project Overview

This project focuses on analyzing sales performance and generating business insights using Microsoft Power BI.

The dashboard was developed using the Sample Superstore dataset to analyze sales, profitability, order volume, customer segments, product performance, regional performance, and discount patterns.

The project includes data preparation using Power Query, data modeling, DAX measures, interactive visualizations, KPI tracking, and business-focused analysis.

## Dataset

The project uses the Sample Superstore dataset, a retail sales dataset containing information about orders, customers, products, sales, quantity, discounts, and profit.

Key fields include:

* Order ID
* Order Date
* Ship Date
* Ship Mode
* Customer ID
* Customer Name
* Segment
* Region
* Category
* Sub-Category
* Product Name
* Sales
* Quantity
* Discount
* Profit

## Tools & Technologies

* Microsoft Power BI
* Power Query
* DAX
* Data Cleaning
* Data Modeling
* Data Visualization
* Business Intelligence

## Data Preparation

Power Query was used to prepare the dataset before analysis.

The following steps were performed:

* Converted Order Date and Ship Date into date format.
* Standardized data types for customer, product, sales, quantity, discount, and profit fields.
* Checked for missing values and data inconsistencies.
* Validated numerical fields for accurate analysis.
* Retained negative and zero-profit transactions because they represent actual business outcomes.
* Created a clean dataset for dashboard development.

## DAX Measures

The following DAX measures were created for the analysis:

```DAX
Total Sales = SUM('Sample - Superstore'[Sales])

Total Profit = SUM('Sample - Superstore'[Profit])

Total Orders = DISTINCTCOUNT('Sample - Superstore'[Order ID])

Total Quantity = SUM('Sample - Superstore'[Quantity])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Average Order Value =
DIVIDE([Total Sales], [Total Orders], 0)

Total Customers =
DISTINCTCOUNT('Sample - Superstore'[Customer ID])

Average Discount =
AVERAGE('Sample - Superstore'[Discount])

Profit per Order =
DIVIDE([Total Profit], [Total Orders], 0)

Profit per Customer =
DIVIDE([Total Profit], [Total Customers], 0)
```

## Dashboard 1 — Executive Sales Overview

The first dashboard provides a high-level overview of overall sales performance.

### Key Performance Indicators

* Total Sales: 2.30M
* Total Profit: 286.40K
* Total Orders: 5K
* Total Quantity: 38K
* Profit Margin: 12.47%

### Visualizations

* Monthly Sales & Profit Trend
* Sales by Category
* Sales by Region
* Top 10 Products by Sales

### Filters

Interactive slicers were added for:

* Order Date
* Category
* Region

These filters allow users to explore the dashboard dynamically.

## Dashboard 2 — Customer & Product Analysis

The second dashboard focuses on customer segments, product profitability, sub-category performance, and discount relationships.

### Visualizations

* Sales by Segment
* Profit by Segment
* Top 10 Products by Profit
* Bottom 10 Products by Profit
* Sales vs Profit by Sub-Category
* Discount vs Profit

This dashboard helps identify profitable customer segments, high-performing products, underperforming products, and potential relationships between discounting and profitability.

## Key Business Insights

* Technology is one of the key categories contributing to overall sales performance.
* Customer segments can differ significantly in both sales contribution and profitability.
* Top-performing products contribute substantially to overall revenue and profit.
* The Bottom 10 Products by Profit visual helps identify products that may require pricing, discount, or product-level review.
* Sub-category analysis highlights differences between sales volume and actual profitability.
* Discount vs Profit analysis can help identify areas where discounting may negatively affect profitability.

## Business Recommendations

* Monitor highly profitable customer segments and strengthen retention strategies.
* Review low-profit and loss-making products to identify opportunities for pricing or cost optimization.
* Evaluate discount strategies to balance sales growth with profitability.
* Use regional and category-level analysis to prioritize business opportunities.
* Track key KPIs regularly through interactive dashboards to support data-driven decision-making.

## Project Structure

```text
Power BI Project - Sales Performance/
│
├── Sales_Performance_Business_Insights.pbix
└── README.md
```

## Conclusion

This project demonstrates how Power BI can be used to transform raw retail transaction data into an interactive business intelligence solution.

Through Power Query, DAX, data modeling, and interactive visualizations, the dashboard provides insights into sales performance, profitability, customers, products, categories, regions, and discount behaviour.

The project demonstrates practical skills in data preparation, business analysis, dashboard development, KPI tracking, and communicating insights through data visualization.
