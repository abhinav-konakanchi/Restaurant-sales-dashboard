
 Restaurant Sales Dashboard — Power BI

A multi-page business intelligence dashboard built on real restaurant  data, analyzing sales performance, menu insights, payment patterns, and table utilization for the period February–March 2026.

### Dashboard Pages

### Page 1 — Overview 
![Overview](page1_overview.png)

**Key Insights:**
- Total Revenue: €11.64K across 289 orders
- Average Order Value: €40.27
- Net Profit: €6.70K (57.6% margin)
- Revenue peaks visible in mid-February and early March

### Page 2 — Menu Performance
![Menu Performance](page2_menu.png)

**Key Insights:**
- Chicken Biryani is the #1 revenue item (€947, 8.1% of total)
- Main Course drives 42.8% of total revenue
- Beverages contribute 25.3% — strong attachment rate
- 2 high-revenue items (Special Tuk Tuk MENU, Chapati) 
  currently marked unavailable — potential recovery opportunity

### Page 3 — Payments & Finance
![Payments & Finance](page3_payments.png)

**Key Insights:**
- Cash dominates at 65% of transactions
- €56.20 in refunded payments identified
- €356.40 in tips collected
- Expenses tracked against revenue for profitability view

### Page 4 — Tables & Reservations
![Tables & Reservations](page4_tables.png)

**Key Insights:**
- Table B1 handles the most orders (40+)
- Table V4 generates the highest revenue (€2K+) 
  despite fewer orders — highest average spend per visit
- Party size 2 dominates reservations (couples/date-night venue)
- Reservation trend shows growth toward end of March

---

## Tools & Technologies
- **Power BI Desktop** — data modeling, DAX measures, visualizations
- **Power Query (M language)** — data cleaning and transformation
- **DAX** — calculated measures including Revenue, Net Profit, 
  Failed Payments, Table Utilization
- **Data modeling** — Star schema with 8 tables and relationships

## Data Model
- 8 tables: `orders`, `order_items`, `menu_items`, `menu_categories`,
  `payments`, `restaurant_tables`, `reservations`, `expenses`
- Star schema with a central `Date` table for time intelligence
- 8 relationships (5 core + 3 date relationships)

## Data Notes
- Data covers February–March 2026 (order data)
- Raw data anonymized for privacy (GDPR compliance)
- `.pbix` file available upon request

##  Author
**Konakanchi Abhinav**  
Master's student in Business Management, Data Analytics & AI  
Berlin, Germany  
www.linkedin.com/in/konakanchi-abhinav-3791822bb
navkona49@gmail.com
