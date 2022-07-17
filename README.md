# MechaCar_Statistical_Analysis with R 

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
  
  **From the summary, we can see that only the variables "vehicle_length" and "groun_clearance" provided a non-random amount of variance.**
    
  -Is the slope of the linear model considered to be zero? 
  **No** 
  Why or why not? 
  **Because we have correlacion between the metrics and and the dependent variable, mpg**
  
  -Does this linear model predict mpg of MechaCar prototypes effectively? 
  **Yes**
  
  Why or why not? 
  **Because in the summary we can observe that the R squared is**
 
 # Deliverable 2
 ## Summary Statistics on Suspension Coils
 For this Deliverable, we took the data from Suspension_Coils.csv and we did some stats using R functions summarize an groupby
 
 The PSI stats for all the database were: 
 
 <img width="549" alt="total_summary" src="https://user-images.githubusercontent.com/102195803/179329342-dfad1081-bb6b-4697-bb57-37bbc8c5cffd.png">

 And the PSI stats by lot using summarize() and groupby() were: 
 
 <img width="630" alt="lot_summary" src="https://user-images.githubusercontent.com/102195803/179329429-3b7896bb-35c0-4bef-8589-9c7e875310d2.png">

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? **No** Why or why not?
Because the Variance for the lot3 is greater than 100 psi.

# Deliverable 3 
## T-Test  on Suspension Coils 
For this deliverable, we  were asked for perform t-tests to determine if all manufacturing lots and each lot individually to search if they were  statistically different from the population PSI mean of 1,500 pounds per square inch.

Is there a statistical difference between the mean of the sample distribution and the mean of the population distribution? 
For the four cases,  I used the R function for  Student´s T-Test or simply t-test to compare the the mean of one dataset to another. because the T-Test answers this question. ppi. These were my hypthesis for all the cases. 

   H0 : There is no statistical difference between the observed sample mean and its presumed population mean.
   Ha : There is a statistical difference between the observed sample mean and its presumed population mean.

So, we calculate the T-Test.

   ### For all manufacturing lots. 
   
<img width="656" alt="Captura de Pantalla 2022-07-16 a la(s) 20 10 45" src="https://user-images.githubusercontent.com/102195803/179414528-94d79db0-c1de-4ade-8689-e524b2d57cdd.png">

 **In this case we can see that the p-value is the 0.06 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between all manufacturing lots PSI  mean that is 1,498.78 and the popultation mean 0f 1,500.**  

   ### Lot1 
<img width="657" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 08" src="https://user-images.githubusercontent.com/102195803/179414567-ffb5a3ff-9839-41c4-84ad-eb8d745b354a.png">

 **In this case we can see that the p-value is the 1 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between Lot1 PSI mean that is 1,500 and the popultation mean 0f 1,500.** 
 
   ### Lot2
<img width="660" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 27" src="https://user-images.githubusercontent.com/102195803/179414586-3812c6b4-8a2d-4f20-8e32-4f5d046d63a5.png">

**In this case we can see that the p-value is the 0.60 so, its more than 0.05, so our Null Hypothesis is true, i.e. there is no  statistical difference between Lot2 PSI mean that is 1,500.2 and the popultation mean 0f 1,500.** 

   ###Lot3
<img width="648" alt="Captura de Pantalla 2022-07-16 a la(s) 20 11 42" src="https://user-images.githubusercontent.com/102195803/179414618-ad41d072-53df-4f95-add5-e85ab3c99989.png">

**In this case we can see that the p-value is the 0.041 so, its less than 0.05, so our Null Hypothesis is FALSE, then our alternative hypothesis is TRUE, i.e. there is a statistical difference between Lot3 PSI mean that is 1,496.14 and the popultation mean 0f 1,500.**



# Deliverable 4
Deliverable 4: Design a Study Comparing the MechaCar to the Competition (20 points)
Deliverable 4 Instructions
Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

Follow the instructions below to complete Deliverable 4.

In your README, create a subheading ## Study Design: MechaCar vs Competition.
Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
In your description, address the following questions:
What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?
