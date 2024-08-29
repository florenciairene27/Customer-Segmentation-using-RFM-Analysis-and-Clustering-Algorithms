# Customer-Segmentation-using-RFM-Analysis-and-Clustering-Algorithms

In marketing, customer segmentation is the process of dividing customers into distinct groups. Why? So that marketers can better understand the behaviors, trends, and patterns of these groups and tailor marketing strategies accordingly. In today’s digital era, accurately segmenting customers is crucial for optimizing marketing efforts and achieving a higher return on investment.

Traditionally, many marketers have relied on subjective methods to segment customers, manually grouping them based on specific thresholds in the data. While simple and intuitive, this approach becomes increasingly difficult to apply as the number of variables or features grows.

To address this challenge, I decided to explore the use of unsupervised machine learning—specifically clustering techniques—to segment customers. Clustering algorithms are powerful because they can detect patterns in data that may be too complex for humans to identify. Among the many clustering methods available, this project will focus on the most popular ones: agglomerative clustering, prototype-based clustering (like k-means), and Gaussian-based clustering.

By applying multiple algorithms, my goal is to determine which method yields the most meaningful and actionable customer segments. The main challenge in clustering is finding clusters that genuinely reflect the underlying structure of the data, and since no single algorithm works best for all datasets, the choice of method must be tailored to the specific characteristics of the data.

Alongside applying clustering algorithms to find meaningful segments, I will also seek to derive valuable insights through the usual data science pipeline, for example through exploratory data analysis (EDA), and provide how these insights could be applicable directly to the business.

# Table of Contents
- **Business Problems**
- **Data Source**
- **Method**
- **Results**
- **Conclusion**
- **Limitations and Recommendations**
- **How to use the Files**

# Business Problems

Can we identify meaningful customer segments based on their purchasing behavior?If so, how can we tailor strategies for each of these segments?

# Data Source

Source: [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)
Description:  The dataset is  obtanied from UCI Machine Learning. The data itself is a transactional data from a Uk non-store online retail between 01/12/2010 and 09/12/2011, contains 541909 observations.

# Methodology

- Data Preprocessing
- Exploratory Data Analysis
- Clustering Algorithms:
  - Feature Engineering : RFM Analysis
  - Kmeans, Hierarchical clustering, Gaussian Mixture Model
- Evaluation:
  - Cluster Visualization: PCA 

# Tech Used 
- R (for Data preprocessing & Visualization)
- Python (for Clustering)

# Results
1. **Data Visualization**
   
   - **Total Purchases by each Country**
     
   <img src="EDA%20images/Percentage_of_Total_Purchases.png" alt="Geospatial Distribution of Total Purchases" width="400"/><img src="EDA%20images/total_purchases_by_country.png" alt="Percentage of Total Purchases by Country" width="400"/>
   
   - **Top Selling Items**
     
   <img src="EDA%20images/top 10 item sold.png" alt="top 10 item sold" width="400"/> <img src="EDA%20images/Top 5 Item Sold.png" alt="Top 10 Ttem Sold" width="400"/>

   - **Sales Trends**
     
   <img src="EDA%20images/sales_trends.png" alt="sales_trends" width="400"/>

   **Marketing Insights:**
   
   1. **Leverages Regional Insights**
      - **Insight** : UK accounts for the highest percentage of total purchases and has the highest order volume, follow by Netherlands, Ireland and Germany
      - **Recommendation**: Tailor marketing strategies to focus on high-performing regions, and explore opportunities to enhance market presence in regions with lower sales but potential for growth. To refine this approach, conduct further analysis to understand the types of products that are popular in these high-performing regions
   3. **Monitor Order Volume Trends**
      - **Insight**: The size of the points in the visualization represents order volume, highlighting the regions with higher sales volumes.
      - **Recommendation**: Use order volume insights to identify key markets and allocate resources effectively. Prioritize customer service and inventory management in regions with high order volumes to maintain customer satisfaction and support sustained growth.
   5. **Address the January Sales Drop**
      - **Insight**: Sales experience a dramatic decline in January.
      - **Recommendation**: Investigate the factors contributing to this drop. It might be related to seasonal buying patterns, post-holiday fatigue, or other market dynamics. Consider implementing strategies to boost sales during this period, such as special promotions, product bundles, or targeted marketing campaigns to re-engage customers.
   7. **Focus on Peak Sales Periods**
      - **Insight**: The highest sales increases are observed in September, October, and November, with November reaching its peak.
      - **Recommendation**: Plan marketing campaigns and promotions to capitalize on these peak months. Consider increasing advertising spend, launching special offers, and enhancing product visibility during these months to maximize revenue.
     
