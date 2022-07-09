# Amazon Vine Analysis

## Overview of Project

Perform an analysis on Amazon Reviews data using PySpark on Google Colab.

### Purpose

From approximately 50 select 1 of the Amazon Reviews Dataset, and use PySpark to load and transform the data to determine if there is any bias toward favorable reviews from Vine members in your dataset. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products.

## Results

For the [Gift Cards](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Gift_Card_v1_00.tsv.gz) dataset from the [Amazon Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), the results are as follows.

* Total Vine (Paid) Reviews: 0
![Paid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/total-paid.png)

* Total Unpaid Reviews: 355
![Unpaid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/total-unpaid.png)

* 5 Star Paid Reviews Count: 0
![5 Star Paid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/five-star-paid-reviews.png)

* 5 Star Unpaid Reviews Count: 90
![5 Star Unpaid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/five-star-unpaid-reviews.png)

* Percentage of 5 Star Paid Reviews: 0% (See image below, and comment circled in yellow)
![Paid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/five-star-paid-percentage.png)

* Percentage of 5 Star Unpaid Reviews: 25.352%
![Paid Reviews](https://github.com/psidhu42/amazon-vine-analysis/blob/main/resources/five-star-unpaid-percentage.png)


## Summary

From this analysis, we can see that there are 0 (Zero) Vine (paid) reviews for the Gift Cards. Which gives us Zero 5-star reviews and a zero percentage of 5-star reviews from the total paid paid reviews. Out of the 355 Unpaid reviews, 90 are 5-star reviews, which gives us roughly 25.4% of the unpaid reviews being 5-star. It can be safely determined that there is no 'Positivity Bias' for this dataset because there are no paid reviews at all.

This dataset was not a good candidate to determine positivity bias, because there are no paid reviews. However, if this were a dataset that had paid reviews, an additional analysis could be to order reviews by date and focus on the most recent month of reviews. If there are very few unpaid reviews compared to paid ones, this may also suggest 'Positivity Bias'.