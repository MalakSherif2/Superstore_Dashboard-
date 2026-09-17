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
