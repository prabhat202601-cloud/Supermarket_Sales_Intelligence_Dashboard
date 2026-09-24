# Supermarket Sales Intelligence
### IBM SkillsBuild Academic Internship — Data Analytics with AI | August 2026

---

## Overview

An end-to-end data analysis project on 500 supermarket sales transactions across 4 branches and 8 product categories. Built as part of the IBM SkillsBuild Data Analytics with AI internship.

The project covers data quality checks, descriptive statistics, grouped summaries, chart generation, live business question analysis, and actionable business decisions — all using Python and Claude AI.

---

## Dataset

| Attribute | Value |
|-----------|-------|
| File | SUPER_MARKET_DATA.xlsx |
| Rows | 500 transactions |
| Columns | 13 |
| Date Range | January 2026 to July 2026 |
| Branches | A (Jaipur), B (Delhi), C (Mumbai), D (Bengaluru) |
| Categories | Beverages, Personal Care, Dairy, Grocery, Fruits, Snacks, Vegetables, Bakery |
| Products | 20 unique products |
| Payment Methods | UPI, Net Banking, Card, Cash |

---

## Project Structure

```
Supermarket-Sales-Intelligence/
│
├── supermarket_analysis.py         # Main Python analysis script
├── requirements.txt                # Python dependencies
├── SUPER_MARKET_DATA.xlsx          # Source dataset
├── Project_Report.md               # Full written project report
├── README.md                       # This file
└── outputs/
    ├── chart1_monthly_trend.png
    ├── chart2_category_revenue.png
    ├── chart3_branch_revenue.png
    ├── chart4_payment_revenue.png
    ├── chart5_customer_gender.png
    ├── chart6_rating_category.png
    └── chart7_top_products.png
```

---

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/prabhat202601-cloud/Supermarket-Sales-Intelligence
cd Supermarket-Sales-Intelligence

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the analysis
python supermarket_analysis.py
```

All 7 charts are saved to the outputs/ folder automatically.

---

## Key Findings

- Total revenue: ₹2,44,411 across 500 transactions
- Top product: Cheese at ₹27,906
- Top category: Beverages at ₹56,108 (22.9% of revenue)
- Best branch: Branch C Mumbai at ₹72,469
- Most used payment: UPI with 127 transactions and highest avg spend ₹535
- Average rating: 3.99 out of 5.0
- Members drive 58.5% of total revenue

---

## Live Analysis — IBM Questions

| Question | Answer |
|----------|--------|
| Which product generates the highest sales? | Cheese — ₹27,906.30 |
| Which branch performs best? | Branch C (Mumbai) — ₹72,469.45 |
| Which category sells the most? | Beverages — ₹56,108.24 |
| Most popular payment method? | UPI — 127 transactions |
| Do Members spend more than Normal? | No — Normal avg ₹497 vs Member ₹483 |
| Average customer rating? | 3.99 out of 5.0 |

---

## Tools Used

Python, pandas, NumPy, Matplotlib, Seaborn, Claude AI, openpyxl

---

## About

Built by Prabhat Puru (Puru Tiwari)
Data Analyst | AI Automation Engineer | IBM SkillsBuild Intern

LinkedIn: https://www.linkedin.com/in/puru-tiwari-314aab135/

Also see:
- FIFA World Cup Data Intelligence: https://github.com/prabhat202601-cloud/FIFA-WorldCup-Data-Intelligence
- Olist E-Commerce Sales Intelligence: https://github.com/prabhat202601-cloud/Olist-ECommerce-Sales-Intelligence

Built with Claude AI · IBM SkillsBuild · Data Analytics with AI · August 2026
