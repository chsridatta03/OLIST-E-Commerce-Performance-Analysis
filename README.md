# 📦 Olist E-Commerce End-to-End Analytics Project

This project analyzes the Brazilian e-commerce dataset (Olist) to answer one core business question:

> How can an online marketplace increase revenue while improving delivery performance and customer experience?

The analysis was executed across four stages — Excel for raw data, SQL for ETL & business logic, Python for deep EDA, and Power BI for interactive dashboards.
Each tool played a unique role in the overall story.

---

## 🧾 1. Excel — Raw Data Collection

The project begins with 10 raw CSV files from Olist’s e-commerce platform.
Excel acted as the data landing zone, where data structure and column consistency were first examined.

📌 *Files included:*
`customers_data`, `orders_data`, `order_items_data`, `products_data`, `sellers_data`, `geolocation_data`, `payments_data`, `reviews_data`, `category_names_translation`

🔍 *Role of Excel in the project:*

* Understanding table relationships
* Checking column formats & missing values
* Exporting clean files for SQL import

*No transformations were performed here — just secure raw storage.

---

## 🧠 2. SQL — Data Cleaning, Modeling & Business KPIs

SQL Server was used to transform raw data into clean, structured, business-ready tables.
This is where data engineering + business analysis intersect.

### 🔧 Major SQL Work Done

✔ Cleaned city names, product names, seller names (case normalization, accent removal, trimming)
✔ Handled NULL values with meaningful replacements
✔ Fixed data types — consistent numeric, text, and datetime columns
✔ Checked duplicates across all tables
✔ Derived new time metrics (delivery delay, approval time, ship time, total order cycle)

### 📌 Created Data Model

Foreign-key relationships were built so each entity connects correctly:
Customers → Orders → Order Items → Products → Sellers → Payments → Reviews → Geolocation

### 📊 Created Business-Meaningful KPIs using Views, CTEs & Window Functions

* Order Life Cycle View (purchase → approval → delivery → ETA comparison)
* 3-Month Rolling Average Revenue
* % Orders Delivered Late
* Average Delivery Delay by Customer Location
* Customer Repeat Purchase & Revenue Contribution

SQL delivered the first layer of business insights:

> ⁃ Late deliveries were a major driver of poor review scores
> ⁃ Delivery delays varied widely by region
> ⁃ Revenue growth was steady but customer retention was extremely low

These outputs became the foundation for deeper statistical analysis in Python.

---

## 🐍 3. Python — Exploratory Data Analysis & Behavioral Insights

Python was used to go deeper into patterns that dashboards cannot reveal visually.

📌 Key analyses performed with Python

| Area                                | Insight                                                                 |
| ----------------------------------- | ----------------------------------------------------------------------- |
| Delivery delays                     | Majority of delays range between -15 and 0 days (early delivery common) |
| Delay vs Review Score               | Longer delays strongly lower review score                               |
| Price vs Freight                    | Freight cost increases non-linearly with product price                  |
| Installment payments vs Order Value | Higher order values correlate with more installments                    |
| Order cycle breakdown               | 90% of orders spent more time shipping than approval                    |
| Rating distribution                 | ~60% of reviews are 5 stars despite delivery issues                     |

### 🔥 Why Python added value

Power BI can show KPIs but cannot expose statistical relationships.
Regression and KDE density plots exposed behavioral drivers of revenue and satisfaction, allowing us to answer questions like:

* What frustrates customers the most? → delivery delay
* What influences freight cost?* → product price
* Who buys again?* → shockingly low repeat rate

Python uncovered the cause → effect mechanisms behind the KPIs.

---

## 📊 4. Power BI — Final Business Dashboard & Storytelling

All curated and processed data was loaded into Power BI for interactive business monitoring.

> The dashboard is split into two pages, each answering a different management question.

### 📌 Page 1 — Business Performance Dashboard

Focus: How is the business performing financially?
Highlights:

* Total Orders, Delivered Orders, Total Customers
* Total Revenue & Average Order Value
* Order & revenue trend (monthly)
* Payment method behavior
* Top performing product categories
* State-wise revenue heat map

### 📌 Page 2 — Delivery & Customer Experience Dashboard

Focus: How is delivery performance shaping customer sentiment?
Highlights:

* On-time delivery %, Average Delivery Days
* Average review score & delays
* Monthly delivery punctuality trend
* Seller-wise delay & satisfaction heat table
* Repeat customer % (near zero) — a major red flag

### 🎯 Key Business Takeaways from Dashboards

| Area                 | Finding                                    | Action                              |
| -------------------- | ------------------------------------------ | ----------------------------------- |
| Customer retention   | Repeat purchases are almost 0%             | Launch loyalty & retention programs |
| Delivery reliability | 10% of orders delivered late               | Optimize slow-performing sellers    |
| Revenue growth       | High order volume but fragile satisfaction | Improve post-purchase experience    |
| Geography            | Delays cluster by specific states          | Adjust logistics partnerships       |

---

## 🚀 Final Outcome

| Skill Area        | Deliverable                                    |
| ----------------- | ---------------------------------------------- |
| Data Engineering  | Clean SQL relational model                     |
| Business Analysis | KPIs & views answering real business questions |
| Data Science      | Python EDA uncovering behavioral drivers       |
| BI                | Executive-ready 2-page dashboard               |

This project replicates how a real data analyst / BI analyst solves an end-to-end business problem — not just visualizing data but transforming it into recommendations that impact revenue and customer satisfaction.

---

## 📂 Repository Structure

```
📁 Excel — Raw source data
📁 SQL — All cleaning + transformation + KPI queries
📁 Python — Jupyter Notebook files for EDA
📁 PowerBI — .pbix dashboard file
📁 README.md — Project documentation
```

---

If you want, I can also generate:
✔ A short LinkedIn post summarizing this project
✔ A PDF case study to attach with your resume
✔ A one-page portfolio website version

Just ask. 🚀
