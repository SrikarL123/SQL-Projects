

# Amazon Sales Report Analysis using SQL

This project performs an exploratory data analysis (EDA) on an Amazon sales report dataset. The primary objective is to clean the raw data and use SQL queries to extract meaningful insights about sales performance, customer behavior, and product category trends.

## 🧰 Tools Used

  * **SQL**

## 🧹 Data Cleaning

The initial dataset contained several columns that were either redundant or irrelevant for this specific analysis. To streamline the data and improve query efficiency, 11 columns were dropped using the following SQL command:

*Initial state of the data before cleaning:*
*(Image: `before.png`)*

```sql
ALTER TABLE amazon_sale_report
DROP COLUMN `Date`,
DROP COLUMN `Index`,
DROP COLUMN `Sales_Channel`,
DROP COLUMN `Style`,
DROP COLUMN `SKU`,
DROP COLUMN `ASIN`,
DROP COLUMN `Ship_Postal_Code`,
DROP COLUMN `Ship_Country`,
DROP COLUMN `Promotion_IDs`,
DROP COLUMN `Fulfilled_By`,
DROP COLUMN `Unnamed:22`;
```

-----

## 📊 Analysis and Key Insights

Several SQL queries were executed to explore the cleaned dataset and uncover key business insights.

### 1\. Total Unique Orders

To understand the overall transaction volume, the total number of distinct orders was calculated.

**Query Result:** The dataset contains a total of **202 unique orders**.
*(Image: `total orders.png`)*

-----

### 2\. Order Status Breakdown

This analysis groups orders by their fulfillment status to assess the distribution of shipped, delivered, and canceled orders.

**Query Result:**

  * **Shipped:** 191 orders
  * **Shipped - Delivered to Buyer:** 51 orders
  * **Cancelled:** 17 orders

**Insight:** A high fulfillment rate is observed, with the vast majority of orders being successfully shipped to customers.
*(Image: `status x orders.png`)*

-----

### 3\. Customer Type Analysis (B2B vs. B2C)

Customers were segmented into Business-to-Business (B2B) and Business-to-Consumer (B2C) to analyze their respective contributions to orders and revenue.

**Query Result:**

  * **B2C:** 258 orders, generating ₹154,403.41 in revenue.
  * **B2B:** 1 order, generating ₹329.00 in revenue.

**Insight:** The business is overwhelmingly **B2C-focused**, with B2B sales representing a negligible portion of the activity in this dataset.
*(Image: `customer type.png`)*

-----

### 4\. Product Category Analysis

An in-depth analysis of product categories was performed to identify the most popular and profitable items. The `Category` column required cleaning to remove `NULL`, blank, and numeric-only values.

*Initial queries showing data quality issues in the 'Category' column:*
*(Images: `category with null values.png`, `total categories.png`)*

#### Orders and Revenue per Cleaned Category

After filtering out the invalid entries, the orders and revenue were aggregated for each valid product category.

**Top Categories by Orders:**

1.  **kurta:** 104 orders
2.  **Set:** 103 orders
3.  **Top:** 23 orders

*(Image: `Category (cleaned).png`)*

**Top Categories by Revenue:**

1.  **Set:** ₹78,341.46
2.  **kurta:** ₹45,254.00
3.  **Western Dress:** ₹16,662.33

*(Image: `category x revenue.png`)*

**Insight:** Although 'kurta' has slightly more orders, **'Set' generates significantly more revenue** (over 70% more), indicating that items in the 'Set' category have a much higher average price point.

-----

## 📜 Summary of Findings

  * The analysis covers **202 unique sales orders**.
  * The business model is heavily skewed towards **B2C customers**, who account for over 99% of both orders and revenue.
  * The top-performing product categories by volume are **'Set' and 'kurta'**.
  * **'Set' is the most valuable category**, bringing in the highest revenue.
  * The order fulfillment process appears efficient, with a low cancellation rate.
