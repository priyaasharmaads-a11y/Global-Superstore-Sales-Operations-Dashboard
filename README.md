# Dashboard Draft: Executive Sales & Operations Overview (Single Page)

This Power BI report is designed as a single-page executive dashboard combining sales, profit, customer segments, category performance, and operational metrics. The goal is to provide business stakeholders with an at-a-glance view of overall performance and the ability to explore the data through interactive filters.

---

## Page Layout Structure (Single Page)

The dashboard is divided into four major sections:

---

### 1. KPI Summary (Top Row)

The top section contains the primary business KPIs:

- Total Sales
- Total Profit
- Profit Margin
- Average Delivery Days

These KPIs give an immediate understanding of overall business performance. Each card is formatted with clear labels, consistent font sizes, and automatic unit scaling.

---

### 2. Sales Trend | Month-Level Analysis

A line chart showing monthly sales across all years.

**Fields used:**
- Axis: `Calendar[Month]` (sorted by Month Number)
- Values: `Total Sales`

This visual helps identify seasonal patterns, monthly variations, and overall sales movement through the year.

---

### 3. Category-Level Performance

A horizontal bar chart that breaks down Total Sales across major categories:

- Technology
- Furniture
- Office Supplies

**Fields used:**
- Axis: `Category`
- Values: `Total Sales`

This shows which product categories contribute most to revenue.

---

### 4. Regional Sales Distribution

A bar chart summarizing sales contribution across global regions.

**Fields used:**
- Axis: `Region`
- Values: `Total Sales`

This highlights strong and weak-performing markets and supports geographic performance review.

---

### 5. Slicers Panel (Interactive Filters)

Placed on the left side for easy access:

- Region
- Segment
- Year

These slicers allow the user to filter the entire dashboard, enabling interactive analysis without navigating to another page.

---

## DAX Measures Used

```dax
Total Sales = SUM(Superstore[Sales])

Total Profit = SUM(Superstore[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Avg Delivery Days = AVERAGE(Superstore[Delivery_Days])
```

---

## Purpose of This Dashboard

This single-page design is intended to:

- Provide a clean, consolidated view of business performance
- Support decision-making without requiring multi-page navigation
- Highlight trends, product category insights, and geographic patterns
- Deliver a balance of summary (KPIs) and detail (category/region visuals)
- Offer interactive filtering for deeper exploration

The entire analysis is intentionally presented on one page to maintain simplicity, clarity, and executive usability.
