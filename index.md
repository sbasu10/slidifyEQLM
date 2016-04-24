---
title       : Earthquakes LM
subtitle    : Linear Model For CSV Datasets
author      : Sujoy Basu
job         : Coursera Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Main Idea: Leverage the lm function for a Handy Application

1. lm is robust function in R, used to fit linear models
2. It takes an object of class "formula" as input
3. Prompt user for the terms that make up the formula
4. Limit the terms offered as choices to the columns of CSV file
5. Render plots and summary information of linear model on single page

--- .class #id 

## Layout determined by ui.R

1. Simplicity and ease of use are primary considerations
2. Left panel captures response column and terms of the predictor from the user
3. The main panel has separate tabs for the linear model, dataset and help section 

--- .class #id 

## Logic determined by server.R

1. The runRegression method is reactive
2. Unless user changes the selections in left panel, model is not recomputed
3. Residual plots, followed by model and ANOVA summary for maximum information
4. Easy to spot key information such as residuals and Adjusted R-squared metric

--- .class #id 

## Future Work


```
## [1] "Formula (frmlObj): "
```

```
## Magnitude ~ Depth + NST
```

2. The defaults choices are reasonable for this Earthquakes dataset
3. Application can be extended to take the dataset as input, and detect reasonable defaults
4. The model may be applied to test dataset, and the predictions displayed in a separate tab

