# MechaCar_Statistical_Analysis Challenge
In your README, create a subheading, 

## Linear Regression to Predict MPG. 
In this deliverable, we are going to use multiple linear regression to predict which variables affect a car's performance measured in miles per gallon (mpg). To do this, we define our null hypothesis as that none of the metrics that describe the cars affect their performance.
As part of the data exploration, I used R's eigenfunction to plot each of the metrics vs. mpg, to see if there is a quantitative correlation. From the graphs you can see that only "vehicle_length" and "ground_clearance" seem to affect the mpg variable. Running the corr() function we can see that all the variables have a correlation, but the ones that have the most are vl and gc.
+
Subsequently, I used the R function for linear regression lm(), using all the variables and the summary gave us the following data:
 p-value = 5.35 e-11, clearly less than 0.05, so we can reject our null hypothesis and affirm that there is a correlation between the car's metrics and mpg.
Looking at our predictor variable, adjusted R-squared, we can say that 68.25% of the mpg variability is predicted by our model.

Subsequently, I used the R function for linear regression lm(), using all the variables and the summary gave us the following data:
From the image we can see that only vl and gc have p-value less than 0.05, so in these two cases the null hypothesis is false and therefore, these variables do correlate with mpg. In the case of the other metrics, we discard them because their p-value is greater than 0.05.

now to determine the coefficients, we use the attribute of the coefficients object and obtain these values.
-1.039 and e02
-103.9 + 6.26 x1 + 3.54 x2



nd write a short summary using a screenshot of the output from the linear regression, and address the following questions:




Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
Is the slope of the linear model considered to be zero? Why or why not?
Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
