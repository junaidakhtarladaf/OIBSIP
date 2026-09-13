# Customer Segmentation Analysis

## Oasis Infobyte – Data Analytics Internship

### Task 2: Customer Segmentation Analysis

This project focuses on segmenting e-commerce customers based on their purchasing behaviour using RFM analysis and K-Means clustering.

## Objective

The objective of this analysis is to identify distinct customer groups based on their purchasing behaviour and provide targeted marketing recommendations for each segment.

## Dataset

The analysis uses the **Online Retail Dataset** containing transactional data from a UK-based online retail business.

The dataset includes information such as:

- Invoice Number
- Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Analysis Performed

### 1. Data Inspection and Cleaning

The dataset was inspected for its structure, data types, missing values, and duplicate records.

Data cleaning included:

- Removing transactions with missing Customer IDs
- Removing cancelled invoices
- Removing invalid quantities and prices
- Removing duplicate records

### 2. Customer Purchase Metrics

The following metrics were calculated:

- Average Purchase Value
- Average Purchase Frequency
- Average Customer Lifetime Value

### 3. RFM Analysis

Customer behaviour was analysed using three key features:

- **Recency** – How recently a customer made a purchase
- **Frequency** – Number of purchases made by a customer
- **Monetary** – Total amount spent by a customer

### 4. Feature Scaling

The RFM features were standardized using `StandardScaler` before applying clustering.

### 5. K-Means Clustering

The Elbow Method was used to determine a suitable number of clusters.

Based on the analysis, **5 customer clusters** were selected for the K-Means model.

### 6. Cluster Visualization

Customer segments were visualized using scatter plots based on different combinations of RFM features.

### 7. Cluster Profiling

Each cluster was profiled using the average Recency, Frequency, and Monetary values to understand customer behaviour.

## Customer Segments

The analysis identified five customer segments:

- **Regular Customers** – Customers with moderate purchasing activity
- **At-Risk / Lost Customers** – Customers with low engagement and long periods since their last purchase
- **High-Value Loyal Customers** – Customers with high purchase frequency and spending
- **Loyal Customers** – Customers with recent purchases and strong spending behaviour
- **VIP Customers** – Customers with very high purchase frequency and monetary value

## Key Insights

- A small group of customers contributes very high purchase frequency and spending, making them important high-value segments.
- Customers with low engagement and long periods since their last purchase require reactivation strategies.
- Regular and loyal customers provide opportunities for increasing purchase frequency through targeted offers and loyalty programs.

## Marketing Recommendations

- Retain VIP and high-value customers through exclusive rewards, personalized offers, and premium benefits.
- Reactivate at-risk or lost customers through targeted discounts, reminders, and relevant product recommendations.
- Develop regular and loyal customers through loyalty programs and personalized promotions to increase purchase frequency and customer value.

## Conclusion

The customer segmentation analysis successfully grouped customers into five distinct segments using Recency, Frequency, and Monetary value. These segments provide useful insights into customer purchasing behaviour and can support targeted marketing, customer retention, and reactivation strategies.

## Project Structure

```text
DataAnalytics-L1-CustomerSegmentation/
│
├── Data/
│   └── Online Retail.xlsx
│
├── Notebook/
│   └── Customer_Segmentation.ipynb
│
└── README.md