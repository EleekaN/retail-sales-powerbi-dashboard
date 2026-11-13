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
4. Products with zero discount maintained a 18.12% profit margin, however overall profit with discounts dropped the profit margin at 8.02%.

## Recommendation
- **Strict application of discounts on products.** Profit margin falls from 18.12% with no discounts to -16.45% with 30% discounts.
- **Stock up before the peak season.** Sales in Q4 (Oct-Dec) are 24.26% higher than the rest of the year. Increase inventory for *Office Supplies* to avoid stock-outs.
- **Identify what worked for East region and repeat it elsewhere.**  East leads with Rs 2,71,72,858.50 (26.46% of total sales). Review its top products, customer segments and test the same approach in weakest region.
- **Keep Office supplies in stock always.** It has the highest profit margin 25.59% and 40.31% of orders. Set a minimum stock level so these items never run out.
## Insights
<img width="1122" height="661" alt="Insights" src="https://github.com/user-attachments/assets/0935e64b-f0f5-4c5f-b4e1-1644ea603d9c" />

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

