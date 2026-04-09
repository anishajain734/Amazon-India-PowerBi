# Amazon India Sales Dashboard 2025

A Power BI dashboard analyzing Amazon India’s 2025 sales performance, combining business storytelling, analytics, and decision-ready insights.

## Key Highlights
- **Total Sales:** ₹1.12B
- **Total Quantity Sold:** 45K
- **Rolling 3-Month Average Sales:** 285.76M
- **Average Review Rating:** 3.04
- **Sales MoM Growth:** +10%
- Payment method analysis (COD vs UPI vs Cards)
- State-level and category-level drill-through insights

## Insights
- MoM sales grew 10%, driven by Electronics & Beauty categories.
- Digital payment methods outperform COD.
- High-rated but low-selling categories show potential growth opportunities.

## DAX Formulas Used
1. `% Contribution by Payment Method = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL('Amazon 2025'[Payment_Method])))`
2. `AOV = DIVIDE([Total Sales], DISTINCTCOUNT('Amazon 2025'[Order_ID]))`
3. `Avg Review Rating = AVERAGE('Amazon 2025'[Review_Rating])`
4. `Customer Type = IF([Customer Orders] > 1, "Repeat", "New")`
5. `Rolling 3M Sales = CALCULATE([Total Sales], DATESINPERIOD('Amazon 2025'[Date], MAX('Amazon 2025'[Date]), -3, MONTH))`

## How to Use
1. Open `Amazon_India_2025_Dashboard.pbix` in Power BI Desktop.  
2. Use slicers to filter by State, Month, Payment Method, Delivery Status, or Product Category.  
3. Explore drill-through tables for granular state-level insights.

## Screenshots
![Dashboard Overview](docs/screenshots/dashboard_overview.png)
![State Drillthrough](docs/screenshots/state_drillthrough.png)
