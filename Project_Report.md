# Supermarket Sales Intelligence
## Project Report — IBM SkillsBuild Academic Internship
### Data Analytics with AI | August 2026

**Author:** Prabhat Puru (Puru Tiwari)
**Dataset:** SUPER_MARKET_DATA.xlsx
**Tools:** Python, pandas, NumPy, Matplotlib, Seaborn, Claude AI

---

## 1. Introduction

This project analyses supermarket sales data to uncover patterns across products, branches, categories, customers, and payment methods. The goal is to answer key business questions using data and translate the findings into actionable decisions that a supermarket management team can act on.

The dataset contains 500 transactions across 4 branches in 4 Indian cities, covering the period January 2026 to July 2026.

---

## 2. Dataset Overview

| Attribute | Value |
|-----------|-------|
| Source | SUPER_MARKET_DATA.xlsx (custom dataset) |
| Total Rows | 500 |
| Total Columns | 13 |
| Date Range | January 1, 2026 to July 1, 2026 |
| Branches | A (Jaipur), B (Delhi), C (Mumbai), D (Bengaluru) |
| Categories | 8 (Beverages, Personal Care, Dairy, Grocery, Fruits, Snacks, Vegetables, Bakery) |
| Products | 20 unique products |
| Payment Methods | UPI, Net Banking, Card, Cash |

### Column Descriptions

| Column | Type | Description |
|--------|------|-------------|
| Invoice ID | Identifier | Unique transaction ID (INV0001 to INV0500) |
| Date | Temporal | Transaction date |
| Branch | Dimension | Store branch (A, B, C, D) |
| City | Dimension | City of the branch |
| Customer Type | Dimension | Member or Normal customer |
| Gender | Dimension | Male or Female |
| Product | Dimension | Product name |
| Category | Dimension | Product category |
| Quantity | Metric | Units purchased |
| Unit Price | Metric | Price per unit (₹) |
| Payment | Dimension | Payment method used |
| Rating | Metric | Customer satisfaction score (1–5) |
| Sales | Metric (derived) | Quantity × Unit Price |

---

## 3. Data Quality Report

### 3.1 Completeness Check

| Column | Missing Values | Status |
|--------|---------------|--------|
| All 13 columns | 0 | Complete |

**Result:** Zero missing values across all 500 rows and 13 columns.

### 3.2 Duplicate Check

| Check | Result | Status |
|-------|--------|--------|
| Duplicate rows | 0 | Clean |
| Duplicate Invoice IDs | 0 | Clean |

### 3.3 Sales Validation

The Sales column was validated against the formula: **Sales = Quantity × Unit Price**

| Validation | Result |
|-----------|--------|
| Matching rows | 500 / 500 |
| Mismatches | 0 |

**Conclusion:** The dataset is clean, complete, and ready for analysis with no data quality issues.

---

## 4. Descriptive Statistics

### 4.1 Numeric Summary

| Metric | Quantity | Unit Price (₹) | Sales (₹) | Rating |
|--------|----------|---------------|-----------|--------|
| Count | 500 | 500 | 500 | 500 |
| Mean | 5.54 | 88.66 | 488.82 | 3.99 |
| Std Dev | 2.88 | 57.28 | 437.33 | 0.57 |
| Min | 1 | 27.67 | 28.61 | 3.0 |
| Max | 10 | 236.71 | 2,114.82 | 5.0 |

### 4.2 Key Business KPIs

| KPI | Value |
|-----|-------|
| Total Revenue | ₹2,44,411.08 |
| Total Orders | 500 |
| Average Order Value | ₹488.82 |
| Total Quantity Sold | 2,768 units |
| Average Customer Rating | 3.99 / 5.0 |
| Unique Products | 20 |

---

## 5. Analysis Results

### 5.1 Revenue by Branch

| Branch | City | Total Revenue | Orders | Avg Order | Avg Rating |
|--------|------|--------------|--------|-----------|-----------|
| C | Mumbai | ₹72,469 | 143 | ₹506.78 | 4.05 ★ |
| B | Delhi | ₹64,116 | 133 | ₹482.08 | 3.98 ★ |
| D | Bengaluru | ₹55,468 | 119 | ₹466.12 | 4.09 ★ |
| A | Jaipur | ₹52,357 | 105 | ₹498.64 | 3.84 ★ |

### 5.2 Revenue by Category

| Category | Total Revenue | Avg Order | Orders | Avg Rating |
|----------|--------------|-----------|--------|-----------|
| Beverages | ₹56,108 | ₹684.25 | 82 | 3.96 ★ |
| Personal Care | ₹45,944 | ₹629.37 | 73 | 3.95 ★ |
| Dairy | ₹43,992 | ₹646.94 | 68 | 4.03 ★ |
| Grocery | ₹40,470 | ₹493.54 | 82 | 3.94 ★ |
| Fruits | ₹23,263 | ₹528.71 | 44 | 3.83 ★ |
| Snacks | ₹16,993 | ₹226.57 | 75 | 4.11 ★ |
| Vegetables | ₹11,124 | ₹231.75 | 48 | 3.99 ★ |
| Bakery | ₹6,516 | ₹232.72 | 28 | 4.24 ★ |

### 5.3 Revenue by Payment Method

| Payment Method | Revenue | Transactions | Avg Order |
|---------------|---------|-------------|-----------|
| UPI | ₹67,910 | 127 | ₹534.73 |
| Net Banking | ₹65,195 | 126 | ₹517.42 |
| Card | ₹57,266 | 125 | ₹458.13 |
| Cash | ₹54,040 | 122 | ₹442.95 |

