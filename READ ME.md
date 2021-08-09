# Project 2 - Ames Housing Data and Kaggle Challenge


## Problem Statement

Selling and or buying a home is a risky investment for all parties involved, as with any investment one wants to reap a large enough return. But with so many features of any home to be factored in, ranging from the roof type to the location, it can be difficult to decide what features of the home should be heavily invested in, in order to see these high returns. We've been hired by XYZ Developers who are located in Iowa and aim to build over 100 homes in the next 2 years. They've requested that we assess whether or not they should invest a substantial amount of their budget to hire, 'Bed, Bath, Basements and Sons' contractors who specialize in building and remodeling beds, baths, and basements for residential homes. XYZ Developers would like to know if a substantial focus on these features of a home will result in high selling prices and better returns. We aim to use our data science modeling skills to provide them with our findings and ultimate recommendations.  

## Brief Background

In order to conduct our analysis and provide our clients with the needed findings and recommendations, we've obtained a public dataset of the housing data in Ames Iowa a town less than 20 miles from the area XYZ Developers plan to build. Ames Iowa is a city in Story County, Iowa and is best known as the home of Iowa State University. This dataset is essentially a large repository of all possible features (over 75) of a house that may affect the selling price. Linked here is a data dictionary to said dataset, detailing each of the features and their accompanying values. For more information on the dataset itself we did some outside research to gain better knowledge of the city as well as the data set:

* [Ames,Iowa (wikipedia)](https://en.wikipedia.org/wiki/Ames,_Iowa)
* [Ames Iowa: Alternative to the Boston Housing Data Set](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)



## Scope & Methodology
1
As mentioned there are over 75 features in this dataset so we could delve into assessing a number of outcomes, but as XYZ Developers has requested we focus our efforts on the services that 'Bed, Bath, Basements and Sons' provides, these are the features we will assess. Our analysis will be performed in four different parts:

__1.__ Data Cleaning: We will clean the initial dataset being cognizant of missing data or features that may not be necessary to our analysis.  

__2.__ EDA: Here we begin to explore the clean data and get an idea of how these features alone and in combination with other complimentary features may affect our ultimate goal of predicting high sales prices. 

__3.__ Modeling Part I: We will utilize linear regression incorporating different sets of features to see what best achieves our objective. 

__4.__ Modeling Part II: An introduction of Lasso and Ridge regularization to our previous models with the aim of improving our model and avoiding as much bias as we possibly can. 
## Exploratory Data Analysis

### Findings 
_1.__ An increase in the number of total rooms a house has, excluding bathrooms, results in higher selling prices, but once the home surpasses 11 rooms, we see a decrease in sales price. 

__2.__ The number of bedrooms has a weak (0.14) effect on sales prices as indicated by our correlation matrix. 

__3.__ Full baths have a strong (0.54) effect on the selling price, due to a lack of other data surrounding baths, 
i.e. the area of said bath, the quality, or the condition we had to solely rely on the number of bathrooms to make an assessment. Having 3 bathrooms was the best number for a higher sales prices, anything more than that showed a reduction in sales price. 

__4.__ Half baths didn't particularly matter. Having at least one increased your sales prices, having two resulted in a reduction in the sales price.

__5.__ Out of all features we assessed, basements showed to have the highest impact on sales prices, particularly the square footage of the basement, with a 0.63 correlation to sales price. 
    - Given a few outliers, there was some pattern of seeing larger basement areas to higher sales prices but
    not enough to rely on solely. We'll have to consider other related features to gain a better relationship.

__6.__ Good is good enough. Analyzing the basement qualitative data, we noted that having a basement with good height, in good condition, and of good quality resulted in higher sales prices. The was no need for these factors to be above and beyond (Excellent) in order to see higher sales prices. 

__7.__ Now houses with 'typical' rating for their basements, still had higher sale prices compared to those with no basements at all. 

__8.__ Overall quality matters. Building homes with poor materials regardless of the features involved yields lower returns, an investment in excellent building materials overall provides for a higher sales prices. 


## Modeling 
Using Multiple Linear Regression (MLR), we created several models starting with one that included the strongest correlated variables within our scope and working from there. See list below for all models generated.

__List of Models__

* __Model 1__ - Strongly Correlated Bed, Bath, and Basement Features
* __Model 2__ - All Beds, Baths, and Basements
* __Model 3__ - All Bed, Bath, and Basements plus.
* __Model 4__ - Baseline Model w/ Polynomial Features
* __Model 5__ - Bed, Bath, and Basements plus Overall Quality

## Conclusions and Recommendations

As a result of EDA and our modeling, it became apparent  the strong impact quality had on the selling price of a home. Adding basement quality and condition, helped improve our model from our initial baseline. Additionally, adding overall quality to our bed, bath, and basement variables, also resulted in a better fit model, one that had a stronger relationship to our sales price target. As s result of this our recommendation are the following:

1. Bedrooms shouldn't be heavily invested in.
2. An investment in full bathrooms should be considered, and having three bathrooms is the best number for their homes, anything more than that may result in lower sales prices.  
3. Having a basement even one of poor quality/condition (not advised) results in higher sales prices than having none at all. 
4. Having a basement of excellent standing won't yield higher prices; a relatively good basement should be enough to result in higher selling prices. 
5. Quality matters. Regardless of the features they decide to invest heavily in, XYZ Developers need to ensure all building materials used are of superb quality, this will allow for better sales prices and higher returns overall. 

