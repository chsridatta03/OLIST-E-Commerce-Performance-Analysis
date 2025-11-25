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

<img width="342" height="530" alt="Screenshot 2025-11-25 105904" src="https://github.com/user-attachments/assets/6a46a69d-6dee-4e77-907b-4b57928a2b64" />

<img width="879" height="386" alt="Screenshot 2025-11-25 105922" src="https://github.com/user-attachments/assets/90b17291-5012-47c1-b896-04f933b5891f" />

<img width="1057" height="527" alt="Screenshot 2025-11-25 105940" src="https://github.com/user-attachments/assets/c9f59848-a0c6-4208-9e96-060594481a30" />

<img width="1030" height="742" alt="Screenshot 2025-11-25 110010" src="https://github.com/user-attachments/assets/7b9ea149-906c-453c-a19a-23e39f301b6b" />

<img width="522" height="207" alt="Screenshot 2025-11-25 110025" src="https://github.com/user-attachments/assets/0df1c907-5aaa-4818-b258-443617c047f1" />

<img width="1131" height="792" alt="Screenshot 2025-11-25 110618" src="https://github.com/user-attachments/assets/d35aee8e-a1ad-429b-8cfd-486cb6cb1cd4" />

<img width="763" height="766" alt="Screenshot 2025-11-25 110711" src="https://github.com/user-attachments/assets/f07cc9ca-3ddc-4ca7-9a77-9b3b0ea6b671" />

<img width="1155" height="329" alt="Screenshot 2025-11-25 110742" src="https://github.com/user-attachments/assets/14013fd1-6a1e-40aa-b535-92193460ddbf" />

<img width="1272" height="807" alt="Screenshot 2025-11-25 110849" src="https://github.com/user-attachments/assets/7812f258-a20e-485d-8d19-ce147dd93666" />

<img width="1212" height="768" alt="Screenshot 2025-11-25 111226" src="https://github.com/user-attachments/assets/6e8726c9-925c-4f63-bb2d-c171d527e76a" />

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

<img width="611" height="601" alt="Screenshot 2025-11-25 111838" src="https://github.com/user-attachments/assets/fd1c48b4-3909-4000-aaf3-7e5be92d3530" />

<img width="348" height="746" alt="Screenshot 2025-11-25 111905" src="https://github.com/user-attachments/assets/9fac9f2c-c568-4f29-8a8d-d506d002cb70" />

<img width="248" height="864" alt="Screenshot 2025-11-25 111921" src="https://github.com/user-attachments/assets/ee8729c3-c6e8-4587-9eaa-88205cd5c8ed" />

<img width="412" height="609" alt="Screenshot 2025-11-25 112007" src="https://github.com/user-attachments/assets/65cb323e-e77c-4ae1-a62b-195b759a1883" />

<img width="710" height="908" alt="Screenshot 2025-11-25 112049" src="https://github.com/user-attachments/assets/2214dae4-133a-4fe0-a93c-b2508cb6d07e" />

<img width="636" height="680" alt="Screenshot 2025-11-25 112118" src="https://github.com/user-attachments/assets/49360b3e-6ea3-4ede-828c-6857d9b75d8e" />

<img width="570" height="572" alt="Screenshot 2025-11-25 112203" src="https://github.com/user-attachments/assets/034f76e2-0a46-4814-abd8-60bd185da84e" />

<img width="621" height="760" alt="Screenshot 2025-11-25 112218" src="https://github.com/user-attachments/assets/0ae57d89-af2d-4853-92f8-82cead9c0f42" />

<img width="663" height="616" alt="Screenshot 2025-11-25 112230" src="https://github.com/user-attachments/assets/765f0581-585f-4327-bed3-12056e477457" />

<img width="645" height="584" alt="Screenshot 2025-11-25 112241" src="https://github.com/user-attachments/assets/eabb0c17-4ea8-49d6-a914-2908398e2075" />

<img width="770" height="860" alt="Screenshot 2025-11-25 112317" src="https://github.com/user-attachments/assets/8b531fb3-4817-40c8-a1ec-e70dcddb3b59" />




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
