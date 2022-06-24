# Using Linear Regression to Predict Undervalued Homes  In Dutchess County, NY

# Model Files

#### Main Notebook - model.ipynb
#### Data Scraper - Dutchess County Residental Sales Scraper.ipynb
#### Places Scraper - Get Nearby Places from Yelp API.ipynb

![](img/house.jpg)

## Project Description

In this project, I will be trying to predict house prices using a multiple linear regression model on a dataset I scraped from public records. This notebook contains the code and analysis used for creating that model from the already created dataset, and then using those predictions to determine homes that may have been undersold or undervalued.

## Introduction

Since 2020, the housing market has been tumultuous and volatile. Median sales prices for houses across the US, have increased significantly, and many first time home buyers are continually being placed further away from their dream of owning a home. Due to many factors, the demand for owning a house is high. Besides first time buyers, there are many [corporations buying low cost houses](https://www.nytimes.com/2022/04/23/us/corporate-real-estate-investors-housing-market.html?referringSource=articleShare) and renovating them to eventually rent.

There are many factors that have led to the unaffordability of first time buyers. According to [Nerdwallet’s 2021 Home Buyer Report](https://www.nerdwallet.com/blog/2021-home-buyer-report/), the top factors that are preventing first time home buyers from purchasing a home are: 
Not enough saved for a down payment
Credit Score
The coronavirus pandemic
Low income
Lack of available home in budget or preferred area

I am interested if, after predicting the price of a home, I can find houses that might be of interest to first time home buyers due to their affordability. If a house is listed for a price lower than its prediction, the property may be of interest as an investment.

## The Data

In order to try to predict the price in the current volatile market, I aimed to create a dataset from current and recent data. The dataset used in this notebook was scraped from public records on the Dutchess County, NY parcel access website. The data ranges from July 2019 and June 2020 and contains all residential home sales. 

Apart from a few outliers, I will be the entire range of home prices. Even though we are aiming to predict the affordability of a house, we will use the entire distribution of price data to determine a prediction.

I also looked up zip codes and geographical coordinates for each row of data, as well as its proximity to the nearest amenities and schools, and added this to the dataset.

## Projections

I am hoping to predict the affordability given a set of data from current for sale home information in the same county.

Apart from making an accurate prediction, I hope this notebook can be a tool that could test the affordability or value of a house.

 
# Summary

Compared to other linear regression models on housing data around the web, this model did not have the highest R2 score nor is it the most accurate predictor of price. I can say that the model is fairly accurate in predicting the ballpark price for a house, and I have determined that the variance and irreducible error in this model is high.

There are many factors that could lead to high irreducible error in this model and I think one is the volatility of the current housing market. Pandemic spending and panic buying was high during 2020, but the housing market is still extremely 'hot' and houses are being valued for higher and higher prices every day. With remote work and coronavirus variants still possible for the near future, houses in rural areas are still in high demand. I believe that this can be factored into why this model was unable to predict a more accurate price.

Another factor I have considered, is that the model is accurate but the price of a home flucuates widely. Price is determined by the buyer and seller, not by predictive variables. If a seller and a buyer agree to a price, it may not follow the mean or any logic necessarily. The model may not be accurate, but we cannot determine that the price is representative of the actual value of the home.

Apart from achieving high accuracy of results, this model is mostly designed to be used as a predictive tool for first time buyers to better navigate a searing hot market and find an affordable, and smart investment. There are houses being undersold and undervalued everyday, and this model can help to find where those properties are.

I am fairly happy with the results of this model and look forward to adding a validation set of houses still for sale and try to predict whether their list price is under or overvalued.