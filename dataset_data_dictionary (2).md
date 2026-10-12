# Indian Retail Sales Dataset

This is a **fictional, synthetic dataset** created for Power BI learning and portfolio practice. It does not contain real customer records.

## Dataset
- 1,000 order-line records
- Dates from 2024-01-01 through 2026-09-30
- Indian states, cities, and broad regions
- Product categories, customer segments, payment modes, sales, discounts, and profit

## Important definitions
- **Sales**: net sales amount after the discount has been applied.
- **Discount**: discount rate stored as a decimal (for example, `0.10` means 10%).
- **Profit**: simulated profit amount; values are synthetic for practice, not real company financials.
- **Order ID**: unique ID for each row in this practice dataset.
- **Region**: broad geographic grouping (North, South, East, West, or Central).

## Suggested Power BI data types
- Order Date: Date
- Sales, Discount, Profit: Decimal Number
- Quantity: Whole Number
- Remaining columns: Text

## Suggested starter DAX
```DAX
Total Sales = SUM(Sales[Sales])

Total Profit = SUM(Sales[Profit])

Total Orders = DISTINCTCOUNT(Sales[Order ID])

Total Quantity = SUM(Sales[Quantity])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
```

Format `Profit Margin %` as Percentage in Power BI. Since `Sales` is already net of discount, do not subtract `Discount` from `Sales` again.
