Predicting Automobile Fuel Efficiency
========================================================
author: Brian Gulbis
date: October 12, 2015
font-family: 'Arial'
transition: fade
incremental: true

The Issue
========================================================

Recent events have revealed that some auto manufacturers have created certain modifications to their vehicles which   resulted in falsely-high fuel efficiency ratings during government testing.
                           
Many consumers are left wondering just how accurate the information provided by the manufacterers really is, and whether than can trust the information when purchasing a vehicle.

Given this, consumers need an independent way to estimate the fuel efficiency of a vehicle and verify the claims of the manufacturer.

Fuel Efficiency Estimator
========================================================

To resolve this situation, a simple web-based app was created to estimate a vehicle's fuel efficiency (in miles per gallon), using only three characteristics of the vehicle:

- Gross Horsepower
- Vehicle Weight (in tons)
- Number of Cylinders

About the Model
========================================================

Based upon the `mtcars` data set, linear regression was used to estimate the change in a vehicle's fuel efficiency as the horsepower, weight, or number of cylinders are changed.


```r
model <- lm(mpg ~ hp + wt + factor(cyl), data=mtcars)
```


```
 (Intercept)           hp           wt factor(cyl)6 factor(cyl)8 
 35.84599532  -0.02311981  -3.18140405  -3.35902490  -3.18588444 
```

How It Works
========================================================

The app is available by going to: 

- https://bgulbis.shinyapps.io/DataProd-Project

Users can input the three parameters for a vehicle they are interested in, and the app will calculate the estimated fuel efficiency (in miles per gallon, or MPG). 

If the user adjusts one of the parameters, the app will automatically recalculate the fuel efficiency in real-time.

