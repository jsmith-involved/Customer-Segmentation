# Capstone: Customer Segmentation Analysis

### Problem Statement

Help Fresh Harvest Grocers, operating on a tight budget, optimize its product offerings by identifying the customer segment most likely to make purchases. By focusing on this particular segment, the company can efficiently allocate resources, ensuring that marketing efforts are directed towards customers with a higher likelihood of converting. This strategic approach maximizes the return on investment by minimizing marketing to customers less inclined to make purchases.

### Data Dictionary 
| Feature | Type | Dataset | Description |
| --- | --- | --- | --- |
| Enrollment_Age | int | cleaned_df.csv | Age of customer at time of enrollment|
| Tot_Dependents | int | cleaned_df.csv | Total number of children customers have |
| Tot_AccptCmp | int | cleaned_df.csv | Total number of campaigns accepted by customer |
| Income_Level | object | cleaned_df.csv | Income classifcation of customer |
| Days_Enrolled | int | cleaned_df.csv | Length of customer loyalty in days from enrollment date |
| Household_Size | int | cleaned_df.csv | Total number of members in customer's household |

A more detailed data dictionary can be viewed [here](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis/data)

# Summary

| Model |Silhouette Score | |
| --- | --- | --- |
| **KMeans** | 0.13 |

I selected KMeans as the clustering algorithm and evaluated its performance using the silhouette score. Given the abundance of features in the model—over 20—I addressed feature dimensionality by employing PCA. The aim was to retain principal components explaining at least 95% of the variance, ensuring a comprehensive representation of the data. 

To determine the optimal number of clusters, I utilized the elbow method, a reliable technique for pinpointing the inflection point where the rate of decrease in inertia slows down notably. Evaluating cluster quality with the silhouette score, my model achieved a commendable score of 0.13, indicative of moderately well-separated clusters. 

##### Key Findings
The majority of customers are concentrated within cluster 3, with cluster 1 following closely in terms of customer count. Aross all segments, many the majority of customers have a Bachelor's degree. Customers in cluster 2 have substantial spending behaviors within the company, surpassing all other clusters. They have preference for wine products, with customers in cluster 0 being the second top spender in the category.

##### Next Steps?
To maximize marketing efforts, Fresh Harvest Grocers should focus on tailoring wine campaigns specifically for customers in segment 2. These customers typically fall into the demographic of individuals in their late 50s with a Bachelor’s Degree, and they have been enrolled for an average of approximately 3938 days. Targeting this segment is strategic as they demonstrate a higher likelihood of accepting campaigns compared to their overall customer base. Segment 2 customers also exhibit greater spending rates in the wine category, presenting an opportunity to retain more revenue.
# Sources
[Income Level Classification](https://finance.yahoo.com/news/income-fall-americas-lower-middle-122100515.html)

[Education Level Classification](https://www.studera.nu/startpage/higher-education/sweden/levels-degrees/#;h20)