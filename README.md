# Amazon_Vine_Analysis
## Overview of the analysis
Bigmarket, a startup that helps businesses optimize their marketing efforts would like us to assist one of its clients to do some analytics on a large catalog of products posted on Amazon retail review website. They would like to know how the reviews of their products compare to the reviews of similar products sold by their competitors. </br>
The dataset we used for this study consists of reviews of personal care appliances such pulse oximeters, massagers, eyewear, etc. </br> 
We performed an ETL (i.e., Extract, Transform, and Load) process to extract the dataset, transform the data, connect to an AWS RDS (i.e., Amazon Web Services Relational Database Service) instance, and load the transformed data into pgAdmin.  Then we used PySpark in Google Colab to determine if there was any bias toward favorable reviews from Vine members in dataset.
## Results
#### Total count of reviews 
* Vine reviews
![Vine reviews](https://user-images.githubusercontent.com/34750363/163735848-f5ea327a-2798-4f99-9a40-f69b61736a91.png)
* Non-Vine reviews 
![Non-Vine reviews](https://user-images.githubusercontent.com/34750363/163735911-53a9080d-fb71-4651-b871-6e611d8ccce9.png)
#### Total count of 5-star reviews
* Vine reviews
![Vine reviews 5-star](https://user-images.githubusercontent.com/34750363/163735937-cf517be5-7d60-4d8d-a543-2910dc88af11.png)
* Non-Vine reviews 
![Non-Vine reviews 5-star](https://user-images.githubusercontent.com/34750363/163735951-e90e85a2-83e8-46b2-8898-668785351475.png)

#### Percentage of 5-star reviews
* Vine reviews
![Vine reviews 5-star percentage ](https://user-images.githubusercontent.com/34750363/163735984-ffa2a6c9-2d39-48da-a86b-f61f6f5c5faf.png)
* Non-Vine reviews 
![Non-Vine reviews 5-star percentage ](https://user-images.githubusercontent.com/34750363/163736004-e150102b-5d7b-4d56-ae3d-ca0572454d0a.png)
## Summary
The analysis revealed that about 66.7% of reviews in the Vine program were 5-star rated, while only about 55.1% of reviews in the non-Vine program were 5-star rated. Hence, it appears that there could be some degree of positivity bias for reviews in the Vine program. </br>
However, we would suggest running more analysis such as determining the mean, median, and the mode of the star rating variable for both programs (i.e., Vine, non-Vine reviews). These could be followed up by a t-test to compare the means, or a Kruskal_Wallis test to compare the medians to make sure that these two population are actually statistically different.
## Resources
#### Data source:
[Amazon retail review website]( https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
[Dataset]( https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Personal_Care_Appliances_v1_00.tsv.gz)
#### Software:
Google Colab Notebook, PostgresSQL, pgAdmin 4, AWS

