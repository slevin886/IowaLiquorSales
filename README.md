# Predicting Future Liquor Sales in Iowa 
## and Identifying Areas for Future Retail Growth

Accurately projecting future sales and revenue is essential to making effective business decisions. In Iowa, where liquor sales are tightly regulated by the state government, projecting future sales is also essential to balancing the budget. Using a publicly available dataset of more than 2 million sales reports (comprising the entirey of Iowa's liquor sales over 15 months), I projected sales statewide and at the county-level 9 months into the future. Additionally, I went county by county and identified several that warrant consideration for commercial expansion (i.e. opening a liquor store). 

### Projecting Sales 

After cleaning the liquor sales dataset, merging it with county-level demographic data from the 2010 census, and testing a variety of features and models, I projected a 4% increase (or $9.7 million) in sales for the 2016 fiscal year (with a lowerbound estimate of $3.7 million and an upperbound estimate of $15.7 million)

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/Picture2.png" height="300" width="400">
</p>

There were several challenges in arriving at these estimates. First, liquor stores in Iowa vary dramatically in size and there is a corresponding dramatic variance in their sales statistics as you can see across a variety of sales features below.

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/Picture7.png" height="300" width="400">
</p>

Because stores also submit their liquor reports to the state government at irregular intervals, there was also the challenge of missing data. Specifically, there were 81 discordant (i.e. present in 2015 or 2016, but not in both) stores recording sales during the first 3 months in each year that didn't record sales in the other year. Below, you can see the effects of imputing sales data for these stores at the 20th percentile (left) and 10th percentile (right). 

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/dualimage.png" height="300" width="600">
</p>

Regardless, looking only at stores that did in fact record sales across both time periods, reveals $3.8 million in additional sales during the first three months of 2016 compared to the same period in 2015- lending additional credence to the overall estimate. Likewise,  stores only present in 2016 outsold those only present in 2015 by $18,000.

### Identifying locations for commercial expansion

Looking at county demographics proved valuable in predicting profitability at the store-level. Below you can see  the correlations between the **number of stores in a county** and **profitability by store**, the concentration of **men between the ages of 20-34**, and **median income**. 

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/lastimage.png" height="475" width="600">
</p>

Even accounting for these variations (red representing strong positive correlation and blue negative correlation), predicting sales at the store level varied systematically across samples as you can see in the chart below (overestimating for small stores and underestimating for large stores). 

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/Picture6.png" height="475" width="600">
</p>

Nevertheless, across various tests several counties were continuously present. In particular, **Story County** (third from the right below) is predicted to have the capacity for 28 additional (mean-sized) stores. 

<p align="center">
  <img src="https://github.com/slevin886/IowaLiquorSales/blob/master/Images/Picture4.png" height="320" width="450">
</p>
