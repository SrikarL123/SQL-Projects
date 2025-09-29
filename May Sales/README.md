
# Sales Analysis (May 2022)

## Project Overview

This project analyzes product pricing and category-level statistics from a **May 2022 e-commerce sales dataset**. The goal is to extract insights such as:

* Unique product categories
* Number of products per category
* Average discount percentages
* Trade price vs selling price margins
* Average platform prices per category

This analysis helps identify profitable categories, pricing trends, and platform-specific pricing strategies.

---

## Dataset Description

The dataset contains product and pricing information across multiple e-commerce platforms. Relevant columns used in this analysis:

| Column Name      | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| `Category`       | Product category (e.g., T-Shirts, Shoes)                     |
| `Weight`         | Product weight (used for inventory or shipping analysis)     |
| `TP`             | Trade Price – the price at which the seller buys the product |
| `MRP Old`        | Original MRP before any discount                             |
| `Final MRP`      | Final selling price after discount                           |
| `Ajio MRP`       | Product price on Ajio platform                               |
| `Amazon MRP`     | Product price on Amazon platform                             |
| `Amazon FBA MRP` | Product price on Amazon FBA platform                         |
| `Flipkart MRP`   | Product price on Flipkart platform                           |
| `Limeroad MRP`   | Product price on Limeroad platform                           |
| `Myntra MRP`     | Product price on Myntra platform                             |
| `Paytm MRP`      | Product price on Paytm platform                              |
| `Snapdeal MRP`   | Product price on Snapdeal platform                           |

> Other columns such as `SKU`, `Index`, `Style ID`, and `Catalog` were dropped during cleaning to focus on category-level insights.

---

## Data Cleaning Steps

1. Removed unnecessary columns: `index`, `style id`, `catalog`, `SKU`.
2. Standardized column names for consistency.
3. Removed rows with missing or invalid categories.
4. Handled missing or zero prices by converting them to `NULL` where necessary.

---

## Analysis / Query Descriptions

### 1. Distinct Categories

**Image:** `distinct_categories.png`

* Shows all unique product categories in the dataset. Useful to understand product variety and coverage.

---

### 2. Count of Products per Category

**Image:** `products_x_category.png`

* Displays the number of products in each category, highlighting which categories are most stocked or represented.

---

### 3. Average Discount Percentage per Category

**Image:** `avg_discount.png`

* Shows the average discount applied in each category, giving insights into promotional strategies and pricing aggressiveness.

---

### 4. Trade Price vs Selling Price Margin

**Image:** `margin_per_category.png`

* Displays the average profit margin (%) per category, calculated as the difference between the selling price (`Final MRP`) and trade price (`TP`) relative to trade price. Highlights the most profitable categories.

---

### 5. Average Platform Price per Category

**Image:** `avg_platform_price.png`

* Shows the average product price in each category for all platforms (Ajio, Amazon, Flipkart, etc.), revealing platform-specific pricing trends and strategies.

---

## Key Insights

* Categories with higher discounts indicate aggressive promotions.
* Categories with higher profit margins are more profitable.
* Average platform prices reveal pricing strategies across marketplaces.
* Distinct categories and product counts help understand product variety and coverage.

---
