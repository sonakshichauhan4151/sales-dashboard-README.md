# Sales Performance Dashboard

**Question:** Which regions, categories, products and customer segments drive our sales, and how do sales change over time?
**Audience:** Sales manager deciding where to focus next quarter.
**Tools:** Excel (formulas, charts, dashboard).
**Data:** Superstore Sales dataset (Kaggle): 9,800 rows, 18 columns, orders from January 2015 to December 2018.

![Dashboard](dashboard.png)

## Summary
I analyzed four years of Superstore orders ($2.26M in sales, 4,922 orders, 793 customers) to see what drives sales. Sales grew 50% from 2015 to 2018, peak every September to December, and are concentrated in the West and East regions and in California and New York. I recommend building stock and campaigns before September and making a plan to lift the South and Central regions.

## Key numbers
| Measure | Value |
|---|---|
| Total sales | $2,261,537 |
| Total orders | 4,922 |
| Total customers | 793 |
| Average order value | $459 |
| Average days to ship | 4.0 |

## Findings
1. **Sales are growing.** $480K in 2015 to $722K in 2018 (+50%), after a small dip in 2016.
2. **Sales are seasonal.** September to December delivers 52% of all sales, and November is the single biggest month.
3. **Sales are concentrated.** West and East together bring 61% of sales, California and New York bring 33%, and the Consumer segment brings 51%.

## Recommendation
Stock up and run campaigns before September, and build a plan to lift the South and Central regions, which together bring only 39% of sales.

## Limits
This dataset has **Sales only** (no Profit or Discount column), so the findings are about revenue, not profit. A high-sales product or region is not necessarily a profitable one.

## Files
- `Sales_Dashboard_Final.xlsx`: dashboard, KPIs, analysis tables, cleaning log, data
- `dashboard.png`: screenshot of the dashboard

## Method
1. Order Date and Ship Date were stored as text (DD-MM-YYYY). I converted them to real dates with a formula.
2. Added Year, Month, Month Number and Days to Ship helper columns.
3. Calculated sales by month, year, region, category, sub-category, segment, ship mode, state and product with SUMIFS.
4. Counted unique orders and customers by flagging the first row of each ID.
5. Built the dashboard with KPI cards and bar and line charts with takeaway titles.
6. Logged every change in the Cleaning Log sheet.
