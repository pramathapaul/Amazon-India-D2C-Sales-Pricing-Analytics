# Amazon India D2C Sales & Pricing Analytics

## Project Overview
The primary objective of this project is to analyze real-world e-commerce data from Amazon India to uncover pricing strategies, measure the impact of discounts, and understand customer purchasing behavior. To solve real Direct-to-Consumer (D2C) business challenges, Python was used for raw data extraction and cleaning, followed by Power BI to build an interactive, executive-ready dashboard.

## 🛠️ Tech Stack Used
- **Data Cleaning & Feature Engineering:** Python (Pandas, NumPy)
- **Data Visualization & Modeling:** Power BI, DAX
- **Environment:** Jupyter Notebook / VS Code

## Data Cleaning & Pre-processing (Python)
The raw dataset was highly unstructured. The following transformations were performed using Pandas:
- **Data Type Conversion:** Stripped special characters (`₹`, `,`, `%`) from price and discount columns and converted them to `float64` for mathematical aggregation.
- **Handling Nulls:** Identified and dropped rows with missing ratings and review counts to maintain data integrity.
- **Category Splitting:** Parsed complex breadcrumb category strings (e.g., `Computers&Accessories|...`) into clean `main_category` and `sub_category` columns.
- **Feature Engineering:** Engineered a strategic `price_tier` column, segmenting products into `Budget (Under ₹1K)`, `Mid-Range (₹1K-₹5K)`, and `Premium (₹5K+)` to enable market segmentation analysis.

## Power BI Dashboard Features
The following interactive visuals were built to track critical D2C metrics:
- **Executive KPIs:** Dynamic cards displaying Total Revenue (4.58M), Average Rating, and Average Discount %.
- **Correlation Analysis (Scatter Plot):** Evaluates the relationship between Discount % and Number of Orders (using rating count as a proxy for volume).
- **Market Share (Treemap & Donut Chart):** Visualizes volume distribution across main categories and price tiers.
- **Top Performers (Matrix/Bar Chart):** Ranks the bestselling items at the sub-category level.

## Key Business Insights
1. **Price Sensitivity:** Over 50% of the product volume sits in the 'Budget' tier (Under ₹1K), directly reflecting the price-sensitive nature of the Indian e-commerce landscape.
2. **Discount vs. Volume Correlation:** The scatter plot analysis reveals that while deeper discounts successfully drive higher order volumes in specific budget categories, the strategy yields diminishing returns for premium segments.
3. **Top Revenue Drivers:** The Electronics and Accessories categories consistently generate the highest revenue and order frequency.

## How to Run
1. Execute the `amazon.ipynb` script to process the raw CSV.
2. Open the generated `amazon_india_dashboard_ready.csv` and `amazon.pbix` files in Power BI Desktop to view the dashboard.