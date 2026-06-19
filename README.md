# Zepto Inventory & Sales Analysis - SQL
A SQL-based analysis of Zepto's product inventory data. Zepto is an Indian quick-commerce platform and I wanted to dig into how their pricing, discounts, and stock availability actually look across categories.

### **Why I did this**
I use Zepto pretty regularly and was curious about the pricing patterns — which categories get the most discounts, which high-priced items go out of stock, whether the per-gram pricing actually makes sense across products. Turned that curiosity into a structured SQL project.

### **Dataset**
Zepto Inventory Dataset — Kaggle
🔗 https://www.kaggle.com/datasets/palvinder2006/zepto-inventory-dataset/data?select=zepto_v2.csv
Contains product-level data including category, MRP, discounted price, discount percentage, available quantity, weight, and stock status.

### **What I covered**
* Data Exploration

Row count and sample preview
Null value check across all columns
Distinct product categories
In-stock vs out-of-stock product count
Products with duplicate SKUs

* Data Cleaning

Removed products where MRP = 0 (invalid entries)
Converted prices from paise to rupees

* Analysis

Top 10 best-value products by discount percentage
High MRP products (above ₹300) that are currently out of stock
Estimated revenue per category based on available inventory
Products with MRP above ₹500 but discount below 10% - low value deals
Top 5 categories with the highest average discount
Price per gram for products above 100g — finding the best value by weight
Product weight segmentation - Low, Medium, and Bulk
Total inventory weight per category


* A few things I found

Some categories consistently offer 40–50% discounts while others barely cross 10% — the discount strategy is clearly not uniform
Several high-MRP products (₹300+) are out of stock, which is a revenue loss hiding in plain sight
Price per gram varies wildly even within the same category - some products are priced 3-4x higher per gram than similar ones
A handful of categories hold the bulk of total inventory weight, suggesting Zepto prioritizes stocking certain segments heavily


### **Tech Stack**

PostgreSQL        
Raw SQL - no Python or BI tools, just queries

### Rishav Raj



