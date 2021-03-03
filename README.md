
# Assessing Marketing Campaigns
## Promotion Performance | A/B Testing

**Author**: Miguel Santana

Thank you for reviewing this repository. The author's contact info, blog, sources and social media profiles are listed below under **further information.**

The contents of this repository detail an analysis of three marketing campaigns in a retail environment. A new item has been introduced in several markets. The markets were randomly selected and different promotions are used at each location. The results are tracked and then used to select the most effective marketing campaign. Our analysis will determine which promotion has the largest impact on sales performance and offer actionable insight. 

### Project Framework

![!](/images/OSEMN.png)

**Data processing and analysis is completed using the OSEMN framework. The structure includes: Obtaining the data, Scrubbing (processing), Exploratory Data Analysis, Statistical Modeling and Interpretation of the Results.**

#### The Data

The project data is made available via Udemy course **Data Science & Deep Learning for Business**. A full Udemy source citation is available below under **sources.** 

#### Feature Details

The data includes 548 promotional records:
- MarketId: unique market identifier
- AgeOfStores: age of store
- LocationID: unique store identifier
- Promotion: promotion identifier
- Sales in Thousands: sales per store, promotion and week
- Market size: small, medium & large market ID
- Week: week 1-4 of the promotion

## Scrubbing/Data Cleaning 

**Key Decisions**

* Check for null values

The dataset is manufactured and as such has no missing values. Typically, businesses closely guard their promotional data so real use cases are rarely publicly available for analysis. Our A/B testing of marketing campaigns is for educational and illustrative purposes.

# Exploratory Data Analysis

#### Sales by Promotion

![!](/images/salesxpromo.jpg)

#### Promotions by Market Size

![!](/images/promoxmarket.jpg)

#### Age of Stores

![!](/images/storeages.jpg)

# A/B Testing

    Total Per Promotion
    1     9993.03
    2     8897.93
    3    10408.52
    Name: SalesInThousands, dtype: float64

    Mean | Sales Per Promotion Promotion
    1    58.099012
    2    47.329415
    3    55.364468
    Name: SalesInThousands, dtype: float64
    
    Standard Deviation | Sales Per Promotion Promotion
    1    16.553782
    2    15.108955
    3    16.766231
    Name: SalesInThousands, dtype: float64
    
    Total Promotion Count Per Promotion 
    1    172
    2    188
    3    188
    Name: SalesInThousands, dtype: int64

## Promo 1 vs 2

    T-value: 6.42752867090748
    P-value: 4.2903687179871785e-10

The sales counts and mean values for promotion 1 are larger than those in group 2. 

The T-Value of 6.23 illustrates a degree of difference (variation) between the two promotions. The P-Value of 0.0000000004 (when compared to a threshold of 0.05) means difference between the promotions is statistically significant. 

Promotion 1 out performs promotion 2 in a significant way. 

## Promo 1 vs 3


    T-value: 1.5560224307758634
    P-value: 0.12059147742229478

Promotion 1 and 3 have a very similar mean, standard deviation and total sales per promotion (difference is a few hundred dollars).

The T-Value and P-Value illustrate no real significance between the two groups. While promotion 3 ended up with more sales - this may be explained by the additional 16 promotional cites counted under promo 3.

Failed to reject the null hypothesis. There is no statistical difference between promo 1 and promo 3.

# Interpreting Results | Recommendations

A/B test results showed promotion 1 outperformed promotion 2 in a significant manner. A/B test results did not show a significant difference between promotions 1 and 3. The mean and standard deviation values were very similar and while promotion 3 lead to more sales, the selection of promotions per market per location were done at random. There were 172 occurrences of promotion 1 and 188 172 occurrences of promotion 3. The difference in sales performance is more than likely due to random chance. 

### Limitations
The analysis was completed for illustrative purposes only. As mentioned at the top of our notebook - businesses vary rarely make sales data available to the public and as such this project was completed using data from a Udemy course. 

The main challenge to this project is understanding how similar the provided dataset is to something that will be seen in the workplace. This may be effected by year (when compared to today's data), region and many other industry factors. 

## Future Work

Future work should include a larger dataset with additional context. While fabricated, an ideal dataset would mimic current sales trends, in a specific market with multiple products and promotions to test for effects of markets or locations themselves on the the promotion. Understanding these effects will lead to a more functional determination of 'best' promotion for this business within their industry. 

### Further Information
Please review the narrative of our analysis in [our jupyter notebook](./jupyter_notebook.ipynb) or review our [presentation](./presentation.pdf)

For any additional questions, please reach out via email at santana2.miguel@gmail.com, on [LinkedIn](https://www.linkedin.com/in/miguel-angel-santana-ii-mba-51467276/) or on [Twitter.](https://twitter.com/msantana_ds)

A blog post on this analysis is available on [Medium.](https://miguelangelsantana.medium.com/marketing-campaign-assessment-b7f5785ffb4c)

#### Sources

Additional analysis, notes and file sources can be found on Udemy's website. 

* Course Name: Data Science & Deep Learning for Business by Rajeev Ratan

##### Repository Structure

```

├── README.md               <- The top-level README for reviewers of this project.
├── jupyter_notebook.ipynb     <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf        <- pdf version of project presentation

```