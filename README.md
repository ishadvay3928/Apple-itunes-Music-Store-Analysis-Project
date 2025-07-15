# 🎵 Apple iTunes Music Analysis Dashboard

This project delivers a **comprehensive analysis** of Apple iTunes music data using **Power BI Dashboards**, **MySQL Queries**, and **EDA-driven SQL logic**. The objective is to uncover insights into **revenue performance**, **customer behavior**, **music content trends**, and **employee operations**—empowering strategic decisions across the digital music platform.

---

## 📌 Project Objectives

* Analyze global sales performance and revenue trends.
* Identify top-spending customers and segment lifetime value.
* Understand music content popularity (genre, artist, playlist, media type).
* Assess employee structure, hiring trends, and customer support efficiency.
* Provide data-backed insights to improve user retention and product strategy.

---

## 🧾 Dataset Overview

* **Source**: Apple iTunes relational dataset (CSV-based, loaded via MySQL)
* **Tables Used**:

  * `Customer`, `Employee`, `Invoice`, `Invoice_line`, `Track`, `Album`, `Artist`, `Genre`, `Media_type`, `Playlist`, `Playlist_track`
* **Data Span**: Jan 2017 – Dec 2020

### Key Preprocessing Steps:

* Verified column data types (`INT`, `VARCHAR`, `FLOAT`, `DATE`)
* Handled nulls using `NULLIF`, STR\_TO\_DATE, and placeholder values (e.g., ‘N/A’)
* Removed duplicates using subqueries and grouped counts
* Built relational models with foreign keys for robust joins

---

## 📊 Phase 1: Revenue & Sales Dashboard (Page 1)

**Dataset**: `Invoice_cleaned`

### ✅ KPIs:

* **Total Revenue**: \$4.71K
* **Total Customers**: 59
* **Invoice Count**: 614
* **Average Invoice Value**: \$7.67

### ✅ Key Visuals & Insights:

1. **Monthly Revenue Trend (Line Chart)**

   * Revenue peaked in mid-2019 and late 2020
   * Fluctuations between \$5–\$10 suggest moderate, seasonal spikes

2. **Top 5 States by Revenue (Pie Chart)**

   * **Arizona (22.31%)** and **Manitoba (21.52%)** lead in contribution
   * Followed by NSW, NWT, and BC—indicating broad global distribution

3. **Recent Invoices Table**

   * Validates revenue KPI with invoice-level totals
   * Range from \$0.99 to \$23.76, covering 2017–2020

4. **Revenue by Country (Bar Chart)**

   * **USA** is the highest contributor (> \$1,000)
   * Canada, Brazil, France follow as key revenue markets

---

## 👥 Phase 2: Customer Analytics Dashboard (Page 2)

**Dataset**: `Customer_Invoice_Merged`

### ✅ KPIs:

* **Total Customers**: 59
* **Support Reps Active**: IDs 3, 4, 5
* **Avg. Lifetime Value**: \$80 (approx.)

### ✅ Key Visuals & Insights:

1. **Customer Distribution (Map Visual)**

   * Global spread across Europe, USA, Brazil, Canada, Australia

2. **Top 10 Customers by Revenue (Bar Chart)**

   * **František Wichterlová** leads with >\$100 spend
   * Followed by Helena Holý, Hugh O'Reilly

3. **Customer Lifetime Value Over Time (Line Chart)**

   * Peaks in mid-2017, early 2019, and mid-2020
   * Shows stable engagement trends

---

## 🎶 Phase 3: Music Content Insights (Page 3)

**Dataset**: `Track_Merged` (Track + Artist + Album + Playlist + Media Type)

### ✅ KPIs:

* **Total Tracks**: 3,503
* **Total Albums**: 347
* **Total Genres**: 25
* **Playlists**: 14
* **Artists**: 204

### ✅ Key Visuals & Insights:

1. **Top Albums (Bar Chart)**

   * "Are You Experienced?" dominates by track count

2. **Media Type Distribution (Pie Chart)**

   * **MPEG audio file** = 86.6% of library
   * AAC & MPEG4 formats form a minor share

3. **Genre & Artist Analysis (Flow/Bar Chart)**

   * **Rock** is the largest genre (816 tracks)
   * Top artists include **Nirvana, U2, Pearl Jam**
   * Most purchased playlists: "Music" and "90's Music"

---

## 🧑‍💼 Phase 4: Employee & Support Dashboard (Page 4)

**Dataset**: `Employee_Support_Merged`

### ✅ KPIs:

* **Total Employees**: 64
* **Active Support Reps**: 3
* **Avg. Customers per Rep**: 15

### ✅ Key Visuals & Insights:

1. **Employee Hierarchy (Treemap)**

   * Sales Support and IT Staff form major roles
   * Leadership visible through "IT Manager", "Sales Manager"

2. **Customers Managed by Rep (Bar Chart)**

   * **Peacock Jane** manages \~20 customers
   * Followed by **Park Margaret** and **Johnson Steve**

3. **Hiring Trend (Line Chart)**

   * Major hiring spike in **April 2017**
   * Headcount stabilized post-surge

---

## 🔍 Conclusion

The dashboard enables a **360° view** of Apple iTunes operations:

* 🎧 **František Wichterlová** and USA lead in customer spend and revenue.
* 💵 Revenue peaks in **mid-2019** and **late 2020**, with steady invoice growth.
* 🎸 **Rock genre** and **MPEG audio** dominate the content library.
* 👨‍💼 Support reps like **Peacock Jane** are crucial for customer engagement.
* 🌍 Wide customer base across USA, Europe, and Australia.
* 📈 Consistent lifetime value and retention trends point to a loyal user base.

---

## 🛠️ Tools & Technologies Used

* **Power BI** – Visualization and dashboard creation
* **MySQL** – Data preparation and SQL queries
* **Excel** – Pre-cleaning and field validation
* **DAX** – KPI measures, aggregations, and time intelligence
* **Adobe Reader** – For reporting and exporting PDF dashboards

---

## 📁 Project Structure

```
Apple-iTunes-Music-Analysis/
│
├── data/
│   └── *.csv (customer, invoice, track, etc.)
│
├── powerbi/
│   └── itunes_dashboard.pbix
│
├── sql/
│   └── create_load_queries.sql
│   └── insights_queries.sql
│
├── reports/
│   └── Apple iTunes Music Analysis Report.pdf
│   └── README.md
└── images/
    └── [charts, visuals for documentation]
```

---

## 📬 Contact

**Isha Chaudhary**

📧 [ishachaudhary3928@gmail.com](mailto:ishachaudhary3928@gmail.com)

🔗 [LinkedIn](https://www.linkedin.com/in/ishachaudhary18)

📍 Noida, India
