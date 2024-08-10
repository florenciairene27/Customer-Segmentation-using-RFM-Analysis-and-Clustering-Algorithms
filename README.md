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
- Clustering Algorithms: Kmeans, Hierarchical clustering, Gaussian Mixture Model
- Evaluation:
  - Visualization: PCA 

# Tech Used 
- R (for Data preprocessing & Visualization)
- Python (for Clustering)

# Results
1. Data Visualization
<div style="display: flex; justify-content: space-between;">

  <div style="flex: 1; text-align: center;">
    <img src="EDA%20images/Percentage_of_Total_Purchases.png" alt="Geospatial Distribution of Total Purchases" width="300"/>
    <p><strong>Geospatial Distribution of Total Purchases</strong></p>
  </div>

  <div style="flex: 1; text-align: center;">
    <img src="EDA%20images/total_purchases_by_country.png" alt="Percentage of Total Purchases by Country" width="300"/>
    <p><strong>Percentage of Total Purchases by Country</strong></p>
  </div>

</div>

   - **Geospatial Distribution of Total Purchases**
     
   <img src="EDA%20images/Percentage_of_Total_Purchases.png" alt="Geospatial Distribution of Total Purchases" width="400"/>
   

   - **Percentage of Total Purchases by Country**
   <img src="EDA%20images/total_purchases_by_country.png" alt="Percentage of Total Purchases by Country" width="400"/>

   - **Top **

   
   
3. Clustering Algorithms


# Conclusion
# Limitations and Recommendations
# How to use the Files

