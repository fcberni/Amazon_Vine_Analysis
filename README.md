# Amazon_Vine_Analysis

## Overview of the analysis 

The purpose of this analysis is to view Amazon Vine reviews and determine if there is any bias toward favorable reviews from Vine members in the dataset. Given the choice of various products ranging from clothing apparel to wireless products, I chose reviews of video games. I used Amazon’s AWS services, Postgres and pgAdmin, and Pyspark and Google Collaboratory in order to perform the Extract, Transform and Load method. After performing the ETL, I used various Pyspark functions on the vine data in order to find what trends the data is pointing towards. 

![insert customer table]()
![insert review table]()
![insert products table]()
![vine table]()


## Results

![insert paid vine](paid vine) ![insert nonpaid vine](nonpaid vine)

How many Vine reviews and non-Vine reviews were there?

When determining which reviews were Vine reviews and which weren’t, I first used the filter() method and created two separate tables based on the vine column for “Y”s and for “N”s. Afterwards, I used the count() method for both tables to get a final count of 94 Vine reviews and 40471 Non-Vine reviews.

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

To determine how many 5 star ratings each had, I applied a filter on the star_rating column for each respective table. I ended up with 48 Vine 5 Stars and 15,663 Non-Vine 5 Stars.

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

For these figures, I performed a simple math function of dividing the total count of 5 star ratings by the total count of each respective table. 51.06% of Vine reviews were rated 5 stars while 38.70% of Non-Vine reviews were rated 5 stars.

## Summary:

While analyzing the results of the Vine reviews versus Non-Vine reviews for positivity bias, looking at the percentages without much context can definitely make an argument that paid reviewers will rate video games more favorably. Over half of the Vine reviews are 5 star ratings meanwhile Non-Vine reviews have closer to one third of their reviews rating 5 star reviews. However, when looking at the total numbers for each category, Non-Vine reviews are significantly larger than Vine reviews so it is not a truly fair comparison since the sample sizes are so vastly different. There would definitely need more analysis in order to fully come to a conclusion on positivity bias here.
 
If I were to provide an additional analysis to determine positivity bias, I would look at unfavorable reviews as well. If unfavorable reviews such as 1 star reviews were much less for Vine reviews than Non-Vine, then we can compare both sets of data to make a solid argument here.
