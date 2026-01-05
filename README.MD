# Customer Shopping Behavior Analysis

## 📌 Project Overview
This project analyzes customer shopping behavior using transactional data from **3,900 purchases** across multiple product categories.  
The objective is to uncover insights into **spending patterns, customer segmentation, product preferences, and subscription behavior** to support data-driven business decisions.

---

## 📊 Dataset Summary
- **Total Rows:** 3,900  
- **Total Columns:** 18  

### Key Features
- **Customer Demographics:**  
  - Age  
  - Gender  
  - Location  
  - Subscription Status  

- **Purchase Details:**  
  - Item Purchased  
  - Category  
  - Purchase Amount  
  - Season  
  - Size  
  - Color  

- **Shopping Behavior:**  
  - Discount Applied  
  - Promo Code Used  
  - Previous Purchases  
  - Frequency of Purchases  
  - Review Rating  
  - Shipping Type  

- **Missing Data:**  
  - 37 missing values in the `review_rating` column  

---

## 🧹 Exploratory Data Analysis (Python)
Data preparation and cleaning were performed using **Python**:

### Steps Performed
- **Data Loading:** Imported the dataset using `pandas`
- **Initial Exploration:**  
  - Used `df.info()` to inspect structure  
  - Used `df.describe()` for summary statistics  

- **Missing Value Handling:**  
  - Identified missing values  
  - Imputed missing `review_rating` values using the **median rating per product category**

- **Column Standardization:**  
  - Renamed all columns to **snake_case** for consistency

- **Feature Engineering:**  
  - Created `age_group` by binning customer ages  
  - Created `purchase_frequency_days` from purchase frequency data  

- **Data Consistency Check:**  
  - Identified redundancy between `discount_applied` and `promo_code_used`  
  - Dropped `promo_code_used`

- **Database Integration:**  
  - Connected Python to **PostgreSQL**  
  - Loaded the cleaned dataset into the database for SQL analysis  

---

## 🗄️ Data Analysis Using SQL (PostgreSQL)
SQL queries were used to answer key business questions:

1. **Revenue by Gender** – Compared total revenue between male and female customers  
2. **High-Spending Discount Users** – Customers using discounts but spending above average  
3. **Top 5 Products by Rating** – Products with highest average review ratings  
4. **Shipping Type Comparison** – Average purchase amount: Standard vs Express shipping  
5. **Subscribers vs Non-Subscribers** – Average spend and total revenue comparison  
6. **Discount-Dependent Products** – Top 5 products with highest discounted purchase rate  
7. **Customer Segmentation** – Classified customers as:
   - New  
   - Returning  
   - Loyal  
8. **Top 3 Products per Category** – Most purchased products in each category  
9. **Repeat Buyers & Subscriptions** – Likelihood of subscription for customers with >5 purchases  
10. **Revenue by Age Group** – Revenue contribution across age segments  

---

## 📈 Power BI Dashboard
An **interactive Power BI dashboard** was developed to visualize:
- Revenue trends
- Customer segments
- Product performance
- Subscription behavior
- Shipping preferences  

This dashboard enables stakeholders to explore insights dynamically.

---

## 💡 Business Recommendations
- **Boost Subscriptions:** Promote exclusive benefits for subscribers  
- **Customer Loyalty Programs:** Incentivize repeat buyers to move into the *Loyal* segment  
- **Review Discount Strategy:** Balance promotional impact with profit margins  
- **Product Positioning:** Highlight top-rated and best-selling products  
- **Targeted Marketing:** Focus campaigns on high-revenue age groups and express-shipping users  

---

## 🛠️ Tools & Technologies
- **Python** (pandas, data cleaning, feature engineering)
- **PostgreSQL** (SQL-based business analysis)
- **Power BI** (data visualization & dashboarding)
---
## 📸 Project Screenshots

### 📊 Power BI Dashboard
![Power BI Dashboard]("/Screenshots/Screenshot_20260105_135654.png")

### 🧮 SQL Analysis (PostgreSQL)
![SQL Queries]("/Screenshots/Screenshot_20260105_164204.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164228.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164245.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164304.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164336.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164358.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164426.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164510.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164529.png")
![SQL Queries]("/Screenshots/Screenshot_20260105_164543.png")

### 🧹 Python EDA & Data Cleaning
![Python EDA]("\Screenshots\Screenshot_20260105_162203.png")
![Python EDA]("\Screenshots\Screenshot_20260105_162217.png")
![Python EDA]("\Screenshots\Screenshot_20260105_162946.png")


---
## ✅ Conclusion
This project demonstrates an end-to-end data analytics workflow—from **data cleaning and feature engineering** to **SQL analysis and dashboard visualization**—providing actionable insights into customer shopping behavior.
