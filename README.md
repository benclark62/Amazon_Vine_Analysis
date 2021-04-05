# Amazon_Vine_Analysis
Module 16 Challenge

### Overview of the analysis
This analysis was conducted to determine if any positivity bias is generated in product reviews due to the paid Amazon Vine program.  The primary concern being that if paid reviewers from the Amazon Vine program are unable to deliver unbiased product reviews, the legitimacy of the program is called into question and Amazon's brand risks being undermined. 

We used the Watches category to evaluate the presence or lack of bias in product reviews.  Initially, we excluded reviews with fewer than 20 votes to ensure credibility of the votes.  We also created a metric ("helpfulRate") to include only the most helpful reviews.  This was derived by calculating the percentage of votes that were deemed helpful by the Amazon community and only included those with a rate >.50.

### Results

How many Vine reviews and non-Vine reviews were there?

After filtering for helpfulRate > 0.5, the following results were observed:

- vine_filtered = 43

![vine](https://github.com/benclark62/Amazon_Vine_Analysis/blob/main/vine_helpful.png)

- nonVine_filtered = 7720 

![nonVine](https://github.com/benclark62/Amazon_Vine_Analysis/blob/main/nonVine_helpful.png)

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- vine_filtered where star_rating = 5 == 14

- nonVine_filtered where star_rating = 5 == 4018

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- vine_filtered where star_rating = 5 as a % of total vine_filtered = 32.56% 

- nonVine_filtered where star_rating = 5 as a % of total nonVine_filtered = 52.05%

### Summary

There is no evidence of positivity bias related to the Vine program in the Watch review category.  Vine reviewers represented 0.55% (43/7763) of all filtered reviews (min. 20 votes, helpfulRate >0.5), but only represented 0.35% (14/4032) of the filtered five-star reviews.  If a positivity bias existed, you would expect Vine reviewers to represent a larger share of the five-star reviews than the population of all reviews.

This analysis was conducted on a single category, requiring additional analysis to be conducted across others to determine the presence of positivity bias.  For example, the impact of reviews likely varies across categories, so less style- or brand-conscious categories than watches would require a similar analysis.  Within this dataset, I would dive deeper into sales or win rates by product and brand to understand the impact of the Vine program's reviews. 
