# Inventory Analytics Summary

# Objective

The objective of this project was to **optimize retail inventory decisions** by
quantifying trade-offs between service levels, working capital, and profitability.

The analysis demonstrates how data-driven inventory analytics can:

- Reduce capital locked in excess and dead stock

- Minimize lost sales due to stock-outs

- Improve service levels for high-value products

- Enhance overall cash flow and profitability



# Business Problem

Retailers face conflicting pressures:

- Overstocking increases holding costs and ties up capital

- Understocking leads to stock-outs and lost revenue

- Long lead times inflate safety stock

- High return rates erode margins

The key challenge is identifying:

- Which SKUs deserve protection

- Which SKUs should be deprioritized or liquidated

- Where inventory risk and revenue leakage occur


# Analytical Framework

## 1. Inventory Classification (ABC–XYZ)

- **ABC analysis** classified products based on cost and revenue contribution

- **XYZ analysis** measured demand variability

- Combined into a **9-box ABC–XYZ matrix**

**Outcome:**  

Clear differentiation between:

- High-value, stable-demand SKUs (AX)

- Low-value, volatile-demand SKUs (CZ)


## 2. Inventory Health & Risk

Using inventory snapshots and sales data, the following were analysed:

- Days of supply

- Inventory turnover

- Excess inventory value

- Aged inventory

- Slow-moving and dead stock

**Outcome:**  

Identification of categories and SKUs acting as **cash traps**.



## 3. Replenishment & Safety Stock

- Lead-time demand calculated

- Safety stock and reorder points derived using demand variability

- Service-level targets applied selectively

**Outcome:**  

Improved replenishment logic for high-priority products without inflating overall inventory.



## 4. Service Level & Stock-Out Analysis

- Fill rate analysed by category and ABC–XYZ class

- Stock-out days and lost sales estimated

**Outcome:**  

High-value products were found to disproportionately contribute to lost revenue when stock-outs occurred.



## 5. Cost & Profitability Analysis

- Inventory holding cost calculated at SKU and category levels

- Most profitable products identified

- Return rates analysed by category

- Supplier performance evaluated

**Outcome:**  

Profit concentration was found to be skewed toward a small subset of products,
highlighting the importance of protecting top-performing SKUs.


# Key Business Insights

- A small fraction of SKUs drive a large share of revenue and profit

- Excess and aged inventory represent significant locked working capital

- Stock-outs in high-value categories lead to outsized revenue loss

- Selective safety stock policies outperform blanket replenishment rules

- Inventory analytics can directly improve cash flow and profitability


# Impact

This project demonstrates how inventory analytics can transform inventory from
a cost center into a **strategic profit lever**, with applications across retail,
e-commerce, and supply-chain operations.
