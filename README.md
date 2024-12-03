# **Grafana_Dashboard**

# **Furniture Data Insights**

**Objective**

This project utilizes advanced data analysis and visualization techniques to understand trends in furniture sales and operational efficiency. By analyzing key metrics such as sales, profit margins, inventory levels, and delivery performance, the goal is to identify actionable insights that drive business decisions. The dashboard has been designed to provide an intuitive overview of critical KPIs, enabling stakeholders to monitor and optimize business operations effectively.

**Dataset Overview**

**1. Source and Scope**

The dataset used for this project consists of detailed records of furniture sales transactions. It includes 12,000 rows and 15 columns, collected over the past two years from a retail furniture business operating across various regions. The data encompasses multiple dimensions such as pricing, product categories, inventory, and customer behavior, providing a comprehensive basis for analysis.

**2. Attributes**

The dataset includes a mix of numerical, categorical, and temporal features:

1. Categories: Chair, Table, Sofa, Bed, Cabinet, etc.
2. Location: Area where selling Product (Rural, Urban etc)
3. Season: Different types of Season (Summer , Winter etc)
4. Store Type: Types of stores where selling the product (Online, Retail etc)
5. Material: Material type of the furniture (e.g., Wood, Metal, Plastic).
6. Region: Geographical area of the transaction (e.g., North, South, East, West).
7. Price (₹): Selling price of the furniture item.
8. Cost (₹): Cost price of the furniture item.
9. Profit Margin (%): Percentage profit earned on each sale.
10. Sales (₹): Total sales amount for each transaction.
11. Discount (%): Discount offered on the item.
12. Inventory_Level: Stock levels before the transaction.
13. Delivery_Days: Number of days taken for delivery.
    
**3. Dataset Features**

Volume: 3000 rows
Format: CSV (pre-ingestion)


**Data Ingestion Process**

Step 1: Data Preprocessing
Header Standardization:
Column names were standardized by converting them to lowercase and removing spaces.

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


Step 3: Data Loading
The dataset was loaded into a Influxdb database for dashboard creation.
ETL Process:
A Python-based ETL (Extract, Transform, Load) pipeline was developed to automate data cleaning, transformation, and loading.



**Dashboard**


