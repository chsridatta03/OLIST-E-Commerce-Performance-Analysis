# OLIST-E-Commerce-Performance-Analysis
# E-Commerce Data Analysis SQL Project

## 📊 Project Overview
This project involves analyzing a Brazilian E-Commerce dataset to uncover valuable business insights into customer behavior, sales performance, product trends, and operational efficiency. The analysis was conducted entirely using SQL to query a relational database.

## 🗂️ Dataset & Tools
*   **Dataset:** Olist E-Commerce Public Dataset
*   **Database:** PostgreSQL / MySQL
*   **Tools:** SQL, Git, GitHub

## 🔍 Analysis & Key Insights

Here are the key questions I asked of the data and the answers I found.

### 1. Overall Order Statistics
**How many orders have been placed overall?**
This query gives us the total volume of transactions on the platform.

<img width="643" height="212" alt="Screenshot 2025-09-20 090750" src="https://github.com/user-attachments/assets/bef9d4e9-7b57-4bba-bb0b-2669717d3c88" />


---

### 2. Order Status Distribution
**How many orders are in each status?**
Understanding order statuses is crucial for monitoring the operational health of the e-commerce pipeline. The vast majority of orders are successfully delivered.

<img width="718" height="297" alt="Screenshot 2025-09-20 090922" src="https://github.com/user-attachments/assets/edbf73b9-23bd-40c3-8011-a3e4e75cc503" />

---

### 3. Total  Revenue
**What is the total revenue generated?**
This query calculates the total revenue from all paid orders, including freight values.

<img width="980" height="222" alt="Screenshot 2025-09-20 090854" src="https://github.com/user-attachments/assets/e6cff305-8c63-488d-939d-346ee1d3118a" />

**What is the average order value (AOV)?**
The AOV is a critical metric for understanding customer spending habits.

<img width="898" height="262" alt="Screenshot 2025-09-20 091430" src="https://github.com/user-attachments/assets/02e486da-b273-42cc-a00d-8731a6b76340" />

---

### 4. Customer Geographic Analysis
**Where are our customers located?**
Identifying the top states by customer count helps in geographic targeting and logistics planning.

<img width="671" height="379" alt="Screenshot 2025-09-20 091348" src="https://github.com/user-attachments/assets/72f75819-2eaf-4142-bf75-9f0f0273aee0" />

---

### 5. Sales Trends Over Time
**How many orders are placed each month?**
This time-series analysis shows sales growth and seasonality trends over the years.

<img width="990" height="749" alt="Screenshot 2025-09-20 091547" src="https://github.com/user-attachments/assets/ee32f8ea-5530-4404-a01f-e67e763d46ab" />

---

### 6. Product Performance
**Which product categories are sold the most?**
This reveals the best-performing categories, which is vital for inventory, marketing, and strategic focus.

<img width="805" height="755" alt="Screenshot 2025-09-20 091512" src="https://github.com/user-attachments/assets/f7258f84-5fbe-432d-8688-f00e73c32599" />

---

### 7. Seller Performance
**Which sellers generated the highest revenue?**
Recognizing top-performing sellers is key to partnership and business strategy.

<img width="1006" height="417" alt="Screenshot 2025-09-20 091727" src="https://github.com/user-attachments/assets/79d1adac-bd0f-43c7-9133-0c273601d7f2" />

---

### 8. Customer Payment Preferences
**What is the distribution of payment types?**
Understanding how customers prefer to pay is essential for optimizing the checkout process.

<img width="1143" height="412" alt="Screenshot 2025-09-20 091803" src="https://github.com/user-attachments/assets/4d5e3519-57fb-44b9-9272-8be2bc4cc1ec" />

---

### 9. Operational Metrics
**What is the average shipping time and cost?**
Monitoring delivery times and freight costs is crucial for customer satisfaction and operational efficiency.

**Average Delivery Time:**
<img width="1170" height="256" alt="Screenshot 2025-09-20 091634" src="https://github.com/user-attachments/assets/e3c7074d-50be-4c70-b491-78889c262649" />

**Average Shipping Cost & Proportion to Order Value:**
<img width="1417" height="330" alt="Screenshot 2025-09-20 092223" src="https://github.com/user-attachments/assets/74b30e8c-3a73-4391-b2e3-a984ad5c8fc1" />

---

### 10. Customer Satisfaction & Impact
**Is there a link between review scores and revenue?**
This is a powerful insight showing that higher customer satisfaction (5-star reviews) directly correlates with significantly higher revenue generation.

<img width="1180" height="387" alt="Screenshot 2025-09-20 092357" src="https://github.com/user-attachments/assets/e246874e-203a-4999-be76-adc545ddc0d6" />

---

## 🛠️ Technical Skills Demonstrated
*   **SQL Clauses:** `SELECT`, `FROM`, `JOIN` (INNER), `WHERE`, `GROUP BY`, `ORDER BY`, `LIMIT`
*   **SQL Functions:** Aggregate functions (`COUNT()`, `SUM()`, `AVG()`), `ROUND()`, `DATEDIFF()`, `FORMAT()`
*   **Advanced Techniques:** Subqueries, casting data types (`CAST`, `DECIMAL`), aliasing, handling `NULL` values.

## 📂 Project Files
*   `analysis.sql` - Contains all SQL queries used for this analysis.
*   `README.md` - This file, explaining the project and insights.
*   `screenshots/` - Folder containing all the result visuals (like the ones above).

## 🎯 Conclusion
This SQL analysis provided a comprehensive overview of the e-commerce business, revealing strengths (high delivery rate, strong revenue from top sellers) and potential areas for improvement (shipping cost proportion, geographic expansion beyond top states). The clear link between customer reviews and revenue underscores the immense business value of customer satisfaction.

---
