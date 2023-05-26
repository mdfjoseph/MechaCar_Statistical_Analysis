# MechaCar_Statistical_Analysis

## Project Overview
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management needs
help reviewing the production data for insights that may help the manufacturing team.

In this challenge, the following has been requested:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 
- For each statistical analysis, write a summary interpretation of the findings.

## Part 1: Linear Regression to Predict MPG
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to 
identify ideal vehicle performance. Multiple metrics were collected for each vehicle. RStudio will be used to design a linear model that predicts the mpg of MechaCar
prototypes using several variables from the MechaCar_mpg.csv file.

### Linear Regression 
Perform linear regression using the lm() function. In the lm() function, pass in all six variables.

![Screenshot 2023-05-25 at 7 48 06 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/4206f5d3-7d59-4676-8ddd-1a4d4d20ae7e)

### Summary Linear Regression Model
Using the summary() function, determine the p-value and the r-squared value for the linear regression model.

![Screenshot 2023-05-25 at 7 46 52 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/6122ddc7-da8e-496d-959c-dda13a582072)

#### 1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
The vehicle length and ground clearance variables provided non-random amounts of variance to the mpg values in the dataset.

#### 2. Is the slope of the linear model considered to be zero? Why or why not?
The p-Value (5.35e-11) is smaller than the assumed significance level of .05% which indicates that the slope of this model is not zero.

#### 3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The linear model has an r-squared value of .7149.  So, 71% of all mpg predictions can be determined by using this model.  Therefore, it will effectively predict the
mpg of MechaCar prototypes.

## Part 2:  Summary Statistics on Suspension Coils
The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils
were tested to determine if the manufacturing process is consistent across production lots. RStudio will be used to create a summary statistics table to show:
- The suspension coil’s PSI continuous variable across all manufacturing lots.
- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

### Total Summary Dataframe
Write an RScript that creates a total_summary dataframe using the summarize() function to get the mean, median, variance, and standard deviation of the suspension
coil’s PSI column.

![Screenshot 2023-05-25 at 7 52 01 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/cff44683-a2aa-4396-8cfe-1f1fb641e177)

### Lot Summary Dataframe
Write an RScript that creates a lot_summary dataframe using the group_by() and the summarize() functions to group each manufacturing lot by the mean, median, 
variance, and standard deviation of the suspension coil’s PSI column.

![Screenshot 2023-05-25 at 7 52 50 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/8de74e88-0ebd-4fc2-9baf-6ad1faaddd55)

#### 1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 
#### Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
The suspension coils variance is 62.39 and does not exceed the 100 pounds per square inch.  However, Lot 3 variance is 170.  It is very high and does not meet the 
design specifications.  Lot 1 and 2 have lower variances.

## Part 3:  T-Tests on Suspension Coils
Using RStudio, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds
per square inch.

### T-Test for All Manufacturing Lots
Write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 
pounds per square inch.



### Individual T-Tests for Three (3) Manufacturing Lots
Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each 
manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

![Screenshot 2023-05-25 at 9 02 38 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/c9bee650-b6a6-46b3-af97-5810c7d0c527)

#### T-Test:  Lot 1

![Screenshot 2023-05-25 at 9 02 44 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/f96a1c4d-07c4-4c21-9182-ed9678e598cc)

#### T-Test:  Lot 2

![Screenshot 2023-05-25 at 9 02 52 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/ea4a43ad-cb88-45d3-bc9d-0d5decb54b24)

#### T-Test:  Lot 3

![Screenshot 2023-05-25 at 9 03 03 PM](https://github.com/mdfjoseph/MechaCar_Statistical_Analysis/assets/114943747/efd6d26b-7026-4de9-ad5a-621b31998a04)

## Part 4:  Study Design: MechaCar vs Competition
Write a short description of a statistical study that can quantify how the MechaCar performs against the competition.

#### 1.  What metric or metrics are you going to test?
What is the Average Yearly Costs for Routine Car Maintenance for MechaCar and its competitors over the past 3 years?  

#### 2. What is the null hypothesis or alternative hypothesis?
Null Hypothesis:  The costs for routine car maintenance for MechaCar and its competitors is equal across the board.
Alternative Hypothesis:  Routine car maintenance for MechaCar vehicles costs less than the competitors' vehicles.

#### 3. What statistical test would you use to test the hypothesis? And why?
Using a multiple linear regression statistical summary would show how all the variables that impact the average yearly costs for rountine car maintenance for
MechaCar and its competitors.

#### 4. What data is needed to run the statistical test?
Use a random sampling of data collected by MechaCar and its competitors.  The data collected would include Vehicle type (i.e. Small, medium, 
midsized SUVs, Midsize pickups, half-ton crew cab pickups, hybrid, and electric), rountine maintenance costs (i.e. Oil change, Windshield wiper 
replacement, New battery, Brake pad replacement, and Tire rotation or replacement), data from the past 3 years in the United States.
