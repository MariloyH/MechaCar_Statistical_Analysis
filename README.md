# MechaCar_Statistical_Analysis with R 

# Deliverable 1
## Linear Regression to Predict MPG. 
 In this deliverable, we are going to use multiple linear regression to predict which metrics  affect a car's performance measured in miles per gallon (mpg). To do this, I defined the null hypothesis as that none of the metrics that describe the cars affect their performance.
As part of the data exploration, I used R's function to plot each of the metrics vs. mpg, to see there were a correlation. From this plots, I could observe that only "vehicle_length" and "ground_clearance" seem to affect the mpg variable. 

 Subsequently, I used the R function for linear regression lm(), using all the variables in their dataframe. 
 The summary gave us the following data: **p-value = 5.35 e-11**, clearly less than 0.05, so we can **reject our null hypothesis and affirm that there is a correlation between the car's metrics and mpg**, that´s why **we can no consider zero our linear model slope**. The variables that provide a non-random amount of variance were **"vehicle_length" and "ground_clearance"**. Aditionally, looking at our predictor variable, R-squared has a value of 0.7149, so we can say that **71.49% of the mpg variability is predicted by our model, So this model is predicted effectively**. Finally the linear equation for our model will be: 
 ## y = -104 + 6.24x1 + 3.54 x2  
   where x1 is vehicle length and x2 ground clearance.
       
<img width="700" alt="D1Summary()" src="https://user-images.githubusercontent.com/102195803/179312746-40b806ab-b50a-446c-b56c-2015cb2c9508.png">

 # Deliverable 2
 ## Summary Statistics on Suspension Coils
 For this Deliverable, we took the data from Suspension_Coils.csv and we did some stats using R functions *summarize()* and *groupby().*
 The PSI stats for all the database were: 
 
 <img width="549" alt="total_summary" src="https://user-images.githubusercontent.com/102195803/179329342-dfad1081-bb6b-4697-bb57-37bbc8c5cffd.png">

 And the PSI stats by lot using summarize() and groupby() were: 
 
 <img width="630" alt="lot_summary" src="https://user-images.githubusercontent.com/102195803/179329429-3b7896bb-35c0-4bef-8589-9c7e875310d2.png">

The design specifications for the MechaCar Suspension Coils indicate that the variance of the Suspension Coils must not exceed 100 pounds per square inch. Although the all manufacturing lots in total, Lot 1 and Lot 2 meet the design specifiction, the Lot3 didn´t because its variance was 170, well above the variance of 100 psi established by the desgin specification.

# Deliverable 3 
## T-Test  on Suspension Coils 
For this deliverable, we  were asked for perform t-tests to determine if all manufacturing lots and each lot individually to search if they were  statistically different from the population PSI mean of 1,500 pounds per square inch.

Is there a statistical difference between the mean of the sample distribution and the mean of the population distribution? 
For the four cases,  I used the R function for  Student´s T-Test or simply t-test to compare the the mean of one dataset to another. because the T-Test answers this question. ppi. These were my hypthesis for all the cases. 

   H0 : There is no statistical difference between the observed sample mean and its presumed population mean.
   Ha : There is a statistical difference between the observed sample mean and its presumed population mean.

So, we calculate the T-Test.

   ### For all manufacturing lots. 
   
<img width="400" alt="Captura de Pantalla 2022-07-16 a la(s) 20 10 45" src="https://user-images.githubusercontent.com/102195803/179414528-94d79db0-c1de-4ade-8689-e524b2d57cdd.png">

 **In this case we can see that the p-value is the 0.06 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between all manufacturing lots PSI  mean that is 1,498.78 and the popultation mean 0f 1,500.**  

   ### Lot1 
<img width="400" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 08" src="https://user-images.githubusercontent.com/102195803/179414567-ffb5a3ff-9839-41c4-84ad-eb8d745b354a.png">

 **In this case we can see that the p-value is the 1 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between Lot1 PSI mean that is 1,500 and the popultation mean 0f 1,500.** 
 
   ### Lot2
<img width="400" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 27" src="https://user-images.githubusercontent.com/102195803/179414586-3812c6b4-8a2d-4f20-8e32-4f5d046d63a5.png">

**In this case we can see that the p-value is the 0.60 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between Lot2 PSI mean that is 1,500.2 and the popultation mean 0f 1,500.** 

   ### Lot3
<img width="400" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 42" src="https://user-images.githubusercontent.com/102195803/179414618-ad41d072-53df-4f95-add5-e85ab3c99989.png">

**In this case we can see that the p-value is the 0.041 so, its lower than 0.05, so our Null Hypothesis is FALSE, then our alternative hypothesis is TRUE, i.e. there is a statistical difference between Lot3 PSI mean that is 1,496.14 and the popultation mean 0f 1,500.**

# Deliverable 4
## Study Design: MechaCar vs Competition.

If we were asked to quantify how the MechaCar performs againts the competition, I selected the cost as the dependent, measured variable and cylinders, hp, city and highway fuel efficiency, safety rating and maintenance cost, each one as the single independent variable to evaluate in multiple groups. 
Then, I will select the **One Way ANOVA T-Test** for each metric, because  we need to compare metrics from several different populations, MechaCar and more than one competitor. Starting from these,  we formulate our hypothesis:

   H0 : The means of all groups are equal, or µ1 = µ2 = … = µn.
   Ha : At least one of the means is different from all other groups.  
   
And we make these assumptions to run the statitistical analysis about our input data from MechaCar and from the competitors:
   - The dependent variable is numerical and continuous, and the independent variables are categorical.
   - The dependent variable is considered to be normally distributed.
   - The variance among each group should be very similar.that we have MechaCar and competitor data are normally distribuided, 
And we need a large enough sample size,  to avoid Type 1 Error (False NULL).

  


