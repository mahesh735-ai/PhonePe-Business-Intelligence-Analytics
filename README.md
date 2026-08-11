# 📱 PhonePe Payment Insights Dashboard — Power BI

An end-to-end **Power BI Business Intelligence** project analyzing **300K+ PhonePe UPI transactions and 108K+ users** to understand payment behavior, transaction trends, service performance, and customer activity.

The project demonstrates how a Data Analyst can transform raw fintech transaction data into actionable business insights to support product and business decisions.

---

## 📸 Dashboard Preview

<!-- Add your dashboard screenshot below -->

![PhonePe Payment Insights Dashboard](https://github.com/mahesh735-ai/PhonePe-Business-Intelligence-Analytics/blob/main/Phonepe_Dashboard.png)

---

## 🎯 Business Problem

Digital payment platforms generate large volumes of transaction data across multiple services, users, and payment outcomes.

The objective of this project is to transform raw transaction and user data into a business intelligence solution that helps answer questions such as:

- Which services contribute the highest transaction value?
- How are transaction volume and value changing over time?
- Which user segments contribute most to platform activity?
- What percentage of transactions are successful or failed?
- What are the major reasons for payment failures?
- When are users most active?
- Which services and customer segments require further attention?

---

## 📊 Dataset

The project uses a **PhonePe transaction and user dataset** containing detailed information about users, transactions, services, payment status, and transaction outcomes.

| Table | Records | Key Fields |
|---|---:|---|
| `All_Users` | ~108K | User_ID, Name, Age, Join_Date |
| `All_Transactions` | ~300K | Transaction_ID, Amount, User_ID, Service, Service Type, Payment_Status, Reason, Date |

**Time Period:** January 2024 – December 2024

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — Data modeling, DAX, visualization and dashboard development
- **Power Query (M)** — Data cleaning and transformation
- **DAX** — KPI calculations and time-based analysis
- **Microsoft Excel** — Source data
- **Figma** — Custom dashboard UI/background design

---

## 🏗️ Data Preparation & Modeling

The project follows an end-to-end BI workflow:

**Raw Data → Power Query → Data Cleaning → Data Modeling → DAX → Visualization → Business Insights**

### Data Cleaning & Transformation

- Removed duplicate records
- Handled blank/missing values
- Standardized categorical values
- Validated data types
- Prepared data for analytical modeling

### Data Modeling

- Built a proper **Star Schema**
- Created a dedicated Date Table using DAX
- Implemented **1-to-many relationships**
- Used single-direction cross-filtering
- Structured the model for efficient analysis

### Date Table

The Date Table includes:

- Year
- Month
- Quarter
- Weekday
- Weekend Flag
- Date-based analysis fields

---

## 📐 DAX & Analytics

Developed **8 DAX measures** for KPI and business analysis, including:

- Total Transactions
- Total Transaction Value
- Unique Users
- Successful Transactions
- Transaction Success Rate
- Month-over-Month Transaction Growth
- Month-over-Month Transaction Value Growth
- Other supporting business metrics

### Dynamic Analytics

The dashboard also includes:

- Dynamic conditional formatting
- MoM growth indicators
- Gradient-based visual formatting
- Dynamic insight text based on slicer selections
- Drill-through/tooltips for deeper analysis

---

## 📊 Dashboard Features

### Executive Overview

The main dashboard provides a high-level view of:

- Total Transactions
- Total Transaction Value
- Unique Users
- Transaction Success Rate
- Monthly Transaction Trends
- Service Performance
- User Demographics
- Weekday vs Weekend Activity

### Interactive Analysis

Users can explore the data using:

- Month filters
- Payment Status filters
- Interactive charts
- Drill-through/tooltips
- Dynamic business insights

---

## 💡 Key Business Insights

| Finding | Business Interpretation |
|---|---|
| **Loans generate the highest transaction value** | Loan-related services represent a significant share of transaction value |
| **96% overall transaction success rate** | The remaining failed transactions represent an opportunity to investigate payment issues |
| **Millennials represent 37.3% of users and Gen Z 20.74%** | Younger customer segments form a significant portion of the user base |
| **71.6% of transactions occur on weekdays** | User activity is significantly higher during weekdays |
| **Transaction volume shows monthly variation** | Seasonal patterns can help inform campaign and engagement planning |

### 🔎 Additional Insights

> Add your own findings here after independently exploring the dashboard and dataset.

- 
- 
- 

---

## 🎯 Business Recommendations

Based on the analysis:

1. **Investigate payment failures** to identify operational issues and reduce unsuccessful transactions.
2. **Focus engagement strategies on younger customer segments** based on their significant contribution to the user base.
3. **Optimize service-specific campaigns** around high-value services such as Loans.
4. **Use transaction seasonality** to plan targeted promotional campaigns.
5. **Monitor weekday transaction behavior** when planning customer engagement activities.

### 💡 Additional Recommendations

> Add your own business recommendations after your independent analysis.

1. 
2. 
3. 

---

## 📁 Project Structure

```text
PhonePe-Business-Intelligence-Analytics/
│
├── PhonePe_Analysis_Project_BI.pbix
├── Phonepe-Final-Dataset.xlsx
├── README.md
├── Documentation.md
├── STAR_Interview_Prep.md
│
└── screenshots/
    └── dashboard-preview.png
