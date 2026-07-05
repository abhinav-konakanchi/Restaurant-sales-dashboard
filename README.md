
# Restaurant Sales Intelligence Dashboard — Power BI

> An end-to-end business intelligence solution transforming raw restaurant transaction data into actionable insights across sales, menu performance, payments, and table utilization.

##  Project Overview

This project is a **multi-page, star-schema-driven Power BI dashboard** built on real-world restaurant operations data, covering the period **February – March 2026**. It was designed to answer the questions a restaurant owner, operations manager, or finance lead would actually ask:

- Where is revenue coming from, and when does it peak?
- Which menu items and categories drive profitability — and which are underperforming or unavailable?
- How are customers paying, and where is money being lost to refunds?
- Which tables and party sizes generate the most value, and how are reservations trending?

Rather than a single static report, the dashboard is structured as a **decision-support tool** — each page targets a distinct business function (Sales, Menu, Finance, Operations) so different stakeholders can go straight to what matters to them.

## Dashboard Pages

### 1️Overview — Executive Sales Summary
A single-glance snapshot of business health for leadership and stakeholders.

| Metric | Value |
|---|---|
| Total Revenue | **€11.64K** across 289 orders |
| Average Order Value | **€40.27** |
| Net Profit | **€6.70K** (**57.6%** margin) |
| Trend | Clear revenue peaks in mid-February and early March |

**Why it matters:** A 57.6% net margin combined with a €40+ average order value signals healthy unit economics — and the visible seasonal peaks give management a data-backed basis for staffing and inventory planning around high-demand periods.

### 2️Menu Performance — Product Mix Analysis

Breaks revenue down by item and category to identify what's working — and what's being left on the table.

-  **Chicken Biryani** is the #1 revenue-generating item (**€947**, **8.1%** of total revenue)
-  **Main Course** items drive **42.8%** of total revenue — the core profit engine
-  **Beverages** contribute **25.3%** — a strong attachment/upsell rate worth protecting
-  **2 high-revenue items** (*Special Tuk Tuk MENU*, *Chapati*) are currently marked **unavailable** — a flagged, quantifiable **revenue recovery opportunity**

**Why it matters:** This page doesn't just report what sold — it surfaces an actionable gap. Restoring two known high-performing items to the active menu is a low-effort, high-impact lever for revenue recovery.

### Payments & Finance — Transaction & Profitability View
Tracks how money moves through the business — from payment method to refunds to tipping behavior.

-  **Cash** dominates, accounting for **65%** of all transactions
-  **€56.20** identified in refunded payments — flagged for loss/leakage monitoring
-  **€356.40** collected in tips — a service-quality signal
-  Expenses tracked directly against revenue for a true **profitability view**, not just a top-line one

**Why it matters:** Heavy cash dependency has real implications for reconciliation, fraud risk, and digital payment strategy — this page turns that operational reality into a visible, trackable KPI rather than an assumption.

### 4️Tables & Reservations — Operational Utilization
Analyzes physical space efficiency and reservation demand patterns.

-  **Table B1** handles the highest order volume (**40+** orders) — a high-turnover table
-  **Table V4** generates the **highest revenue (€2K+)** despite fewer orders — the **highest average spend per visit**, indicating a premium seating zone
-  **Party size of 2** dominates reservations — confirming a **couples / date-night** customer profile
-  Reservation volume shows clear **growth toward the end of March**

**Why it matters:** Table B1 vs. Table V4 is a classic *volume vs. value* trade-off — this insight alone can inform pricing, seating allocation, and even marketing targeting toward the venue's actual customer base.

##  Tools & Technical Stack

| Layer | Technology | Purpose |
|---|---|---|
| **Visualization & Modeling** | Power BI Desktop | Interactive dashboards, report design, data modeling |
| **Data Transformation** | Power Query (M Language) | Cleaning, shaping, and preparing raw transactional data |
| **Business Logic** | DAX | Custom measures — Revenue, Net Profit, Failed Payments, Table Utilization |
| **Architecture** | Star Schema | Optimized for performance and time intelligence |

##  Data Model Architecture

The dashboard is powered by a **star schema** — the industry-standard architecture for BI reporting, chosen for query performance and analytical clarity.

**8 Tables:**
`orders` · `order_items` · `menu_items` · `menu_categories` · `payments` · `restaurant_tables` · `reservations` · `expenses`

**8 Relationships:**
- 5 core relationships connecting fact and dimension tables
- 3 relationships to a centralized `Date` dimension table, enabling time intelligence (trends, period-over-period comparisons, seasonality)

```
                    ┌─────────────┐
                    │    Date     │
                    │ (Dimension) │
                    └──────┬──────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
   ┌────▼────┐       ┌─────▼─────┐      ┌─────▼──────┐
   │ orders  │───────│  payments  │      │reservations│
   └────┬────┘       └────────────┘      └─────┬──────┘
        │                                       │
   ┌────▼──────┐                          ┌─────▼──────────┐
   │order_items│                          │restaurant_tables│
   └────┬──────┘                          └─────────────────┘
        │
   ┌────▼──────┐       ┌──────────────┐
   │menu_items │───────│menu_categories│
   └───────────┘       └──────────────┘

              ┌──────────┐
              │ expenses │
              └──────────┘
```

This design ensures every dashboard page — Sales, Menu, Payments, Tables — draws from a single consistent source of truth, avoiding duplicated logic or conflicting numbers across visuals.

##  Data Notes

- Dataset scope: **February – March 2026** order data
-  Raw data has been **anonymized to ensure GDPR compliance** — no personally identifiable information is included
-  The full `.pbix` file is **available upon request**

##  Potential Next Steps

- Automated refresh via a live POS/database connection
- Predictive modeling for demand forecasting during peak periods
- Customer segmentation layered on top of party-size and spend data
- Alerting/thresholds for refund rates and unavailable high-revenue items


## Author

**Konakanchi Abhinav**
Master's Student — Business Management, Data Analytics & AI
📍 Berlin, Germany

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/konakanchi-abhinav-3791822bb)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat&logo=gmail&logoColor=white)](mailto:navkona49@gmail.com)

---

⭐ *If you found this project useful or insightful, consider giving it a star — it helps others discover it too.*
