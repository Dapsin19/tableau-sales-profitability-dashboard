# Sales & Profitability Analysis | Tableau

## Project Overview

High sales do not always translate into high profits. I built this Tableau dashboard to examine both measures across regions, product categories, and time using the Sample Superstore retail dataset.

The dashboard brings together sales, profit, profit margin, and order volume. Rather than looking at total revenue alone, I wanted to understand where sales are concentrated, how profitability differs across the business, and which product groups contribute positively or negatively to overall performance.

**[View the Interactive Tableau Dashboard](https://public.tableau.com/app/profile/adedapo.balogun/viz/dire_17936141562140/SalesProfitabilityExecutiveDashboard)**

## Dataset

**Source:** Tableau Sample Superstore

The dataset contains fictional retail transactions, including order dates, sales amounts, profit, customer orders, product categories, and geographic information.

I used these fields to compare performance across different levels of the business, from overall revenue down to regional and product-level results.

## Performance Summary

| Metric | Result |
|---|---:|
| Total Sales | $2.33M |
| Total Profit | $292.3K |
| Profit Margin | 12.56% |
| Distinct Orders | 5,111 |

The business generates approximately $2.33 million in sales, but only 12.56% of that amount is retained as profit in the dataset. This makes profitability an important part of the analysis rather than treating revenue growth as the only measure of performance.

## Regional Sales Analysis

I compared sales across the four regions to understand how much each contributes to total revenue.

| Region | Sales |
|---|---:|
| West | $739,814 |
| East | $691,828 |
| Central | $503,171 |
| South | $391,722 |

The West region records the highest sales, followed by the East. Together, these two regions account for approximately 61.5% of total sales.

The difference between the highest- and lowest-performing regions is approximately $348,000.

However, sales rankings alone do not establish which region is most profitable. The dashboard also includes profit comparisons so that regional performance can be assessed beyond revenue.

## Dashboard Components

### 1. Sales and Profit KPIs

Four KPI cards display total sales, total profit, profit margin, and distinct order count.

I calculated profit margin as:

`SUM([Profit]) / SUM([Sales])`

For order volume, I used:

`COUNTD([Order ID])`

Using distinct order IDs avoids counting multiple product lines from the same transaction as separate orders.

### 2. Monthly Revenue Trend

I grouped sales by month to examine changes in revenue over time.

The line chart makes it easier to identify stronger and weaker sales periods and investigate whether sales follow recurring patterns.

### 3. Monthly Profit Trend

I created a separate monthly profit chart to compare profitability with revenue movement.

This distinction matters because an increase in sales does not necessarily produce an equivalent increase in profit.

### 4. Regional Performance

A horizontal bar chart compares sales across West, East, Central, and South.

I used this chart for both comparison and interaction. Selecting a region allows the dashboard to display results for that part of the business.

### 5. Product Profitability

This view compares profit across product subcategories.

Its purpose is to distinguish products that contribute to profit from those that may reduce overall profitability, even when they generate sales.

### 6. Geographic Performance

I added a US map to examine the geographic distribution of sales.

The map provides a location-based perspective alongside the regional bar chart, allowing users to explore geographic differences at a more detailed level.

## Interactive Filtering

I configured and tested cross-chart filtering in the dashboard.

For example, selecting the West region updates the other connected visualizations to show results for that region.

This allows users to move from a nationwide overview to a regional analysis without opening separate worksheets.

Tooltips also provide additional values when hovering over chart marks.

## Tableau Techniques Used

- Calculated fields for profit margin and distinct order count
- Aggregation using `SUM()` and `COUNTD()`
- Monthly date aggregation
- Geographic data visualization
- Bar and line charts
- Dashboard layout and KPI formatting
- Cross-worksheet filtering
- Interactive tooltips
- Publishing through Tableau Public

## What I Learned

One important part of this project was getting the different worksheets to behave as a single dashboard.

Creating the individual charts was only one stage. I also had to arrange them into a readable layout, configure interactions, troubleshoot the geographic view, and verify that selecting a region changed the other visualizations.

The project reinforced the importance of checking how dashboard elements work together, rather than evaluating each chart independently.


## Live Dashboard

**[Open Sales & Profitability Executive Dashboard on Tableau Public](https://public.tableau.com/app/profile/adedapo.balogun/viz/dire_17936141562140/SalesProfitabilityExecutiveDashboard)**

**Tool:** Tableau Public  
**Dataset:** Sample Superstore  
**Project Type:** Independent portfolio project
