# Retail Sales Data Analysis – Oasis Infobyte Internship

## Project Overview

This project performs Exploratory Data Analysis (EDA) on retail sales data as part of the Oasis Infobyte Data Analytics Internship.

The analysis focuses on identifying sales trends, customer demographics, product demand, category performance, profitability, and relationships between numerical variables to generate actionable business insights.

## Objective

The main objectives of this project are:

- Analyze monthly and quarterly revenue trends.
- Understand customer demographic patterns.
- Identify the top-selling products based on order quantity.
- Compare revenue and profit across product categories.
- Analyze relationships between important numerical variables.
- Identify profitability patterns using profit margins.
- Generate actionable business recommendations from the analysis.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Analysis Performed

The following analysis was performed in the project:

1. Data loading and initial inspection
2. Data cleaning and duplicate record removal
3. Descriptive statistics
4. Monthly revenue analysis
5. Quarterly revenue analysis
6. Customer age-group analysis
7. Gender distribution analysis
8. Top 10 products by order quantity
9. Revenue and profit analysis by product category
10. Profit margin analysis
11. Correlation analysis using a heatmap
12. Additional visualization for category profit margins
13. Business insights and recommendations

## Key Insights

- December recorded the highest overall monthly revenue, while July and August showed comparatively lower revenue.
- Adults aged 35–64 represented the largest age group by transaction records.
- Bikes generated the highest revenue of approximately **61.43 million** and the highest total profit of approximately **20.40 million**.
- Accessories achieved the highest profit margin at approximately **58.63%**, compared with **33.92%** for Clothing and **33.21%** for Bikes.
- Water Bottle - 30 oz. was the highest-selling product by order quantity.
- Unit Cost and Unit Price showed an extremely strong positive correlation of approximately **0.998**.
- Profit and Revenue showed a very strong positive correlation of approximately **0.957**.
- Customer Age showed very little linear relationship with Revenue and Profit.

## Business Recommendations

1. **Increase Accessories Cross-Selling**  
   Promote high-margin accessories such as bottles, repair kits, and tubes alongside bike purchases to improve overall profitability.

2. **Focus on the Bikes Category**  
   Maintain sufficient inventory and use targeted promotions for strong-performing bike products because Bikes are the largest contributor to total revenue and profit.

3. **Optimize Inventory for High-Demand Products**  
   Products with high order quantities, such as Water Bottle - 30 oz. and Patch Kit/8 Patches, should be considered for inventory planning, bundles, and promotional campaigns.

## Conclusion

The analysis provides useful insights into sales trends, customer demographics, product demand, category performance, and profitability.

Bikes are the strongest category in terms of total revenue and profit, while Accessories have the highest profit margin. The findings can support inventory planning, cross-selling, product promotion, and profitability-focused business decisions.

## Project Structure

```text
Retail-Sales-EDA/
│
├── Data/
│   └── Raw/
│       └── Retail_Sales_EDA.csv
│
├── Notebook/
│   └── Retail_Sales_EDA.ipynb
│
└── README.md