### 5.4 Revenue by Customer Type

| Customer Type | Total Revenue | Orders | Avg Order |
|--------------|--------------|--------|-----------|
| Member | ₹1,43,009 | 296 | ₹483.14 |
| Normal | ₹1,01,402 | 204 | ₹497.07 |

### 5.5 Monthly Revenue Trend

| Month | Revenue |
|-------|---------|
| January 2026 | ₹43,415 |
| February 2026 | ₹30,068 |
| March 2026 | ₹37,306 |
| April 2026 | ₹52,570 ← Peak |
| May 2026 | ₹42,542 |
| June 2026 | ₹35,041 |
| July 2026 | ₹3,467 (partial month) |

### 5.6 Top 10 Products by Revenue

| Rank | Product | Revenue |
|------|---------|---------|
| 1 | Cheese | ₹27,906 |
| 2 | Coffee | ₹27,695 |
| 3 | Shampoo | ₹27,497 |
| 4 | Cooking Oil | ₹21,525 |
| 5 | Tea | ₹17,682 |
| 6 | Apples | ₹17,057 |
| 7 | Face Wash | ₹11,947 |
| 8 | Rice | ₹11,754 |
| 9 | Cold Drink | ₹10,732 |
| 10 | Eggs | ₹10,430 |

---

## 6. Live Analysis — IBM Questions

**Q1. Which product generates the highest sales?**
Cheese generated the highest sales at ₹27,906.30, followed by Coffee at ₹27,694.87 and Shampoo at ₹27,497.48.

**Q2. Which branch performs best?**
Branch C (Mumbai) performed best with total sales of ₹72,469.45 across 143 transactions — the highest revenue and highest order count of all branches.

**Q3. Which category sells the most?**
Beverages had the highest sales at ₹56,108.24 (22.9% of total revenue), with the highest average order value of ₹684.25.

**Q4. What is the most popular payment method?**
UPI was the most used payment method with 127 transactions and the highest revenue at ₹67,910.33. UPI customers also had the highest average spend per order.

**Q5. Do Members spend more than Normal customers?**
No. The average Member transaction was ₹483.14 vs ₹497.07 for Normal customers. However, Members make significantly more purchases (296 vs 204) and contribute 58.5% of total revenue.

**Q6. What is the average customer rating?**
The average customer rating was 3.99 out of 5. Branch D (Bengaluru) had the highest branch rating at 4.09 ★ and Bakery was the highest rated category at 4.24 ★.

---

## 7. Business Decisions

### [HIGH PRIORITY] Fix Branch A — Jaipur
Branch A has both the lowest revenue (₹52,357) and the lowest customer rating (3.84 ★). It is the only branch where both performance and satisfaction are simultaneously weak. An immediate operational and staff review is recommended.

### [HIGH PRIORITY] Counter the February Revenue Dip
February was the lowest revenue month at ₹30,068 — 43% below the April peak of ₹52,570. Targeted January promotions and bundle offers are needed to carry momentum into February.

### [OPPORTUNITY] Grow Branch D — Bengaluru
Branch D has the highest average rating (4.09 ★) but the second-lowest order volume. Customer satisfaction is strong but footfall is low — a marketing and awareness investment is recommended.

### [OPPORTUNITY] Double Down on Beverages and Personal Care
These two categories account for 41.7% of total revenue (₹1,02,052 combined). Increasing shelf space, variety, and promotional investment in these categories would have the highest revenue impact.

### [STRATEGY] Promote UPI Payments
UPI users spend 20.7% more per transaction than Cash users (₹535 vs ₹443). Introducing UPI cashback offers or loyalty points would incentivise higher-spending customers to transact more.

### [STRATEGY] Bakery Visibility Campaign
Bakery is the highest rated category (4.24 ★) but the lowest revenue generator (₹6,516). Customers love the products but very few buy them. A point-of-sale visibility and range expansion drive is recommended.

### [STRATEGY] Formalise the Member Loyalty Programme
Members contribute 58.5% of total revenue and make 45% more transactions than Normal customers. A tiered rewards programme to retain Members and convert Normal customers would protect the highest-value customer segment.

### [PRODUCT] Protect the Top 3 SKUs
Cheese, Coffee, and Shampoo together account for 33.8% of total revenue from just 3 of 20 products. Zero stockouts and premium display placement for these three are non-negotiable.

---

## 8. Charts Generated

| File | Description |
|------|-------------|
| chart1_monthly_trend.png | Monthly revenue trend with peak and low highlighted |
| chart2_category_revenue.png | Revenue by product category (horizontal bar) |
| chart3_branch_revenue.png | Revenue by branch and city |
| chart4_payment_revenue.png | Revenue by payment method |
| chart5_customer_gender.png | Revenue split by customer type and gender (pie charts) |
| chart6_rating_category.png | Average customer rating by category |
| chart7_top_products.png | Top 10 products by revenue |

---

## 9. Conclusion

This analysis of 500 supermarket transactions reveals that Beverages and Personal Care are the highest revenue categories, Branch C (Mumbai) is the top-performing location, Cheese is the single best-selling product, and UPI is both the most popular and most lucrative payment method.

The most important finding for management is the gap between customer satisfaction and revenue in the Bakery category — products customers rate most highly generate the least revenue, pointing to a visibility and awareness problem rather than a quality problem.

The full interactive dashboard is available at the GitHub repository link.

---

*Built with Claude AI · IBM SkillsBuild Academic Internship · Data Analytics with AI · August 2026*
