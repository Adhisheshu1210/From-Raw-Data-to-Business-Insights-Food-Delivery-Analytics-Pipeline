# From Raw Data to Business Insights: Food Delivery Analytics Pipeline

## Overview
This project demonstrates the end-to-end integration and analysis of multi-source food delivery data. The goal is to create a single source of truth dataset and derive actionable business insights. The datasets include transactional orders, user master data, and restaurant master data.

---

## Data Sources
1. **orders.csv** – Transactional data containing order details.
2. **users.json** – User master data with personal and membership information.
3. **restaurants.sql** – Restaurant master data including cuisine type and ratings.

---

## Steps Performed

### 1. Load Data
- CSV file (`orders.csv`) using `pandas.read_csv()`.
- JSON file (`users.json`) using `json.load()` and `pandas.DataFrame()`.
- SQL file (`restaurants.sql`) into SQLite in-memory database and then into pandas.

### 2. Merge Data
- Left join `orders` with `users` on `user_id`.
- Left join the resulting dataset with `restaurants` on `restaurant_id`.
- Resulting dataset retains all orders and combines user and restaurant information.

### 3. Clean Data
- Resolved duplicate restaurant name columns.
- Converted `order_date` to datetime.

### 4. Final Dataset
- Saved as `final_food_delivery_dataset.csv`.
- Contains order details, user information, and restaurant information.
- Single source of truth for all analysis.

---

## Analysis Performed

### Order Trends
- Orders per day and month.
- Revenue trend over time.

### User Behavior
- Repeat users.
- Average order value per user.
- Membership impact (Gold vs Regular).

### City and Cuisine Performance
- City-wise revenue and order volume.
- Cuisine-wise popularity and revenue contribution.

### Revenue Seasonality
- Monthly and weekly revenue trends.
- Highest revenue quarters.

---

## Key Findings
- Chennai generates the highest revenue from Gold members.
- Mexican cuisine has the highest average order value.
- Over 2000 users placed orders totaling more than ₹1000.
- Highest revenue restaurants have ratings between 4.6 – 5.0.
- 50% of all orders are placed by Gold members.
- Gold + Italian cuisine combination generates the highest revenue.

---

## Key Columns in Final Dataset
- `order_id`, `user_id`, `restaurant_id`, `order_date`, `total_amount`
- `name`, `membership`, `city`
- `restaurant_name`, `cuisine`, `rating`

---

## Tools and Libraries
- Python
- Pandas
- SQLite3
- Matplotlib/Seaborn for visualizations

---

## Feedback / Experience
This hackathon provided practical experience in integrating multi-source datasets and performing actionable business analysis. It closely simulates real-world data engineering and analytics workflows.

---

## GitHub Repository
[From-Raw-Data-to-Business-Insights-Food-Delivery-Analytics-Pipeline]
Angothu Adhisheshu
(https://github.com/Adhisheshu1210/From-Raw-Data-to-Business-Insights-Food-Delivery-Analytics-Pipeline)




