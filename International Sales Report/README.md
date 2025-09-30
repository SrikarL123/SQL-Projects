

# International Sales Analysis – Advanced SQL Project

## **Project Overview**

This project analyzes an **International Sales dataset** to extract actionable business insights using **advanced SQL queries**.
The dataset contains sales transactions with the following columns:

**Index | Order date | Shipping date | Customer | Style | SKU | Size | Quantity | Rate | Gross AMT**

The analysis focuses on **customer behavior, product performance, and revenue insights**, showcasing SQL skills like **aggregation, ranking, segmentation, subqueries, and calculated metrics**.

---

## **Dataset Details**

* **Order date:** Date when the order was placed
* **Shipping date:** Date-Month when the order was shipped
* **Customer:** Customer name
* **Style / SKU / Size:** Product identifiers
* **Quantity:** Number of units sold
* **Rate:** Unit price
* **Gross AMT:** Total revenue from the order (`Quantity × Rate`)

---

## **Key Performance Indicators (KPIs)**

### **Customer Analysis**

1. **Top Customers by Total Revenue**

   * Identifies the highest-spending customers.
   * SQL concepts: `SUM`, `GROUP BY`, `ORDER BY DESC`.
   * **Image:** `Top Customers by Revenue.png`

2. **Top Customers by Most Frequent SKU**

   * Shows which products are repeatedly purchased by top customers.
   * SQL concepts: `COUNT`, `GROUP BY`, `ORDER BY`.
   * **Image:** `Top Customers by Most Frequent_SKU.png`

3. **Customer Segmentation by Order Quantity**

   * Segments customers into High / Medium / Low value categories based on total revenue.
   * SQL concepts: `CASE` statements, `SUM`, `GROUP BY`.
   * **Image:** `Customer_Segmentation.png`

---

### **Product Analysis**

4. **Best-Selling Products (SKU / Style)**

   * Finds top-selling products by quantity and revenue.
   * SQL concepts: `SUM`, `GROUP BY`, `ORDER BY`.
   * **Image:** `Best-Selling Products.png`

5. **Quantity vs Revenue Efficiency**

   * Highlights products with the highest revenue per unit sold.
   * SQL concepts: `SUM`, calculated columns, `GROUP BY`.
   * **Image:** `Quantity vs Revenue Efficiency.png`

6. **SKU / Style Contribution to Revenue**

   * Shows top products contributing the most to total revenue as a percentage of overall sales.
   * SQL concepts: subqueries, `SUM`, calculated percentages.
   * **Image:** `SKU Style Contribution to Revenue.png`

---

## **Insights**

* The project identifies **high-value customers** for targeted marketing.
* Highlights **top-performing products** to optimize inventory and promotions.
* Reveals **product efficiency** metrics to prioritize revenue-generating SKUs.
* Provides a **data-driven foundation** for business strategy and decision-making.

---
