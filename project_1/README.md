# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring climate data of Singapore

# GA Project 1

This project explores the climate data of Singapore including rainfall, temperature, relative humidity, wet bulb temperature, sunshine duration etc.

---

## Introduction

I have been hired by Singapore Tourism Board and am required to advice tourists who visit Singapore and love being outdoors, on how they can be prepared based on their travel months. Weather in Singapore is largely sunny or rainy. However, tourists who are not familiar with local weather conditions may be caught off guard, causing their plans to be disrupted. This project aims to analyse trends in Singapore weather to identify adverse conditions for tourists who enjoy being outdoors. This analysis can help tourists plan travel periods and itineraries better, bringing home a pleasant experience.


### Datasets used

* [Monthly Rainfall Total](https://data.gov.sg/dataset/rainfall-monthly-total)
* [Monthly Number of Rain Days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)
* [Relative Humidity](https://data.gov.sg/dataset/relative-humidity-monthly-mean)
* [Monthly Maximum Daily Rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
* [Monthly Mean Sunshine Hours](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)
* [Visitors To Selected Places Of Interest](https://tablebuilder.singstat.gov.sg/table/TS/M891071)


---

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**no_of_rainy_days**|*integer*|rainfall-monthly-number-of-rain-days|Monthly number of rain days| 
|**total_rainfall**|*float*|rainfall-monthly-total|Total rainfall in mm|
|**maximum_rainfall_in_a_day**|*float*|rainfall-monthly-highest-daily-total|Highest daily rainfall in the month in mm|
|**mean_rh**|*float*|relative-humidity-monthly-mean|Monthly mean relative humidity in %|
|**mean_sunshine_hrs**|*float*|sunshine-duration-monthly-mean-daily-duration|Monthly mean daily sunshine duration in hrs|
|**asian_civilisations_museum**|*integer*|attractions_visitors|Visitors in thousands|
|**national_museum_of_singapore**|*integer*|attractions_visitors|Visitors in thousands|
|**science_centre_singapore**|*integer*|attractions_visitors|Visitors in thousands|
|**jurong_birdpark**|*integer*|attractions_visitors|Visitors in thousands|
|**night_safari**|*integer*|attractions_visitors|Visitors in thousands|
|**river_wonders**|*integer*|attractions_visitors|Visitors in thousands|
|**singapore_zoological_gardens**|*integer*|attractions_visitors|Visitors in thousands|
|**sun_yat_sen_nanyang_memorial_hall**|*integer*|attractions_visitors|Visitors in thousands|
|**indian_heritage_centre**|*integer*|attractions_visitors|Visitors in thousands|

---

## Brief Summary of Analysis

Apart from weather datasets, visitor numbers to popular attractions were analysed to see if there was indeed a correlation with Singapore weather. The heatmap suggests no correlation has been found and it may be more worthwhile to study individual months that have adverse weather conditions.

## Conclusions & Recommendations

Data visualisations show that there is no clear correlation between weather and visitor numbers to attractions. As there are more significant factors other than weather that impact footfall, it may be useful to gather trends from past weather data in order to advise tourists and outdoor lovers on when the best months are for visiting.

The research has shown that the months from November to January tend to be the rainiest months of the year, hence these would be the months to avoid should travellers wish to explore the outdoors. It would be generally considered a safe choice to visit during the months of February to May as this is typically when Singapore experiences the least amount of rain and the most sunshine.