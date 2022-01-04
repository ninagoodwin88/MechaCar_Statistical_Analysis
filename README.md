# MechaCar Analysis - AutosRUs
"R", Rstudio
## Overview of Project

* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Linear Regression to Predict MPG

![d1](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/linear_regression_d1.png)

From the above output we can see that:

1. The **vehicle length**, and **vehicle ground clearance** are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. Conversely,
the **vehicle weight**, **spoiler angle**, and **All Wheel Drive** (AWD) have p-Values that indicate a random amount of variance with the dataset.  

2. The p-Value for this model, ```p-Value: 5.35e-11```, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to **reject our null hypothesis**, which further indcates that the slope of this linear model is **not zero**.


3.  This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model **does predict mpg of MechaCar prototypes effectively**. 

If we remove the less impactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability does decrease, but not drastically: the r-squared value falls from 0.7149 to 0.674. 

![d1](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/new_linear_regression_d1.png)

## Summary Statistics on Suspension Coils

#### Technical Analysis

## Total Summary

![d1](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/data-15-total-summary-data-mean-median-variance-sd.png)

## Lot Summary

![d1](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/data-15-manufacturing-lot.png)



The Suspension Coil dataset provided for the MechaCar contains the results of testing the weight capacities of multiple suspension coils from multiple production lots to determine consistency. 

First looking at all manufacturing lots:

![d2](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/total_lot_summary.png)

Diving a little deeper into each of the 3 lots:

![d2](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/manufactoring_lot_summary.png)



When looking at the entire population of the production lot, the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.  

Similarly, but significantly more consistent, Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively.  However, it is Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29.  It is Lot 3 that is disproportionately causing the variance at the full lot level.  

The below boxplot demonstrates the differences between the lots:

![d2](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/boxplot2.png)


## t-Tests on Suspension Coils

#### Technical Analysis

The next step is to conduct a t-test on the suspension coil data to determine whether there is a statistical difference between the mean of this provided sample dataset and a hypothesized, potential population dataset. Using the presumed **population mean of 1500**, we find the following:

There is a summary of the t-test results across **all manufacturing lots**
![d3](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/t_test_all.png)

From here we can see the **true mean of the sample is 1498.78**, which we also saw in the summary statistics above.  With a **p-Value of 0.06**, which is higher than the common significance level of 0.05, there is **NOT enough evidence to support rejecting the null hypothesis**.  That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500. 

**Next looking at each individual lots:**

1. Lot 1 sample actually has the **true sample mean of 1500**, again as we saw in the summary statistics above. With a **p-Value of 1**, do not reject (i.e. accept) the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).
2. Lot 2 has essentially the same outcome with a **sample mean of 1500.02**, a **p-Value of 0.61**; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar.
3. However, Lot 3, yeilded different results. Here **the sample mean is 1496.14** and the **p-Value is 0.04**, which is lower than the common significance level of 0.05.  All indicating to **reject the null hypothesis** that this sample mean and the presumed population mean are not statistically different.

 ![d3](https://github.com/ninagoodwin88/MechaCar_Statistical_Analysis/blob/main/Resources/Images/t_test_lot.png)

Lot Three production cycle was faulty. A process to check for system failures needs to be implemented. The suspension coils from Lot Three need to be inspected and faulty coils need to be removed.

## Study Design: MechaCar vs Competition

#### Hypothesis: Null and Alternative
After determining which factors are key for the MechaCar's genre:

 * Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.
 * Alternative Hypothesis (Ha): MechaCar is NOT priced correctly based on performance of key factors for its genre.
 
#### Statistical Tests
A **multiple linear regression** would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!)




