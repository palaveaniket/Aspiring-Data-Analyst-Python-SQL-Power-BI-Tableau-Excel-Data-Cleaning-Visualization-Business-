# Sales Performance & Business Intelligence Dashboard

A beginner-friendly Data Analyst portfolio project using Python, Pandas, Matplotlib, CSV data, and Power BI/Tableau-ready summary files.

> **Dataset note:** The included sales data is synthetic and created for portfolio practice. It is not real company data.

## Project goals
- Clean and validate raw sales data.
- Analyze sales, profit, regions, categories, products, and payment methods.
- Create dashboard-ready summary tables and chart images.
- Practice a reproducible data analytics workflow.

## Tools
- Python 3.10+
- Pandas
- Matplotlib
- Power BI or Tableau (optional, for interactive dashboard recreation)
- Jupyter Notebook or VS Code

## Folder structure
```text
Sales_Performance_BI_Dashboard/
├── data/
│   └── sales_data.csv
├── src/
│   ├── clean_data.py
│   └── analyze_sales.py
├── outputs/
│   ├── cleaned_sales_data.csv
│   ├── monthly_summary.csv
│   ├── region_summary.csv
│   ├── category_summary.csv
│   ├── top_products.csv
│   └── payment_summary.csv
├── dashboard_images/
│   ├── monthly_sales_profit.png
│   ├── sales_by_region.png
│   ├── sales_by_category.png
│   ├── top_10_products.png
│   └── payment_methods.png
├── requirements.txt
└── README.md
```

## Dataset fields
| Column | Description |
|---|---|
| OrderID | Unique order identifier |
| OrderDate | Order date |
| CustomerID | Synthetic customer identifier |
| Region | Sales region |
| Category | Product category |
| Product | Product name |
| Quantity | Units sold |
| UnitPrice | Price per unit before discount |
| Discount | Discount rate (e.g. 0.10 = 10%) |
| Sales | Net sales amount |
| Cost | Estimated cost |
| Profit | Sales minus cost |
| PaymentMethod | Payment type |

## Run the project
1. Download or clone this repository.
2. Open a terminal in the project folder.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Clean the dataset:
   ```bash
   python src/clean_data.py
   ```
5. Create summary tables and charts:
   ```bash
   python src/analyze_sales.py
   ```

The analysis script reads `outputs/cleaned_sales_data.csv` and recreates the summary CSV files and chart PNGs.

## Dashboard images

### Monthly sales and profit
![Monthly Sales and Profit](dashboard_images/monthly_sales_profit.png)

### Sales by region
![Sales by Region](dashboard_images/sales_by_region.png)

### Sales by category
![Sales by Category](dashboard_images/sales_by_category.png)

### Top 10 products
![Top 10 Products](dashboard_images/top_10_products.png)

### Orders by payment method
![Payment Methods](dashboard_images/payment_methods.png)

## Suggested Power BI dashboard
Import `outputs/cleaned_sales_data.csv` into Power BI and create:
- KPI cards: Total Sales, Total Profit, Total Orders, Profit Margin.
- Line chart: Sales and Profit by month.
- Bar chart: Sales by Region.
- Bar chart: Sales by Category.
- Bar chart: Top 10 Products by Sales.
- Donut chart: Orders by Payment Method.
- Slicers: OrderDate, Region, Category, PaymentMethod.

Suggested measures:
```DAX
Total Sales = SUM(cleaned_sales_data[Sales])

Total Profit = SUM(cleaned_sales_data[Profit])

Total Orders = DISTINCTCOUNT(cleaned_sales_data[OrderID])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
```

## Business questions
1. Which region generated the highest sales?
2. Which product categories contribute most to revenue?
3. How do sales and profit change month by month?
4. Which products are the top revenue contributors?
5. Which payment methods are used most often?

## Portfolio description
Built a sales analytics project using Python and Pandas to clean a 1,200-row synthetic retail dataset, calculate sales and profit metrics, and generate summary tables and visualizations for business intelligence reporting.

Update this description if your final dataset size or project work changes.

## Limitations
- Data is synthetic and does not represent real customers or transactions.
- Costs and profits are simulated for learning.
- The included dashboard images are static Python charts. To create an interactive Power BI dashboard, follow the suggested steps and save your `.pbix` file separately.
