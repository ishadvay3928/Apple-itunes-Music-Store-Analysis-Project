# 🎵 Apple iTunes Music Analysis Project

This project delivers a **comprehensive end-to-end data analysis** of Apple iTunes music store data using **MySQL** and **Power BI**. It uncovers insights across sales, customer behavior, music content, employee efficiency, and geographic trends.

---

## 📌 Project Objectives

* Understand customer purchase patterns and lifetime value
* Identify top-performing tracks, genres, and media types
* Evaluate sales performance by geography and time
* Analyze employee efficiency and customer support impact

---

## 🛠️ Tools & Technologies Used

* **SQL (MySQL)** – Data Preprocessing , Data querying, transformation, and analysis
* **Power BI** – Interactive dashboard with DAX measures and visuals
* **CSV Data** – Cleaned datasets for each entity

---

## 🗃️ Data Workflow

### 1. Data Loading

* Created SQL tables for `Artist`, `Album`, `Customer`, `Invoice`, etc.
* Loaded data using `LOAD DATA INFILE` with custom delimiters and NULL handling.
* Applied `STR_TO_DATE` for date fields.

### 2. Data Preprocessing

* ✅ Verified data types using `DESCRIBE`
* ✅ Checked for NULLs using `SUM(column IS NULL)`
* ✅ Replaced missing values with 'Unknown' or removed incomplete records
* ✅ Handled duplicates using `NOT IN (SELECT MIN(...))` logic

---

## 📌 SQL Query Highlights

```sql
-- Top Spending Customers
SELECT c.first_name, c.last_name, SUM(i.total) as total_spent
FROM customer c
JOIN invoice i ON c.customer_id = i.customer_id
GROUP BY c.customer_id
ORDER BY total_spent DESC;

-- Revenue by Country
SELECT billing_country, SUM(total) as revenue
FROM invoice
GROUP BY billing_country
ORDER BY revenue DESC;

-- Tracks Never Purchased
SELECT track_id FROM track
WHERE track_id NOT IN (SELECT DISTINCT track_id FROM invoice_line);
```

---

## 📊 Dashboard Overview (Power BI)

The 4-page interactive dashboard visualizes:

### 📈 Page 1: Revenue & Sales

* **KPIs**: Total Revenue = \$4.71K | Avg Invoice = \$7.67 | Total Invoices = 614
* Revenue trends from 2017–2020
* Revenue by State/Country
* Recent invoice table

### 👥 Page 2: Customer Analytics

* Top customers by revenue (e.g., František Wichterlová: \$144.54)
* Global customer map
* Customer Lifetime Value (Avg: \$79.82)
* Repeat & inactive customers

### 🎧 Page 3: Music Content Insights

* Track distribution by genre and media type
* Top albums and most purchased playlists
* “Rock” is the most dominant genre (816 tracks)

### 🧑‍💼 Page 4: Employee & Support Analysis

* Hierarchy visualization of Sales & IT departments
* Customer distribution per support rep
* Employee hire trend spike in April 2017

---

## 🔎 Key Business Insights

### 💰 Customer Insights:

* 59 repeat customers with the highest spender at \$144.54
* Czech Republic has the highest revenue/customer (\$136.62)
* 59 inactive customers since 2020

### 📆 Sales Insights:

* Revenue peaks: Aug 2019 & Jan 2018
* Items priced at \$0.99 drive 90% of sales
* Avg Invoice: \$7.67

### 🎼 Product Insights:

* Top 10 tracks account for major revenue
* "Music" playlist dominates with 4742 purchases
* Many tracks (ID: 99 onwards) have never been purchased

### 🌍 Geographic Trends:

* USA leads in customer count (13) and revenue (\$1040.49)
* Arizona is the top-performing state (22.31% share)

### 🧑‍💼 Operational Insights:

* Avg 20 customers per support rep
* Jane Peacock leads with most revenue generated (\$1731.51)

---

## ✅ Conclusion

The iTunes Music Analysis project effectively demonstrates how raw transactional and music metadata can be transformed into valuable business insights. From customer behavior to product success metrics and operational performance, the analysis highlights revenue drivers and areas for optimization.


## 📬 Contact

**Isha Chaudhary**

📧 [ishachaudhary3928@gmail.com](mailto:ishachaudhary3928@gmail.com)

🔗 [LinkedIn](https://www.linkedin.com/in/ishachaudhary18)

📍 Noida, India