![dashboard 1](https://github.com/user-attachments/assets/8ca015db-b255-4b01-96fa-3c67a5083a91)




![dashboard 2](https://github.com/user-attachments/assets/16b97212-449e-4478-87eb-35a7aa92cfa7)










**Dashboard Video**








https://github.com/user-attachments/assets/3b795ab6-b1c1-434a-88dc-876f2a72b937



**Graphs Included in the Dashboard**

1. Total Sales by Material
   
Question: How do total sales vary by material type?

Key Observations:

Significant variations in sales across different material types.
Notable high sales in certain materials, indicating popular preferences.

Insights:

Understanding material popularity can guide inventory and marketing strategies.

2. Sales Trend Over Time

Question: How do total sales fluctuate over time?

Key Observations:

Clear trends in sales over specific periods.
Potential peaks and troughs indicating seasonal trends.

Insights:

Identifying sales trends can help in forecasting and planning.

3. Average Delivery Days

Question: What is the average delivery time for products?

Key Observations:

Average delivery days provide insight into supply chain efficiency.
Notable variations in delivery times across different categories.

Insights:

Streamlining delivery processes can improve customer satisfaction.

4. Total Sales by Season

Question: How do sales vary across different seasons?

Key Observations:

Seasonal trends showing high sales in specific seasons.
Impact of seasonality on overall sales performance.

Insights:

Seasonal promotions and stock adjustments can maximize sales.

5. Total Sales by Store Type

Question: How do sales compare between online and retail stores?

Key Observations:

Balance of sales between online and retail channels.
Potential dominance of one channel over the other.

Insights:

Channel-specific strategies can optimize sales performance.

6. Total Sales by Category

Question: How do sales vary across different product categories?

Key Observations:

Significant differences in sales among categories.
Categories with consistently high or low sales.

Insights:

Category-specific marketing can enhance sales.

7. Average Profit Margin

Question: What are the profit margins for different categories?

Key Observations:

Variation in profit margins indicating profitability of categories.
High margin categories may require focused attention.

Insights:

Profit optimization strategies can be developed for lower margin categories.

8. Sales by Brand

Question: Which brands generate the most sales?

Key Observations:

Top-performing brands with high sales volumes.
Brands with lower sales indicating potential for growth.

Insights:

Brand partnerships and promotional efforts can boost sales.

9. Maximum Price

Question: What is the highest price point for products sold?

Key Observations:

Identifying premium product segments.
Potential pricing strategy adjustments for high-end products.

Insights:

Premium pricing strategies can be applied to maximize revenue.

10. Sales by Host

Question: How do different hosts impact sales?

Key Observations:

Host-specific sales performance.
Identifying top-performing hosts.

Insights:

Leveraging successful hosts can drive sales.

**Insights from Dashboard**

1. Total Sales by Material

The highest sales were generated by material type D (102 units), indicating its popularity. Materials B and C (40 and 42 units) are performing moderately.

2. Sales Trend Over Time

The dashboard highlights total sales of 242, suggesting steady demand for furniture over the analyzed period.

3. Average Delivery Days

The average delivery time for products is 3.86 days, which is relatively low and may positively impact customer satisfaction.

4. Total Sales by Season

Spring season leads with 139 sales, followed by Fall (82 sales). This indicates a seasonal peak in spring, while summer (21 sales) sees lower demand.

5. Total Sales by Store Type

Retail and online sales are almost evenly split (49% retail, 51% online). This indicates equal importance of both sales channels.

6. Maximum Price

The maximum price of a product sold is 486 units, showing the willingness of some customers to purchase high-value items.

7. Average Profit Margin

The profit margin averages 29.2%, indicating healthy profitability in the furniture segment.

8. Sales by Brand

Brand A dominates sales (98 units), while Brands C and D lag behind (64 and 38 units, respectively).

9. Sales by Season Over Time

The Spring season consistently outperforms other seasons in terms of sales. Summer sales remain significantly low, possibly indicating off-peak demand.

10. Sales by Category Over Time

Beds and Chairs lead in sales, indicating customer preference towards these categories. Sofas have comparatively lower sales, highlighting a potential area for improvement.

11. Sales by Category and Store Type

The Sofa category in Retail stores performs better (77 sales) than online platforms.Beds and Chairs have higher sales online than in retail, suggesting category-wise platform preferences.

12. Sales by Host and Category

Chair sales by Host A dominate (101 sales), showing significant demand in this category. Sofas and Beds have balanced contributions.

13. Average Profit Margin by Category

The Sofa category contributes the highest profit margin (49%), followed by Beds and Chairs (27% and 24%, respectively).

14. Sales by Host

The total sales contributed by all hosts is 242, emphasizing the collective effort and performance across categories and hosts.


**Managerial Implications**

1. Seasonal Trends: Inventory and Promotional Activities
   
    a. Focus on Spring: With Spring showing the highest sales figures (139 units), it is essential to ensure adequate 
 inventory of high-demand products like Chairs and Sofas during this season. Promotions and marketing campaigns should 
 also be intensified to capitalize on the natural uptick in demand.
      
   b. Addressing Summer Slump: Sales in Summer (21 units) are notably low, indicating an opportunity to drive demand 
 through innovative approaches. Consider launching summer-special offers, discounts, or bundled deals to attract 
 customers. Additionally, focus on promoting lightweight, summer-friendly furniture or outdoor categories that may align 
 with seasonal preferences.

2. Channel Optimization: Retail vs. Online
   
   a. Balanced Strategy: The nearly equal contribution of retail (51%) and online (49%) sales indicates the need to maintain a balanced focus on both channels. This 
      includes tailoring strategies to leverage the unique strengths of each channel.

   b. Improving Underperforming Categories: Identify categories that underperform in specific channels and implement targeted measures. For example:

   c. Online: Optimize product descriptions, enhance visuals, and offer free shipping for categories like Beds or Sofas.

   d. Retail: Train staff to upsell products and create immersive store displays to enhance the appeal of high-demand categories.

3. High-Profit Categories: Focus on Sofas

    a. Maximizing Profits: With Sofas contributing the highest profit margin (49%), ensure that they are well-stocked across all seasons and prominently featured in 
      marketing campaigns.

    b. Cross-Selling Opportunities: Use Sofas as a hook product to encourage cross-selling complementary items, such as cushions or coffee tables, to boost overall sales 
      per transaction.

   c. Promotions for Growth: Offer premium options or limited-edition collections within the Sofa category to attract high-value customers.

4. Brand Strategies: Boosting Underperforming Brands

    a. Addressing Brand C and D: With lower sales figures (38 and 64 units, respectively), it is vital to diagnose the root cause of underperformance. This could include 
      revisiting pricing strategies, redesigning products to meet market trends, or launching specific promotional campaigns for these brands.

    b. Strengthening Brand A: Brand A leads with 98 units sold. Invest in maintaining its market dominance through loyalty programs, exclusive offerings, or partnerships 
       to enhance customer retention and brand perception.

7. Delivery Efficiency as a Competitive Advantage

   a. Leverage Fast Delivery Time: The average delivery time of 3.86 days is a key strength. Highlight this as a competitive advantage in marketing materials, emphasizing 
      speedy service to differentiate from competitors.

   b. Enhancing Logistics: Further optimize delivery times by partnering with efficient logistics providers and improving warehouse operations. Consider offering same-day 
      or next-day delivery options for select categories to attract time-sensitive customers.

   c. Customer Satisfaction: Use the fast delivery time to build customer trust and satisfaction, potentially boosting repeat purchases and positive reviews.


**Key Learnings from the Project**

1. Real-Time Sales Monitoring

Real-time data visualization provides immediate insights into sales trends, delivery times, and profit margins. This enables decision-makers to address issues promptly, optimize operations, and capitalize on opportunities during high-demand periods like Spring.

2. Data-Driven Inventory Management

The analysis highlights seasonal and category-specific trends, guiding inventory decisions. For instance, higher sales in Spring and the dominance of categories like Chairs and Beds suggest the need for seasonal stocking and category prioritization.

3. Importance of Channel-Specific Insights

Comparing retail and online performance reveals the strengths of each channel for different categories. This learning underscores the need to develop tailored strategies for retail and online platforms, maximizing sales opportunities.

4. Cross-Category Profitability Analysis

Understanding profit margins by category demonstrates the value of focusing on high-margin items like Sofas. This learning can help in designing targeted marketing strategies to enhance profitability.

5. Effective Use of Visualizations for Stakeholders

The project demonstrates how visual representations, like pie charts, bar graphs, and gauges, simplify the understanding of complex sales data. These visualizations make it easier for stakeholders to grasp key trends and patterns, aiding in informed decision-making.

6. Customization of Dashboards

The ability to customize metrics, such as focusing on Seasonal Sales or Store Type Performance, makes the dashboard versatile and relevant to diverse business needs. Customization enhances the utility of the dashboard across management levels.