2. **Clustering Algorithms**
   
   - **Feature Engineering**
     
     After creating RFM variables, here's the distribution of each of these variables
     
     <img src="EDA%20images/1.jpg" alt="RFM Distribution" width="600"/>

   - **K-means Clustering**
     
     Using elbow and silhoutte plots the best segments are 4, here's the visualization of how data divided to 4 segments using k-means
     
     <img src="EDA%20images/2.jpg" alt="RFM Distribution" width="600"/>
     
   - **Hierarchical Clustering**
     
     Here's the visualization of how hierarchichal clustering divided data into 4 segments
     
     <img src="EDA%20images/3.jpg" alt="RFM Distribution" width="600"/>

   - **Gaussian Mixture Clustering**

     Here's the visualization of how gaussian mixture divided data into 4 segments

     <img src="EDA%20images/4.jpg" alt="RFM Distribution" width="600"/>

     Based on the PCA and 3D visualizations, as well as the clarity of cluster separation, I decided to proceed with the K-means algorithm. The K-means results identify 4 distinct segments, which are visualized using boxplots and summarized by their mean values in the table below:

     <img src="EDA%20images/k-means_boxplot.png" alt="k-means_boxplot" width="400"/> <img src="EDA%20images/Cluster_table.png" alt="Cluster_table" width="400"/>
     We can also use percentiles: 25th, 50th (median), and 75th percentiles to understand the distribution of each cluster and the treshold:
     
     <img src="EDA%20images/percentiles_output.png" alt="percentiles_output" width="400"/>

# Conclusion & Recommendation

Finally, the conclusion of this analysis is that there 4 segment of customers based on their purchasing behaviour. These 4 segments and marketing strategy for each of the segment:
- **Cluster 0**: High value and frequent customers, but their last purchase was relatively recent.
  - *Recommendation*: Re-engagement Campaigns
    
  - *Action*: Encourage more frequent purchases by sending targeted promotions or incentives, such as limited-time offers or bundle deals. Highlight the benefits of staying active with the brand
    
  - *Goal*: Increase purchase frequency and reduce the gap since their last purchase by re-engaging them with appealing offers.
  
- **Cluster 1**: Moderate-value customers who have made recent purchases, indicating potential for re-engagement.
  
  - *Recommendation*: Upselling & Cross-Selling
    
  - *Action*: Leverage their recent purchase activity by offering complementary products or upselling to higher-value items. Provide tailored recommendations based on their purchase history.
    
  - *Goal*: Boost average order value and further engage these customers by introducing them to products that align with their recent interests.
    
- **Cluster 2**:  Low-value customers with infrequent purchases and long periods of inactivity.
  
  - *Recommendation*: Win-Back Campaigns
    
  - *Action*: Implement win-back campaigns to re-engage these inactive customers. Consider offering deep discounts, personalized messages, or reactivation incentives to encourage them to return.
    
  - *Goal*: Revitalize their interest in the brand and convert them from inactive to active customers by addressing potential reasons for their disengagement.

- **Cluster 3**:  The store most valuable and active group, with high-frequency, high-monetary, and low-recency values, indicating highly engaged and valuable customers.
  
  - *Recommendation*: Loyalty Rewards & VIP Programs
    
  - *Action*: Offer exclusive rewards, discounts, or VIP programs to maintain their loyalty. Consider creating personalized offers based on their purchasing history to make them feel valued.
    
  - *Goal*: Strengthen customer retention by rewarding their frequent and high-value purchases, ensuring they remain engaged with the brand.

# Limitations and Recommendations

# How to use the Files

