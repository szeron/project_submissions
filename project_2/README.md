# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Project 2: Creating a HDB Resale Pricing Regression Model

This project explores the Singapore HDB dataset and how a regression model may be created to predict resale prices.

---

## Problem Statement

I am a real estate analyst who created a regression model that aims to accurately predict the resale prices of HDB flats in Singapore based on a given set of variables. Through this analysis, my goal is to educate buyers & sellers if a house is being priced fairly, understand the main factors that impact HDB prices, and finally to predict the resale price of a HDB unit given a set of variables, allowing my clients to make more informed decisions in this dynamic housing market.

---

## Data Dictionary

|Feature|Type|Description|
|---|---|---|
|**resale_price**|*float*|the property's sale price in Singapore dollars. This is the target variable that you're trying to predict for this challenge.| 
|**Tranc_YearMonth**|*object*|year and month of the resale transaction, e.g. 2015-02|
|**flat_type**|*object*|type of the resale flat unit, e.g. 3 ROOM|
|**flat_model**|*object*|HDB model of the resale flat, e.g. Multi Generation|
|**lease_commence_date**|*integer*|commencement year of the flat unit's 99-year lease|
|**Tranc_Year**|*integer*|year of resale transaction|
|**Tranc_Month**|*integer*|month of resale transaction|
|**mid_storey**|*integer*|median value of storey_range|
|**full_flat_type**|*object*|combination of flat_type and flat_model|
|**floor_area_sqft**|*float*|floor area of the resale flat unit in square feet|
|**hdb_age**|*integer*|number of years from lease_commence_date to present year|
|**max_floor_lvl**|*integer*|highest floor of the resale flat|
|**commercial**|*object*|boolean value if resale flat has commercial units in the same block|
|**market_hawker**|*object*|boolean value if resale flat has a market or hawker centre in the same block|
|**multistorey_carpark**|*object*|boolean value if resale flat has a multistorey carpark in the same block|
|**precinct_pavilion**|*object*|boolean value if resale flat has a pavilion in the same block|
|**total_dwelling_units**|*integer*|total number of residential dwelling units in the resale flat|
|**1room_sold**|*integer*|number of 1-room residential units in the resale flat| 
|**2room_sold**|*integer*|number of 2-room residential units in the resale flat|
|**3room_sold**|*integer*|number of 3-room residential units in the resale flat|
|**4room_sold**|*integer*|number of 4-room residential units in the resale flat|
|**5room_sold**|*integer*|number of 5-room residential units in the resale flat|
|**exec_sold**|*integer*|number of executive type residential units in the resale flat block|
|**multigen_sold**|*integer*|number of multi-generational type residential units in the resale flat block|
|**studio_apartment_sold**|*integer*|number of studio apartment type residential units in the resale flat block|
|**1room_rental**|*integer*|number of 1-room rental residential units in the resale flat block|
|**2room_rental**|*integer*|number of 2-room rental residential units in the resale flat block|
|**3room_rental**|*integer*|number of 3-room rental residential units in the resale flat block|
|**other_room_rental**|*integer*|number of "other" type rental residential units in the resale flat block|
|**planning_area**|*object*|Government planning area that the flat is located|
|**Mall_Nearest_Distance**|*float*|distance (in metres) to the nearest mall|
|**Mall_Within_500m**|*float*|number of malls within 500 metres|
|**Mall_Within_1km**|*float*|number of malls within 1 kilometre|
|**Mall_Within_2km**|*float*|number of malls within 2 kilometres|
|**Hawker_Nearest_Distance**|*float*|distance (in metres) to the nearest hawker centre|
|**Hawker_Within_500m**|*float*|number of hawker centres within 500 metres|
|**Hawker_Within_1km**|*float*|number of hawker centres within 1 kilometre|
|**Hawker_Within_2km**|*float*|number of hawker centres within 2 kilometres|
|**hawker_food_stalls**|*integer*|number of hawker food stalls in the nearest hawker centre|
|**hawker_market_stalls**|*integer*|number of hawker and market stalls in the nearest hawker centre|
|**mrt_nearest_distance**|*float*|distance (in metres) to the nearest MRT station|
|**bus_interchange**|*integer*|boolean value if the nearest MRT station is also a bus interchange|
|**mrt_interchange**|*integer*|boolean value if the nearest MRT station is a train interchange station|
|**bus_stop_nearest_distance**|*float*|distance (in metres) to the nearest bus stop|
|**pri_sch_nearest_distance**|*float*|distance (in metres) to the nearest primary school|
|**vacancy**|*integer*|number of vacancies in the nearest primary school|
|**pri_sch_affiliation**|*integer*|boolean value if the nearest primary school has a secondary school affiliation|
|**sec_sch_nearest_dist**|*float*|distance (in metres) to the nearest secondary school|
|**cutoff_point**|*integer*|PSLE cutoff point of the nearest secondary school|
|**affiliation**|*integer*|boolean value if the nearest secondary school has an primary school affiliation|

---

## Methodology

1. Clean data
    - including preparing data for exploratory data analysis by performing the appropriate transformations such as splitting data in train and validation sets
2. Perform Exploratory Data Analysis
    - summary statistics and visualizations such as scatterplots, heatmaps, and boxplots
3. Preprocess data
4. Model data
    - employ multiple linear regression, ridge and lasso models
5. Evaluate models using RMSE

## Conclusions & Recommendations

The optimal model to use is the Ridge regression model. Apart from having the lowest root mean squared error, the Ridge regression model mitigates multicollinearity and avoids overfitting the model. It also adds a regularization term to the linear regression model's cost function, which shrinks the coefficient estimates of highly correlated independent variables and improves the model's accuracy and generalization ability as a result. Therefore, we recommend using the Ridge model for our HDB resale price prediction model.

Based on the top 20 predictors above, resale prices are mainly impacted by the size of the flat and which planning area (location) the flat is at. For HDB buyers who are on a budget, they may consider opting for smaller sized flats in areas like Woodlands, Sembawang & Jurong West. Vehicle owners who have the means to commute freely may also consider choosing flats that are farther from the MRT and hawker centres, as there is a high chance that they will save even more by choosing these units.

One of the main limitations of this project is that it is not feasible to fully explore all the interaction effects between the variables due to computational constraints. A more thorough exploration would require a substantial amount of time and resources that may not be readily available to all. As a result, we opted for a model with relatively lower complexity, but there may still be room for further optimization if we are willing to accept an increase in model complexity.

