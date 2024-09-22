Customer Segmentation Using K-Means Clustering
Project Overview

This project aims to segment customers based on their transactional behavior and demographics using unsupervised machine learning. By identifying distinct customer groups, we can target each segment with personalized coupon offers to increase customer loyalty and satisfaction. The dataset consists of information on customers, their transactions, and branch and merchant data, with features such as the number of transactions, coupon usage, and recency of transactions.
Dataset

The project uses a dataset comprising six interrelated tables:

    Customers: Customer ID, join date, city, gender.
    Genders: Gender ID and gender name.
    Cities: City ID and city name.
    Transactions: Details about customer transactions, including the coupon claimed, status (claimed, burnt), transaction date, and branch.
    Branches: Branch and merchant details.
    Merchants: Merchant details.

Key features used for segmentation:

    Transaction Count: Total number of transactions per customer.
    Burned Count: Number of coupons that were claimed and used by the customer.
    Recency Days: Number of days since the customer's last transaction.

Model Approach

We used the K-Means Clustering algorithm to segment the customers based on their behavioral patterns. The steps involved:

    Data Preprocessing:
        Merging multiple tables to create a complete view of customer transactions and demographics.
        Calculating key features such as transaction count, coupon usage (burned vs claimed), and recency.
        Handling missing data by filling with appropriate values.

    Feature Selection: We selected three key features for clustering:
        transaction_count
        burned_count
        recency_days

    Clustering: We applied the K-Means algorithm with 3 clusters after testing various configurations and evaluating them using the silhouette score.

    Dimensionality Reduction: We used Principal Component Analysis (PCA) to visualize the clusters in a two-dimensional space and better understand customer groupings.

Evaluation Metrics

To evaluate the performance of the clustering, we used the following metric:

    Silhouette Score: This metric measures how well each point lies within its cluster. The score ranges from -1 to 1, where a higher score indicates better-defined clusters. A score of 0.62 was achieved, suggesting a good clustering outcome.

Key Findings

The K-Means clustering algorithm identified three distinct customer segments:
Cluster 0: High-Engagement Customers

    Behavior: Customers in this group frequently make transactions and redeem coupons. They have a low recency, meaning they’ve made purchases recently.
    Recommendation: These customers should be prioritized for loyalty rewards and exclusive offers to maintain their high engagement.

Cluster 1: Previously Active but Dormant Customers

    Behavior: These customers were once active but have become less engaged over time. Their last transaction was a long time ago.
    Recommendation: Use win-back campaigns with significant discounts and time-sensitive offers to re-engage this group.

Cluster 2: Low-Engagement or New Customers

    Behavior: These customers are either new or infrequent shoppers with few transactions and low coupon engagement.
    Recommendation: Encourage more frequent purchases through welcome offers, small purchase incentives, and free shipping.

Conclusion

The customer segmentation provided insights into distinct customer behaviors. By targeting each segment with tailored coupon strategies, we can potentially boost customer loyalty and overall satisfaction. Future steps involve implementing and tracking the effectiveness of these strategies in real-time.
