# retail-sales-powerbi-dashboard
Interactive sales dashboard with KPIs, trends and slicers, built in Power BI on a simulated retail dataset.

## Problem
To understand which month, categories and segment drives sales and profit and do discounts hurt profit.

## Data
- Source: simulated retail sales data (orders, customers, products)
- Period: Jan 2024 - Dec 2025
- Size: 4240 orders after cleaning
- cleaning was done in python : removed duplicates, fixed mixed date formats, handled missing values and removed invalid quanitities.
  
## What the dashboard shows
- **KPI Cards:** Total Sales, Total Profit, Profit Margin %, Total Orders
- **Monthly sales trend** (line chart)
- **Sales and profit by category** (column chart)
- **Sales by region:** (bar chart)
- **Top 10 products by profit**
- **Slicers:** Year, Region, and Segment

## DAX
'''
  total sales = SUM(customers_clean[sales])
  total profit = SUM(customers_clearn[profit]
  profit_margin = DIVIDE([total sales], [total profit])
  total orders = DISTINCTCOUNT(customers_clean[order_id])
'''

## Key findings
1. Technology showed higher sales with 16.97% profit margin, but the office supplies with 2nd highest sales had 25.59% profit margin.
2. East Zone had total sales of 2,71,72,858 which was highest compared to other zones.
3. October to December recorded higher sales volume and lowest sales in March 2024.
4. Products with zero discount maintained a 18.12% profit margin, however profit with discounts dropped the profit margin at 8.02%.

## Recommendation
- Discount should be applied strictly on select products if needed, else avoid.
- Consider increasing the inventory in the last quarter.
- Need to do more market research on the success of East Zone and what needs to be done for other zones.
- Office supplies needs to be in stock always.

## Dashboard Preview
<img width="862" height="677" alt="Screenshot 2026-11-10 212106" src="https://github.com/user-attachments/assets/19f8cd66-00af-48b4-86cb-1dbfac31e8d8" />

## Tools
Power BI desktop, DAX, Python (Pandas) for cleaning

## Files:
- 'retail-sales-powerbi-dashboard.pbix' - powerbi file
- 'retail-sales-powerbi-dashboard.pdf' - exported dashboard
- 'customers_clean.csv' - cleaned dataset
- 'Screenshot 2026-11-10 212106.png' - dashboard preview
retail-sales-powerbi-dashboad.pdf

