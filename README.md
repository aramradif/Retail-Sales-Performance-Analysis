# Aram Radif - Retail Sales Performance Analysis

## Project Overview

### Objective
Analyze historical retail sales data to derive actionable business insights that help optimize inventory planning, promotional strategies, and regional targeting.

### Background
The organization aims to better understand:
- Product performance
- Regional sales trends
- Customer buying patterns

This analysis supports data-driven decision-making to improve revenue and operational efficiency.

---

## Dataset Description

**Source:** `sales.csv`

| Column Name       | Data Type | Description |
|------------------|----------|-------------|
| transaction_id   | String   | Unique identifier for each transaction |
| date             | Date     | Transaction date (YYYY-MM-DD) |
| region           | String   | Sales region (North, South, East, West) |
| product          | String   | Product name |
| category         | String   | Product category |
| units_sold       | Integer  | Number of units sold |
| unit_price       | Float    | Price per unit |
| total_sales      | Float    | Optional (units_sold × unit_price) |
| sales_rep        | String   | Optional sales representative |

---

## Architecture & Tech Stack

| Layer | Technology |
|-----|-----------|
| Storage | AWS S3 |
| Processing | Snowflake Snowpark (Python) |
| Visualization | Streamlit in Snowflake |
| Language | Python |
| Charts | Plotly |

**Why this stack?**
- Snowpark enables scalable in-database transformations
- AWS provides durable storage
- Streamlit allows BI-style dashboards without external tools

---

## Data Pipeline Steps

1. **Data Ingestion**
   - Load CSV from AWS S3
   - Validate schema and data types

2. **Data Cleaning**
   - Handle null values
   - Normalize date formats
   - Compute derived fields

3. **Transformations (Snowpark)**
   - Add `month`, `year`
   - Compute total revenue
   - Aggregate metrics

4. **Analytics & Visualization**
   - Product leaderboard
   - Regional comparisons
   - Monthly trends
   - Units vs revenue
   - Average Order Value (AOV)

---

## Metrics Calculated

### 1. Product Sales Leaderboard
Identifies top revenue-generating products.

### 2. Regional Sales Comparison
Compares performance across regions.

### 3. Monthly Trend Analysis
Detects seasonality and growth patterns.

### 4. Units Sold vs Revenue
Highlights margin differences across products.

### 5. Average Order Value (AOV)
Measures revenue efficiency per unit sold.

---

## Streamlit Dashboard

The dashboard answers:
- Which products drive the most revenue?
- Are there seasonal sales patterns?
- Which regions perform best?

Visuals include:
- Bar charts
- Line charts
- Grouped comparisons

---

## Deliverables

- Snowpark Python pipeline
- Streamlit dashboard
- Clean, modular codebase
- Documentation explaining design decisions

---

## How to Run

1. Upload `sales.csv` to AWS S3
2. Configure Snowflake credentials
3. Run the Snowpark pipeline
4. Launch Streamlit app within Snowflake

---

## Author
Aram Radif

