# Superstore Sales & Profit Analysis Dashboard

An interactive **Microsoft Excel Business Intelligence dashboard** built to analyze profitability, discounts, customer segments, products, and regional performance using a structured **Star Schema data model**.

---

## 📊 Project Overview

This project analyzes a Superstore dataset to uncover patterns in **profitability, discounting, product performance, customer segments, shipping, and regional performance**.

The project follows an end-to-end data analytics workflow, starting from data preparation and modeling, followed by exploratory analysis and interactive dashboard development.

A **Star Schema** was designed using a central `Fact_Sales` table connected to multiple dimension tables, improving data organization, filtering, and analytical flexibility.

---

## 🎯 Business Objectives

The main objectives of this project are to:

- Analyze overall profit performance and trends over time.
- Identify the most and least profitable products.
- Examine the relationship between discounts and profitability.
- Compare profitability across customer segments.
- Analyze regional and geographic performance.
- Explore category and sub-category profitability.
- Identify products generating negative profit.
- Build an interactive dashboard for business-oriented analysis.
- Apply dimensional modeling principles using a Star Schema.

---

## 🏗️ Data Model — Star Schema

The Excel Data Model follows a **Star Schema architecture**.

### Fact Table

**`Fact_Sales`**  
Contains transactional-level business data:
- Row ID
- Order ID
- Order Date
- Ship Mode
- Customer ID
- Region
- Product ID
- Quantity
- Discount
- Profit

### Dimension Tables

- **`Dim_Customers`**: Customer ID, Customer Name, Segment
- **`Dim_Date`**: Order Date, Year, Month, Quarter, Day of Week
- **`Dim_Product`**: Product ID, Category, Sub-Category, Product Name
- **`Dim_Region`**: Country, City, State, Postal Code, Region
- **`Dim_Shipping`**: Ship Date, Ship Mode

### Schema Structure

                    Dim_Customers
                          │
                          │ 1
                          ▼ *
Dim_Date ─────────► Fact_Sales ◄───────── Dim_Product
  (1)     *            ▲            *        (1)
                       │ *
                       │
                       │ 1
                  Dim_Shipping
                       ▲
                       │ *
                       │ 1
                  Dim_Region

---

## 🛠️ Tools & Technologies

- **Microsoft Excel 2021** (Power Query, Data Model, PivotTables, PivotCharts, Slicers, Conditional Formatting)
- **Data Modeling** (Star Schema, Dimensional Modeling, Relational Relationships)
- **Business Intelligence & Analytics** (Profitability Analysis, Visual Exploratory Data Analysis)

---

## 📈 Dashboard Overview

The dashboard provides an interactive overview of Superstore profitability and allows users to explore the data through dynamic filters, key performance indicators (KPIs), and targeted visualizations.

### Key Analysis Areas
- **Profit Overview:** Aggregate metrics and profitability trends over time.
- **Customer Segment Analysis:** Comparative profitability across Consumer, Corporate, and Home Office segments.
- **Product Performance:** Top-performing items vs. Bottom 10 products generating negative profit.
- **Discount Impact:** Analyzing how varying discount rates affect overall net margins.
- **Geographic & Regional Performance:** Breakdown across states, cities, and sales regions.
- **Category & Sub-Category Performance:** Hierarchy drill-downs across product lines.
- **Shipping Mode Breakdown:** Evaluating performance variations across shipping speeds.

> **Data Note:** The dataset used in this project does not contain a `Sales` revenue field. Therefore, the analysis focuses primarily on **Profit**, **Discount**, **Quantity**, and related dimensional attributes rather than revenue-based KPIs (e.g., Total Sales or Profit Margin %).

---

## 💡 Key Business Questions Addressed

1. Which products generate the highest profit, and which yield significant losses?
2. Which customer segments contribute the most to the net profit margin?
3. How does profitability vary across product categories and sub-categories?
4. Are higher discount levels directly correlated with profit erosion or negative profit margins?
5. How does profitability fluctuate over monthly and yearly time horizons?
6. Does shipping mode selection impact product profitability?

---

## 🔎 Key Insights

- **High- and Low-Profit Products:** Clear identification of core profit drivers versus items running at a continuous loss.
- **Discount Thresholds:** Uncovering patterns where discount rates above specific thresholds lead directly to negative margins.
- **Regional & Segment Variances:** Pinpointing geographically underperforming zones and high-value customer groups.

---

## 🔄 Project Workflow

Raw Dataset
    │
    ▼
Data Cleaning & Preparation (Power Query)
    │
    ▼
Star Schema Data Modeling (Excel Data Model)
    │
    ├── Fact_Sales
    ├── Dim_Customers
    ├── Dim_Date
    ├── Dim_Product
    ├── Dim_Region
    └── Dim_Shipping
    │
    ▼
Calculated Measures & PivotTables
    │
    ▼
Exploratory Data Analysis (EDA)
    │
    ▼
Interactive Dashboard Construction
    │
    ▼
Business Insights & Actionable Recommendations

---

## 📁 Repository Structure

Superstore-Excel-Dashboard/
│
├── Superstore_Dashboard.xlsx     # Interactive Excel Workbook & Data Model
├── README.md                     # Project documentation
│
└── screenshots/                  # Dashboard and Data Model visual assets
    ├── dashboard.png
    └── star_schema.png

---

## 🎓 Skills Demonstrated

- Data Cleaning, ETL, and Transformation with **Power Query**.
- **Dimensional Data Modeling** (Star Schema architecture, primary/foreign keys, cardinality).
- Advanced **Excel Data Modeling** and **PivotTable/PivotChart** design.
- **Interactive Dashboard UI/UX Design** using slicers, custom layouts, and conditional formatting.
- Formulating business-driven queries and translating data patterns into actionable insights.

---

## 👩‍💻 Author

**Malak Sherif**  
Data Analyst

### Connect With Me

- 💼 LinkedIn: [Malak Sherif](https://www.linkedin.com/in/malak-sherif-b03138357)

---

⭐ **If you found this project interesting, feel free to explore the repository and share your feedback!**

#DataAnalytics #Excel #BusinessIntelligence #DataModeling #PowerQuery #DataVisualization
