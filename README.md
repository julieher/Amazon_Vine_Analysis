# Amazon_Vine_Analysis

# Overview of the analysis: 

The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program. In this analysis we will be using PySpark in order to perform the ETL process: extract the 'Outdoors reviews' dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. The Vine Program analysis will be executed by using PySpark to determine if there is any bias toward favorable reviews.

# Results: 
-   **Extract:**

    ![](/Resources/extract.png)

-   **Transform:**

    Using PySpark, the 'Outdoors' dataset was filtered to create a DataFrame where there are 20 or more total votes, the percentage of helpful_votes is greater than 50%, there is a Vine review and where there is not a Vine review. The bellow images show the Vine results.

    Filtered DataFrame where there is a Vine review:
    ![](/Resources/paidVine_df2.png)

    Filtered DataFrame where there is not a Vine review:
    ![](/Resources/unPaidVine_df2.png)

    How many Vine reviews and non-Vine reviews were there?
    ![](/Resources/vineReviews.png)

    How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    ![](/Resources/5star_vine.png)

    What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

    ![](/Resources/vine_percentage.png)

# Summary:

From our analysis, there are 39,869 non-paid Vine users, and 107 paid Vine users. Out of those 107, only 56 have a five-star rating. Since the majority of the five-star rating come from non-paid users, we can conclude that there is no bias toward favorable reviews from Vine members in the 'Outdoors' dataset.
