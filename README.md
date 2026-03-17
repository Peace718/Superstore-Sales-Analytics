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

#### Orders
Contains detailed transactional records including: Order ID, Order Date, Customer ID, Product ID, Quantity, Sales, Discount, Profit.

#### Customers
- Contains customer information including: Customer ID, Customer Name, Customer Segment.
- Customer segments include: Consumer, Corporate, Home Office.

#### Locations
Contains geographic information including: City, State, Postal Code

#### States
Maps states to regional classifications: East, West, Central, South

#### Products
Contains product metadata including: Product Name, Category, Sub-Category, Pricing Code

#### Product Pricing Tiers
Contains pricing tier information connected to products using Pricing Code.

## Data Modeling
The dataset is structured using a normalized relational data model designed to support multidimensional business analysis.
The Orders table serves as the central fact table, containing transaction-level metrics such as sales, profit, quantity, and discounts. This table connects to several dimension tables that provide descriptive attributes for customers, products, and geographic locations.
#### Key Relationships
The following relationships were created in the data model:
- Orders → Customers (Customer ID)
- Orders → Products (Product ID)
- Orders → Locations (Location ID)
- Locations → States (State ID)
-Products → Product Pricing Tiers (Pricing Code)
This relational structure enables analysis across multiple business dimensions including customer segments, product categories, pricing tiers, and geographic regions.

## Key Measures (DAX)
Several key performance indicators were calculated using DAX.











