# Data Model

# Overview

This project uses a **star schema–based analytical data model** designed to support
inventory optimization, service-level management, and profitability analysis for a
retail business.

The model separates **transactional fact tables** (sales, inventory, returns) from
**descriptive dimension tables** (products, customers, time, geography, people),
enabling scalable SQL analytics and reliable BI reporting.


# Fact Tables

## fact_orders

**Grain:** One row per order line (order × product × date)

**Purpose:**

- Sales and demand aggregation

- Revenue and profit analysis

- Input for ABC classification

**Key Metrics:**

- Sales

- Quantity

- Profit

- Discount


## fact_inventory_snapshot

**Grain:** One row per product per snapshot date *(synthetically derived)*

**Purpose:**

- Inventory availability tracking

- Days of supply and turnover analysis

- Excess, aged, slow-moving, and dead stock identification

- Holding cost estimation

- Stock-out and lost sales estimation

**Key Metrics:**

- Estimated on-hand inventory

- Days of supply

- Inventory turnover

- Holding cost

- Stock-out days

- Lost sales (proxy)


## fact_returns

**Grain:** One row per returned order line

**Purpose:**

- Return rate analysis

- Revenue leakage identification

- Category-level quality and supply risk


# Dimension Tables

## dim_products

- Product ID

- Category and sub-category

- Cost and pricing attributes

**Used for:**  

ABC–XYZ classification, SKU prioritisation, profitability analysis



## dim_customers

- Customer ID

- Segment

**Used for:**  

Demand aggregation and profitability context


## dim_date

- Day, month, quarter, year attributes

- Weekday and seasonality flags


**Used for:**  

Trend analysis, inventory ageing, turnover calculations



## dim_geography

- Region, state, city

**Used for:**  

Regional inventory and service-level analysis


## dim_people

- Sales representatives and regional mapping

**Used for:**  

Operational accountability and performance reporting



# Relationships

- All dimensions connect to fact tables via **one-to-many relationships**

- No many-to-many joins

- Referential integrity enforced during data preparation

This ensures accurate aggregation, prevents double counting, and supports
complex analytical queries.


# Analytical Outputs Layer

Using SQL aggregations and window functions, the following analytical outputs were
derived from the core data model:

- ABC analysis (by cost and revenue)

- XYZ demand variability analysis

- ABC–XYZ 9-box inventory classification

- Days of supply and inventory turnover

- Excess, aged, slow-moving, and dead stock valuation

- Safety stock and reorder point calculation

- Fill rate and service-level analysis

- Stock-out days and lost sales estimation

- Inventory holding cost (SKU and category level)

- Supplier performance scorecard

These outputs form the foundation of the Power BI dashboards and strategic insights.



# Assumptions

- Inventory levels and stock-outs were **estimated** due to the absence of explicit
  inventory snapshots in the source data

- Industry benchmarks (e.g., 25% annual holding cost) were applied consistently

- All assumptions were documented and applied uniformly across analyses

This reflects real-world retail analytics environments where perfect data is rare.
