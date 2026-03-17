![Report Home View](report_home_view.png)

# Superstore Sales Analytics

## Project Overview
This project presents an interactive business intelligence dashboard built using Microsoft Power BI Desktop to analyze retail sales performance using the Superstore Normalized Dataset.
The objective of this project is to transform raw retail transaction data into meaningful insights that support data-driven decision making. The dashboard analyzes key business metrics including revenue, profitability, customer behavior, regional sales distribution, and product performance.
Through data modeling, DAX calculations, and interactive visualizations, the report provides stakeholders with a comprehensive view of business performance across multiple business dimensions.

## Business Problem

Retail organizations generate large volumes of transactional data across customers, products, and geographic regions. However, without proper analysis tools, it becomes difficult to extract meaningful insights that inform business strategy.

This project addresses several key business questions:

- What is the overall sales and profit performance of the company?
- Which customer segments contribute the most revenue?
- Which regions and states generate the highest profitability?
- Which product categories drive the most sales?
- How do discounts affect profit margins?

The goal of this project is to build an interactive business intelligence dashboard that enables stakeholders to explore these questions through visual analytics.

## Dataset Description
The Superstore dataset represents a fictional retail company and is structured using multiple related tables designed to simulate real-world business data.
1. **Orders**: Contains detailed transactional records including: Order ID, Order Date, Customer ID, Product ID, Quantity, Sales, Discount, Profit.
2. **Customers**:
- Contains customer information including: Customer ID, Customer Name, Customer Segment.
- Customer segments include: Consumer, Corporate, Home Office.
3. **Locations**: Contains geographic information including: City, State, Postal Code
4. **States**: Maps states to regional classifications: East, West, Central, South
5. **Products**: Contains product metadata including: Product Name, Category, Sub-Category, Pricing Code
6. **Product Pricing Tiers**: Contains pricing tier information connected to products using Pricing Code.

## Data Modeling
The dataset is structured using a normalized relational data model designed to support multidimensional business analysis.
The Orders table serves as the central fact table, containing transaction-level metrics such as sales, profit, quantity, and discounts. This table connects to several dimension tables that provide descriptive attributes for customers, products, and geographic locations.
#### Key Relationships
The following relationships were created in the data model:
- Orders --- Customers (Customer ID)
- Orders --- Products (Product ID)
- Orders --- Locations (Location ID)
- Locations --- States (State ID)
-Products --- Product Pricing Tiers (Pricing Code)
This relational structure enables analysis across multiple business dimensions including customer segments, product categories, pricing tiers, and geographic regions.

## Key Measures (DAX)
Several key performance indicators were calculated using DAX.
#### Total Sales
Total Sales = SUM(Orders[Sales])

#### Total Profit
Total Profit = SUM(Orders[Profit])

#### Order Count
Order Count = DISTINCTCOUNT(Orders[Order ID])

#### Average Discount
Average Discount = AVERAGE(Orders[Discount])

#### Customer Count
Customer Count = DISTINCTCOUNT(Customers[Customer ID])

#### Profit Margin
Profit Margin = DIVIDE([Total Profit], [Total Sales])

## Dashboard Pages
The Power BI report contains four analytical dashboards.
1. **Sales & Performance Overview**: Provides a high-level overview of overall company performance including total sales, total profit, order volume, profit margin, and sales trends over time.
2. **Customer Insights**: Analyzes customer behavior and segmentation, including top customers by revenue, customer distribution across segments, and repeat versus one-time customers.
3. **Regional & State Insights**: Examines geographic performance across regions and states, highlighting revenue distribution, profit margins, and cities with the highest order volumes.
4. **Product & Category Performance**: Evaluates product-level performance including revenue by category, best-selling products, profit margins by sub-category, and discount patterns across product categories.

## Dashboard Preview
Below are previews of the dashboards included in the report.

















