# Assignment 5 – Unsupervised Learning for Pattern Discovery and Product Segmentation

## Business Problem

NovaMart Retail is a mid-sized retail company that sells everyday products through physical stores and an online channel. The business wants to improve inventory and marketing decisions by understanding patterns across product records.

The main problem is that products behave differently. Some products have high demand, some have high stock, some are lower-cost everyday items, and some are higher-priced premium products. If NovaMart treats every product the same way, it may waste marketing resources, create overstock, or miss products that need more attention.

## Dataset

The dataset used in this assignment is `novamart_inventory_reorder_dataset.xlsx`.

The dataset contains product, sales, inventory, pricing, customer rating, return rate, website views, supplier, and competitor information.

## Clustering Method

The machine learning method used is **K-means clustering**.

K-means is an unsupervised learning method. This means that the model does not use a target variable to make predictions. Instead, it groups products based on similar numerical patterns.

The selected numerical features were scaled before clustering because K-means is distance-based and can be affected by different measurement scales.

## Features Used for Clustering

The numerical features used for clustering were:

- Current_Stock_Units
- Average_Weekly_Sales
- Lead_Time_Days
- Unit_Cost
- Selling_Price
- Discount_Rate
- Customer_Rating
- Return_Rate
- Website_Views
- Competitor_Price_Index

## Number of Clusters

The Elbow Method was used to compare different values of k. Based on the elbow chart and business interpretability, **3 clusters** were selected.

Three clusters were selected because they provide clear and practical product segments that managers can understand and use for marketing and inventory decisions.

## Main Results

The model identified three product segments:

### Cluster 0 – High Demand / High Stock Products

This segment contains 102 products. These products have high current stock, high average weekly sales, strong website views, and longer lead times.

Business meaning: These products are important revenue drivers and should be monitored carefully to avoid stockouts.

Recommended action: Maintain strong inventory planning, protect availability, and use marketing campaigns to continue demand.

### Cluster 1 – Low-Cost Moderate Demand Products

This segment contains 124 products. These products have lower unit cost, lower selling price, moderate weekly sales, and moderate website views.

Business meaning: These products may support everyday purchases and regular customer traffic.

Recommended action: Use bundles, small discounts, cross-selling, and everyday-value promotions.

### Cluster 2 – Premium Low-Stock Products

This segment contains 134 products. These products have the highest unit cost and selling price, lower stock levels, lower average weekly sales, and the highest reorder-needed rate.

Business meaning: These products may be higher-value items that require careful marketing and inventory decisions.

Recommended action: Use targeted marketing, avoid unnecessary broad discounts, protect margins, and monitor reorder needs closely.

## Visualizations

The notebook includes visualizations to support the analysis:

- Elbow Method plot
- Scatter plot of Average Weekly Sales and Current Stock Units
- Bar chart comparing average product characteristics by cluster
- Box plot comparing selling price by cluster

Each visualization includes a business interpretation explaining what the chart shows and how NovaMart can use the result.

## Business Recommendation

NovaMart should use the clustering results to create different marketing and inventory strategies for each product segment.

High-demand products should receive strong inventory monitoring and availability protection. Low-cost moderate-demand products should be used in bundles and value-based promotions. Premium low-stock products should receive targeted marketing and careful reorder planning to protect profit margins.

This segmentation analysis can help NovaMart improve marketing efficiency, reduce stockout risk, avoid unnecessary overstock, and make better data-driven decisions.

## Limitation

One limitation is that the dataset is synthetic and simplified for teaching purposes. It may not include all real-world factors such as supplier disruptions, competitor promotions, local events, advertising campaigns, weather, or sudden demand changes.

Another limitation is that K-means forces every product into one cluster, even when some products may share characteristics with multiple groups.

## Responsible AI Reflection

K-means clustering should support business decisions, not replace human judgment. If NovaMart uses clusters without human review, it may over-prioritize established products with high website views and under-support new products with limited history.

Managers should review the clusters alongside business context, planned promotions, supplier delays, and seasonal demand before making final marketing or inventory decisions.
