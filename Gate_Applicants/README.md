

# 🚀 GATE 2019 Applicant Data Analysis

## 📌 Executive Summary

This project focuses on **data cleaning and analysis** of GATE (Graduate Aptitude Test in Engineering) applicant data. The goal was to identify the **Top 15 most popular papers in 2019** based on application numbers.

Using targeted SQL queries, the raw dataset was transformed into a **clean, ranked list**, providing insights into engineering education trends in India.

---

## 🎯 Objective

The project answers the key question:

> **“Which engineering disciplines were the most sought-after by GATE applicants in 2019?”**

The raw dataset contained:

* Extraneous columns (e.g., `id`)
* Data from multiple years

The objective was to refine this dataset and highlight **only the top 15 disciplines for 2019**.

---

## ⚙️ Process

### 🔹 1. Data Cleaning

The dataset (`gate_applicants`) included an `id` column that was irrelevant to the analysis. It was dropped to simplify the table:

```sql
ALTER TABLE gate_applicants
DROP COLUMN id;
```

---

### 🔹 2. Analysis & Ranking

A single SQL query was used to filter, sort, and rank the data:

* **Filter by Year:** Keep only records where `year = 2019`
* **Rank by Popularity:** Order by applicant count (`applied`) in descending order
* **Limit Output:** Show only the **Top 15**

```sql
SELECT * 
FROM gate_applicants
WHERE year = 2019
ORDER BY applied DESC
LIMIT 15;
```

---

## 📊 Result

The final output is a **clean, ranked table** showing the **Top 15 GATE papers (2019)** by applicant count.

Key findings:

* **Mechanical Engineering**, **Civil Engineering**, and **Computer Science** attracted the highest number of applicants.
* Traditional disciplines continue to dominate, reflecting strong demand in core engineering fields.

---

## 💡 Value & Applications

✅ **Educational Insights** – Helps policymakers & institutions understand student preferences and allocate resources accordingly.
✅ **Technical Showcase** – Demonstrates SQL skills in:

* Data Cleaning (`ALTER TABLE`)
* Data Analysis (`SELECT`, `WHERE`, `ORDER BY`, `LIMIT`)
  ✅ **Practical Use Case** – Shows how raw datasets can be transformed into **actionable insights**.

---

## 📂 Files in This Repository

* `gate_applicants.csv` → Original dataset (sample structure)
* `before.png`, `after.png` → data before and after cleaning in SQL
* `query.png` → Query used for the result

---

## 🛠️ Tech Stack

* **SQL** (MySQL / PostgreSQL / SQLite – compatible)
* Dataset: GATE applicants (2019)


Do you want me to also **add a small sample output table** (with dummy data for Top 15) so that viewers immediately see the result without running queries?
