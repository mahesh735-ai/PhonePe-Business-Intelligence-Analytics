 PhonePe Payment Insights Dashboard — Power BI

An end-to-end Power BI Business Intelligence project analyzing **300K+ PhonePe UPI transactions** across **108K+ users** to understand payment behavior, transaction trends, service performance, and customer activity.

The project demonstrates how a Data Analyst can transform raw fintech transaction data into actionable business insights that support product and business decisions.

---

## Dashboard Preview

![PhonePe Payment Insights Dashboard](https://github.com/mahesh735-ai/PhonePe-Business-Intelligence-Analytics/blob/main/Phonepe_Dashboard.png)

---

## Business Problem

Digital payment platforms generate large volumes of transaction data across multiple services, users, and payment outcomes. This project turns that raw data into a BI solution answering questions such as:

- Which services contribute the highest transaction value?
- How are transaction volume and value changing over time?
- Which user segments contribute most to platform activity?
- What percentage of transactions succeed or fail, and why?
- When are users most active — weekdays or weekends?

---

## Dataset

| Table | Records | Key Fields |
|---|---:|---|
| `All_Users` | ~108K | User_ID, Name, Age, Join_Date |
| `All_Transactions` | ~300K | Transaction_ID, Amount, User_ID, Service, Service Type, Payment_Status, Reason, Date |

**Time Period:** January 2024 – December 2024

---

## Tools & Technologies

- **Power BI Desktop** — data modeling, DAX, visualization and dashboard development
- **Power Query (M)** — data cleaning and transformation
- **DAX** — KPI calculations and time-intelligence
- **Microsoft Excel** — source data
- **Figma** — custom dashboard UI/background design

---

## Data Preparation & Modeling

**Workflow:** Raw Data → Power Query → Data Cleaning → Data Modeling → DAX → Visualization → Business Insights

**Data Cleaning**
- Removed duplicate rows on `Transaction_ID` and `User_ID`
- Removed blank rows in `All_Users` (missing User_ID would break the relationship)
- Standardized categorical labels (e.g. `Recharge_Bills` → `Recharge Bills`)
- Validated data types across both tables using Power BI's Column Quality/Distribution profiling

**Data Modeling**
- Built a star schema — `All_Users` and `Date_Table` both connect to `All_Transactions` (the fact table)
- All relationships: 1-to-Many, single-direction cross-filtering
- Dedicated **Date Table** built with DAX (`CALENDAR`, `ADDCOLUMNS`) — Year, Month, Month Number, Quarter, Week Day, Day Number, Weekend flag
- Month and Week Day sorted via **Sort By Column** (by their numeric equivalents) so charts display in correct calendar order
- Date table explicitly **Marked as Date Table** to enable time-intelligence DAX functions

---

## DAX & Analytics

8 DAX measures organized in a dedicated `Measures` table, including:

- Total Transactions
- Total Transaction Value
- Unique Users
- Successful Transactions
- Transaction Success Rate
- Month-over-Month Transaction Growth (count)
- Month-over-Month Transaction Value Growth
- Supporting business metrics

**Dynamic Analytics**
- Rule-based conditional formatting — MoM cards turn green/red based on positive/negative growth
- Gradient color-coded bar charts — shaded by transaction value (light → dark)
- Dynamic natural-language insight text — auto-updates based on slicer selection
- Drill-through tooltips — Age Segment breakdown and Service Type sub-category breakdown

---

## Dashboard Features

**Executive Overview**
- Total Transactions, Total Transaction Value, Unique Users, Success Rate
- Monthly transaction trend (line/area chart)
- Service-wise revenue breakdown
- Age segment contribution
- Weekday vs weekend usage
- Top 5 users by transaction value

**Interactive Elements**
- Month and Payment Status slicers
- Drill-through tooltips for deeper breakdowns
- Live insight text that updates with filter selection

**Design**
- Custom background designed in Figma — not a default Power BI theme
- All default visual backgrounds/borders removed for a clean, card-based look
- Kept intentionally simple: 4 KPIs, 2 slicers, 6 core visuals, 2 tooltip pages — prioritizing clarity over visual density

---

## Key Business Insights

| Finding | Business Interpretation |
|---|---|
| Loans generate the highest transaction value (₹2.5B+) among all services | Loan-related services represent the largest share of platform transaction value |
| 96% overall transaction success rate | The remaining 4% (Insufficient Amount, Server Error, Wrong PIN) represents a recoverable-value opportunity |
| Gen X is the largest user segment (37.4%), closely followed by Millennials (37.3%) | The user base skews toward adult, established earners rather than purely younger users |
| 71.6% of transactions occur on weekdays vs 28.4% on weekends | User activity is significantly higher on weekdays |
| Transaction volume shows clear monthly seasonality | Seasonal patterns can inform campaign and engagement timing |

---

## Business Recommendations

1. Investigate payment failure reasons (Insufficient Amount, Server Error, Wrong PIN) to reduce the 4% failure rate.
2. Prioritize loan-related product promotion, given its outsized contribution to transaction value.
3. Design engagement campaigns around the Gen X and Millennial segments, which together drive the majority of platform activity.
4. Use observed monthly seasonality to time promotional campaigns for maximum impact.
5. Leverage weekday activity patterns when scheduling reminders and engagement pushes.

---

## Project Structure

```
PhonePe-Business-Intelligence-Analytics/
│
├── PhonePe_Analysis_Project_BI.pbix          # Main Power BI file
├── Phonepe-Final-Dataset.xlsx                # Source dataset
├── README.md                                 # This file
├── PhonePe_Project_Documentation.pdf         # Detailed project documentation
├── STAR_Interview_Prep.pdf                   # Interview Q&A + STAR method notes
└── Phonepe_Dashboard.png                     # Dashboard screenshot
```

---

## How to Use

1. Clone/download this repository
2. Open `PhonePe_Analysis_Project_BI.pbix` in Power BI Desktop
3. If prompted, update the data source path to point to `Phonepe-Final-Dataset.xlsx` on your machine
4. Explore the dashboard — use the Month and Payment Status slicers to filter

---

## Author

**Mahesh Thakare** — Final-year B.Tech CSE Student | Aspiring Data Analyst
[LinkedIn](https://www.linkedin.com/in/mahesh-thakare-75817b2a7) · [GitHub](https://github.com/mahesh735-ai)

