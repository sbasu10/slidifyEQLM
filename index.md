---
title       : Earthquakes LM
subtitle    : Linear Regression Model For Earthquakes CSV Dataset
author      : Sujoy Basu
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Main Idea: Leverage the lm function for Interactive Linear Regression Application

1. lm is robust function in R, used to fit linear models
2. Provides a linear regression model for the dataset installed with application
3. Prompt user for the columns in dataset that will be the response and predictors in the model
4. Render plots and summary information of linear regression model on single page
5. Leverage the reactive aspect of Shiny for iterative refinement of model
6. User can iterate by selecting different predictors and observing results

--- .class #id 

## Layout determined by ui.R

1. Simplicity and ease of use are primary considerations
2. Left panel captures response column and the predictors from the user
3. The main panel has separate tabs for the linear regression model, dataset and documentation 

--- .class #id 

## Logic determined by server.R

1. The runRegression method is reactive
2. When user changes the selections in left panel, model is recomputed
3. Residual plots, followed by model and ANOVA summary for maximum information
4. Watch for changes in statistics such as Adjusted R-squared metric when selections are changed

--- .class #id 

## Future Work


```
## Magnitude ~ Depth + NST
```

1. The default choices for response and predictor variables shown above are reasonable for this Earthquakes dataset 
2. Application may be extended to take the dataset as input, and detect reasonable defaults
3. User may have more tunable parameters in future, and can upload test datasets
4. The  predictions on test datasets will be displayed in separate tabs

