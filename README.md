# Amazon_Vine_Analysis
Module 16 Challenge

### Overview of the analysis
This analysis was conducted to determine if there is any bias generated in product reviews due to the paid Amazon Vine program.  The concern is if paid reviewers from the Amazone Vine program are able to deliver unbiased product reviews.  

We used the Watches category to evaluate the presence or lack of bias in product reviews.  Initially, we excluded reviews with fewer than 20 votes to ensure credibility of the votes.  We also created a metric ("helpfulRate") to include only the most helpful reviews.  This was derived by calculating the percentage of votes that were deemed helpful by the Amazon community and only included those with a rate >.50.

### Results: Using bulleted lists and images of DataFrames as support, address the following questions:

How many Vine reviews and non-Vine reviews were there?

After filtering for helpfulRate > 0.5, the following results were observed:

- vine_filtered = 43

**vine_filtered screenshot**

- nonVine_filtered = 7720 

**nonVine_filtere screenshot**

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- vine_filtered where star_rating = 5 == 14

- nonVine_filtered where star_rating = 5 == 4018

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- vine_filtered where star_rating = 5 as a % of total vine_filtered = 32.56% 

- nonVine_filtered where star_rating = 5 as a % of total nonVine_filtered = 52.05%

### Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

No, there is no evidence of positivity bias in the Watch review category related to the Vine program.  Vine reviewers represented 0.55% (43/7763) of the filtered reviews (min. 20 votes, helpfulRate >0.5), but only represented 0.35% (14/4032) of the filtered five-star reviews.  If a positivity bias existed, you would expect Vine reviewers to represent a larger share of the five-star reviews than the population of all reviews.

This analysis was conducted on a single category, requiring additional analysis to be conducted across others.  For example, the impact of reviews surely varies across categories, so less style- or brand-conscious categories than watches would require a comparable analysis.  Within this dataset, I would dive deeper into sales or win rates by product and brand to understand the impact of the Vine program's reviews. 
