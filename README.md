# **Grafana_Dashboard**

# **Furniture Data Insights**

**Objective**

This project utilizes advanced data analysis and visualization techniques to understand trends in furniture sales and operational efficiency. By analyzing key metrics such as sales, profit margins, inventory levels, and delivery performance, the goal is to identify actionable insights that drive business decisions. The dashboard has been designed to provide an intuitive overview of critical KPIs, enabling stakeholders to monitor and optimize business operations effectively.

**Dataset Overview**

**1. Source and Scope**

The dataset used for this project consists of detailed records of furniture sales transactions. It includes 12,000 rows and 15 columns, collected over the past two years from a retail furniture business operating across various regions. The data encompasses multiple dimensions such as pricing, product categories, inventory, and customer behavior, providing a comprehensive basis for analysis.

**2. Attributes**

The dataset includes a mix of numerical, categorical, and temporal features:

1. Order_ID: Unique identifier for each sales order.
2. Product: Description of the furniture item sold.
3. Categories: Chair, Table, Sofa, Bed, Cabinet, etc.
4. Material: Material type of the furniture (e.g., Wood, Metal, Plastic).
5. Region: Geographical area of the transaction (e.g., North, South, East, West).
6. Price (₹): Selling price of the furniture item.
7. Cost (₹): Cost price of the furniture item.
8. Profit Margin (%): Percentage profit earned on each sale.
9. Sales (₹): Total sales amount for each transaction.
10. Discount (%): Discount offered on the item.
11. Inventory_Level: Stock levels before the transaction.
12. Delivery_Days: Number of days taken for delivery.
    
**3. Dataset Features**

Volume: 12,000 rows
Data Collection Period: 2 years
Format: CSV (pre-ingestion)

**Data Ingestion Process**

Step 1: Data Preprocessing
Header Standardization:
Column names were standardized by converting them to lowercase and removing spaces (e.g., Order_ID → order_id).

Feature Categorization:

Numerical Features: price, cost, profit_margin, sales, discount, delivery_days.
Categorical Features: product, material, region, default_risk.
Temporal Features: date.
Handling Missing Data:
Missing values in customer_rating and profit_margin were imputed using mean and median values respectively.

Step 2: Data Transformation
Derived Features:

Profit Amount (₹) = Sales (₹) - Cost (₹).
Discount Impact: Calculated to evaluate the effect of discounts on sales performance.
Format Conversion:
Dates were converted to a standard YYYY-MM-DD format for time-series analysis.

Step 3: Data Loading
The dataset was loaded into a MongoDB database for dashboard creation.
ETL Process:
A Python-based ETL (Extract, Transform, Load) pipeline was developed to automate data cleaning, transformation, and loading.

**Dashboard**
![dashboard 1](https://github.com/user-attachments/assets/8ca015db-b255-4b01-96fa-3c67a5083a91)




![dashboard 2](https://github.com/user-attachments/assets/16b97212-449e-4478-87eb-35a7aa92cfa7)



**Dashboard Video**






https://github.com/user-attachments/assets/3b795ab6-b1c1-434a-88dc-876f2a72b937










