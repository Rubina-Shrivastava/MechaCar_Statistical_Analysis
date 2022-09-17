# MechaCar Statistical Analysis
## Purpose:
### AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management wants to review the production data for insights that may help the manufacturing team. In this challenge, we do the following:
#### 1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
#### 2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
#### 3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
#### 4. Design a statistical study to compare the vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
## Result:
## Linear Regression to Predict MPG:
### we can see image of MechaCar_mpg.csv
### Variables/coefficients provided a non-random amount of variance to the mpg values in the dataset:
### The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. All have p-Values that indicate a random amount of variance with the dataset. We can see into the following image
### Linear Regression Image
### The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indicates that the slope of this linear model is not zero.
### This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively.
### If we remove the less impactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability does decrease, but not drastically: the r-squared value falls from 0.7149 to 0. 6825.We can see into the following image 
### Liner Regression Summary Image 
## Summary Statistics on Suspension Coils:
### We can see image of Suspension Coils
### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and does not meet the design specifications. 
### Manufacturing Lot Summary Image
### The mean is 1498.78 for this sample and the population mean was determined to be 1500
### Summary by Manufacturing Lot Number Image
### Similarly, but significantly more consistent, Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, it is Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29. It is Lot 3 that is disproportionately causing the variance at the full lot level.
## T-Tests on Suspension Coils
### We can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 150
### T-Test for All Lots
### Lot 1 p-value = 1, alpha = .05 ,1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
### T-Test for Lot 1
### Lot 2 has essentially the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar
### T-Test for Lot 2
### Lot 3: p-value = .04168, alpha = .05, .04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.
### T-Test for Lot 3

## Study Design: MechaCar vs Competition
### MechaCar performs against the competition, then following metrics would be of interest to a consumer, could include cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
### Metric to test
### In order to analysis the MechaCar’s performance against the competition, I will measure the following three metrics: Cost, Fuel efficiency and Safety rating. Although there a multitude of possible metrics to consider, it may be useful to focus on how MechaCar's mean highway fuel efficiency in particular and compare it to the mean value of multiple competitors. The next metrics to test should be the safety rating, horsepower, and highway fuel efficiency, which address some safety concerns of consumer
### Null hypothesis or Alternative hypothesis
### The null hypothesis is that the mean of the safety rating is zero. The alternative hypothesis is that the mean of the safety rating is not zero. For example, Cost:
### Null Hypothesis: The means of cost of all vehicles in this class are equal.
### Alternative Hypothesis: At least one of the vehicles in this class has a different mean of cost than other vehicles.
### Fuel efficiency:
### Null Hypothesis: The means of fuel efficiency of all vehicles in this class are equal.
### Alternative Hypothesis: At least one of the vehicles in this class has a different mean of fuel efficiency than other vehicles.
### Safety rating:
### Null Hypothesis: The means of safety ratings of all vehicles in this class are equal.
### Alternative Hypothesis: At least one of the vehicles in this class has a different mean of safety rating than other vehicles.
### Statistical use to test the hypothesis
### In order to test the hypothesis that there is no statistical difference between the MechaCar prototype and the fuel efficiency of competitors, we could use a one-way ANOVA test. Also known as the analysis of variance test, the ANOVA test would allow us to test the null hypothesis that the means of all groups are equal. For example, cost we can use One-Way ANOVA test. This test will be used to test the mean cost of MechaCar with multiple other competition vehicles’ mean costs in the same class, for Safety also we can use One-Way ANOVA test and for Fuel efficiency we can use Two-Way ANOVA test. This test will be used to test the mean of fuel efficiency of MechaCar with multiple other competition vehicles’ mean fuel efficiency in the same class.
### data needed to run the statistical test
### To perform this ANOVA test, we would need one continuous, numerical variable for the dependent variable and MPG would satisfy that requirement. For example, for cost, we will need the cost of each of the 250 vehicles. For Fuel efficiency, I need two data points of each vehicle: mean fuel efficiency in the city and mean fuel efficiency on highway. For Safety rating, I need the mean safety rating of each vehicle.
