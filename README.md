# MechaCar_Statistical_Analysis Challenge

# Deliverable 1
## Linear Regression to Predict MPG. 
In this deliverable, we are going to use multiple linear regression to predict which metrics  affect a car's performance measured in miles per gallon (mpg). To do this, I define the null hypothesis as that none of the metrics that describe the cars affect their performance.
As part of the data exploration, I used R's function to plot each of the metrics vs. mpg, to see if there is a quantitative correlation. From this plots,  it can see that only "vehicle_length" and "ground_clearance" seem to affect the mpg variable. 

Subsequently, I used the R function for linear regression lm(), using all the variables in their dataframe and the summary gave us the following data:
 p-value = 5.35 e-11, clearly less than 0.05, so we can reject our null hypothesis and affirm that there is a correlation between the car's metrics and mpg.
Looking at our predictor variable, adjusted R-squared, we can say that 68.25% of the mpg variability is predicted by our model.

Subsequently, I used the R function for linear regression lm(), using all the variables and the summary gave us the following data:
we can see that only vl and gc variables provide a significant contribution to the linear model beacuse their  p-values are  less than 0.05, so in these two cases the null hypothesis is false and therefore, these variables do correlate with mpg. In the case of the other metrics, we discard them because their p-value is greater than 0.05.

now to determine the coefficients, we use the attribute of the coefficients object and obtain these values.
-1.039 and e02
#-103.9 + 6.26 x1 + 3.54 x2

<img width="793" alt="D1Summary()" src="https://user-images.githubusercontent.com/102195803/179312746-40b806ab-b50a-446c-b56c-2015cb2c9508.png">
  -Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    From the summary, we can see that only the variables "vehicle_length" and "groun_clearance" provided a non-random amount of variance.
  -Is the slope of the linear model considered to be zero? No. 
    Why or why not? because we have correlacion between the metrics and and the dependent variable, mpg
  -Does this linear model predict mpg of MechaCar prototypes effectively? Yes Why or why not? Because in the summary we can observe that the R squared is 
  
 # Deliverable 2
 
In your README, create a subheading ## Summary Statistics on Suspension Coils, and write a short summary using screenshots from your total_summary and lot_summary dataframes, and address the following question:

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
Written Summary
