# Housing Price Analysis in Kings County, Washington
![image](https://github.com/Kellyajara/Phase2_Project/assets/127794801/838b5b02-aa53-4435-acbd-aed4887859e6)

By: Kelly Jara, Bianna Gas, Laibah Ashfaq

## Overview
This project utilizes King County housing data from 2021-2022 in order to make predictions regarding the sale prices of houses based on certain home features. After our exploratory data analysis and multiple linear regression modeling, we have determined that location, waterfront, house grade and square footage have the largest impact on increasing the sales prices of homes in this region.

## Business Problem
Our stakeholder, The Corcoran Group is looking to expand into the Kings County area housing market to grow their west coast footprint. In order to help them get to know the real estate market in this new area, we were tasked with analyzing what home features help increase the sales price of the properties. Using our data, the real estate company can narrow down which homes to focus on that would command a higher sales price. 

## Data
This project utilize a dataset from Kaggle regarding Kings County, Washington home sales between 2021-2022. The source includes certain home features such as: 
  * Bedrooms: Number of bedrooms
  * Bathrooms: Number of bathrooms
  * Sqft Living: Square footage of living space in the home
  * Sqft Lot: Square footage of the lot
  * Floors: Number of floors (levels) in the home
  * Waterfront: Whether the house is on a waterfront
  * Greenbelt: Whether the house is adjacent to a greenbelt
  * Nusiance: Whether the house has traffic noise or other recorded nuisances
  * View: Quality of view from house
  * Condition: How good the overall condition of the house is. Related to maintenance and age of the   
    house.
  * Grade: Overall grade of the house. Related to the construction and design of the house.
  * Heat Source: Heat source for the home
  * Sewer System: Sewer system for the house
 
## Modeling
After cleaning our data, we performed a 70%-30% Train-Test split on the data with price as our target variable and all other variables as predictors. Afterwards, we created multiple iterative linear regression models. The following features were included in each model:
  * Model 1: bedrooms, bathrooms, sqft_lot, sqft_above, floors ,sqft_basement, sqft_garage, sqft_patio,     grade_code , view_code , condition_code
  * Model 2: bedrooms, bathrooms, sqft_living, sqft_above, sqft_lot, floors , grade_code , view_code,
    condition_code, sqft_garage, sqft_patio, yr_built, waterfront, greenbelt, nuisance, heat_source,  
    sewer_system 
  * Model 3: bedrooms, bathrooms, sqft_living, sqft_above, sqft_lot, floors, grade_code, view_code,
    condition_code, sqft_garage, sqft_patio, yr_built, waterfront, greenbelt, nuisance, heat_source,   
    sewer_system, zipcode
    
## Results
We computed the mean absolute error, R^2 and root mean squared error of each model to be able to compare the models predictions to actual values.

* Model 1:
  - Mean Absolute Error = 359,955.85 USD
  - Root Mean Square Error = 709,403.43 USD
  - R^2 = 0.498

* Model 2: 
  - Mean Absolute Error = 359,955.85 USD
  - Root Mean Square Error = 709,403.43 USD
  - R^2 = 0.532
 
 * Model 3:
   - Mean Absolute Error = 230,170.53 USD
   - Root Mean Square Error = 774,568.32 USD
   - R^2 = 0.703

We found that adding more categoricals and the zipcodes to our model significantly increased the R2 value from 0.498 to 0.703. Our best model had an R-squared value of 0.701 telling us that the model fit the data with an accuracy of 70.1%.  The mean absolute error also decreased with each iteration, and our final model had an MAE of $230, 170, which signifies that our model is able to predict price within that range. The MAE is fairly low considering our average home price is $1.13 million. By having an increased R2 value, this allowed us see how well our model explains the data and move forward with providing recommendations to our stakeholder. We also computed the coefficients of each feature, which can help us prioritize the features in the model based on its effect on the price.

<img width="134" alt="Screen Shot 2023-06-02 at 11 27 43 AM" src="https://github.com/Kellyajara/Phase2_Project/assets/128645674/a673bcf8-905f-47f6-90ce-8ceb68de941d">


Based on our third model, we were able to visualize the correlation/effect between the following: 

Average price of a home based on location:
![Price Per Zipcode](https://github.com/Kellyajara/Phase2_Project/assets/127794801/5976eb2d-645b-446c-8d2e-216cd4740e76)

Average price of a home based on grade: 
![Price Per Grade](https://github.com/Kellyajara/Phase2_Project/assets/127794801/a7503575-3a49-4228-9939-1ba08ee9159e)

Average price of a home based on waterfront view: 

![Waterfront](https://github.com/Kellyajara/Phase2_Project/assets/127794801/ab46cb13-2dd0-4f19-b4d1-96ac54c00782)

Average price of a home based on the sqft of a home:
![sqft_living](https://github.com/Kellyajara/Phase2_Project/assets/127794801/77a455ef-21d0-4d4d-9b44-4c34ce2c5c62)

## Recommendations
Our recommendations for prioritizing realtor efforts are as follows:
  - Homes in specific zipcodes (98039,98004,98040,98033,98112)
  - Homes on the waterfront
  - Homes with the highest home grade possible 
  - Larger sqft homes

Other features that helped increase sales price significantly include view, condition, bathrooms and greenbelt. 



  

