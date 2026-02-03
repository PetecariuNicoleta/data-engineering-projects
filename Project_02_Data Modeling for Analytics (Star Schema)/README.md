# Data Modeling for Analytics

## Overview
This project focuses on dimensional data modeling for analytics and reporting use cases.
The goal is to design clean, analytics-ready data models using a star schema approach.

The project simulates a typical analytical data warehouse scenario where business users
need fast and intuitive access to sales metrics.

---

## Business Context
A company wants to analyze sales performance across customers, products, and time.
Raw transactional data has already been processed, and the focus is now on building
a semantic layer optimized for BI and reporting tools.

---

## Data Model
The data model follows a **star schema** design:

### Fact Table
- `fact_sales`
  - Represents sales transactions at the order-item grain
  - Contains measurable metrics (e.g. quantity, revenue)

### Dimension Tables
- `dim_customers`
- `dim_products`
- `dim_date`

Each dimension uses surrogate keys to ensure stable joins and historical consistency.

---

## Key Concepts Demonstrated
- Dimensional modeling principles
- Star schema design
- Fact vs Dimension tables
- Grain definition
- Analytics-optimized SQL queries

---
