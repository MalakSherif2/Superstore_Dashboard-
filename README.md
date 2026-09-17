# Superstore Sales & Profit Analysis Dashboard

An interactive **Microsoft Excel Business Intelligence dashboard** built to analyze profitability, discounts, customer segments, products, and regional performance using a structured **Star Schema data model**.

---

## 📊 Project Overview

This project analyzes a Superstore dataset to uncover patterns in **profitability, discounting, product performance, customer segments, shipping, and regional performance**.

The project follows an end-to-end data analytics workflow, starting from data preparation and modeling, followed by exploratory analysis and interactive dashboard development.

A **Star Schema** was designed using a central `Fact_Sales` table connected to multiple dimension tables, improving data organization, filtering, and analytical flexibility.

---

## 🎯 Business Objectives

The main objectives of this project were to:

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

**Fact_Sales**

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

**Dim_Customers**
- Customer ID
- Customer Name
- Segment

**Dim_Date**
- Order Date
- Year
- Month
- Quarter
- Day of Week

**Dim_Product**
- Product ID
- Category
- Sub-Category
- Product Name

**Dim_Region**
- Country
- City
- State
- Postal Code
- Region

**Dim_Shipping**
- Ship Date
- Ship Mode

### Schema Structure

```text
                    Dim_Customers
                         │
                         │ 1 : *
                         ▼
Dim_Date ────────► Fact_Sales ◄──────── Dim_Product
    │                  │  ▲
    │                  │  │
    │                  │  │
Dim_Shipping ─────────┘  │
                         │
                         ▼
                    Dim_Region
## 🛠️ Tools & Technologies
Microsoft Excel 2021
Power Query
Excel Data Model
PivotTables
PivotCharts
Slicers
Calculated Measures
Conditional Formatting
Data Visualization
Business Intelligence
Profitability Analysis
## 📈 Dashboard

The dashboard provides an interactive overview of Superstore profitability and allows users to explore the data through filters, KPIs, and visualizations.

Key Analysis Areas
Profit Overview
Profit Trends Over Time
Profit by Customer Segment
Product Performance
Bottom 10 Products
Discount Analysis
Regional Performance
Category & Sub-Category Analysis
Shipping Analysis

Interactive Slicers allow users to dynamically filter the dashboard and investigate different business dimensions.

## 💡 Key Business Questions

The dashboard was designed to answer questions such as:

Which products generate the highest profit?
Which products generate negative profit?
Which customer segments contribute the most profit?
How does profitability vary across categories and sub-categories?
Which regions show stronger or weaker profitability?
Are higher discounts associated with lower profit?
How does profit change over time?
Which products may require further investigation?
How does shipping mode relate to business performance?

## 🔎 Key Insights

The analysis focuses on identifying patterns that can support business-oriented decision making, including:

Identifying high- and low-profit products and sub-categories.
Comparing profitability across customer segments.
Detecting products with negative profit.
Examining discount patterns and their association with profitability.
Identifying regional differences in profit performance.
Understanding category and sub-category contribution to overall profit.
Exploring differences in performance across shipping modes.

Data Note: The version of the dataset used in this project does not contain a Sales field. Therefore, the analysis focuses primarily on Profit, Discount, Quantity, and related dimensions, rather than sales-based KPIs such as Total Sales or Profit Margin.

## 🔄 Project Workflow

Raw Dataset
     │
     ▼
Data Cleaning & Preparation
     │
     ▼
Power Query
     │
     ▼
Star Schema Data Model
     │
     ├── Fact_Sales
     ├── Dim_Customers
     ├── Dim_Date
     ├── Dim_Product
     ├── Dim_Region
     └── Dim_Shipping
     │
     ▼
PivotTables & Calculated Measures
     │
     ▼
Exploratory Analysis
     │
     ▼
Interactive Visualizations
     │
     ▼
Dashboard
     │
     ▼
Business Insights

## 📁 Repository Structure

Superstore-Excel-Dashboard/
│
├── Superstore_Dashboard.xlsx
├── README.md
│
└── screenshots/
    ├── dashboard.png
    └── star_schema.png

## 🎓 Skills Demonstrated

This project demonstrates practical experience in:

Data Cleaning & Transformation
Power Query
Dimensional Data Modeling
Star Schema Design
Excel Data Model
PivotTables & PivotCharts
Calculated Measures
Interactive Dashboard Development
Data Visualization
Profitability Analysis
Business Question Formulation
Data-driven Insights

## 🚀 Project Highlights

Data Modeling

Designed a structured Star Schema with a central fact table and multiple dimension tables to support flexible analytical reporting and filtering.

Data Analysis

Used PivotTables, calculated measures, and dimensional attributes to investigate profitability across multiple business perspectives.

Dashboard Design

Built an interactive dashboard using KPIs, charts, conditional formatting, and slicers to make the analysis easy to explore and understand.

Business Analysis

Translated data patterns into business-focused questions and insights related to products, discounts, customer segments, categories, regions, and shipping.

## 👩‍💻 Author

Malak Sherif 

Data Analyst
