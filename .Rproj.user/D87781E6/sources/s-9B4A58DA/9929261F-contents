Cigarette Project 


Create a boxplot of the average number of packs per capita by state. Which states have the highest number of packs? Which have the lowest?

https://rpubs.com/programeralebrijes/796742

Find the median over all the states of the number of packs per capita for each year. Plot this median value for the years from 1985 to 1995. What can you say about cigarette usage in these years?

# A tibble: 11 × 2
    year meanPacks
   <int>     <dbl>
 1  1985     122. 
 2  1986     119. 
 3  1987     116. 
 4  1988     113. 
 5  1989     109. 
 6  1990     104. 
 7  1991     101. 
 8  1992      98.5
 9  1993      96.3
10  1994      95.0
11  1995      96.3

21.0656% decrease

What can you say about cigarette usage in these years?
 The usage os cigarettes desecrate 21.0656% during the 11 year period 

Create a scatter plot of price per pack vs number of packs per capita for all states and years.

https://rpubs.com/programeralebrijes/796777

Are the price and the per capita packs positively correlated, negatively correlated, or uncorrelated?
Explain why your answer would be expected.

The correlation of this hipotesis is negative correlated since the usage of cigarettes decreace 21% 


Change your scatter plot to show the points for each year in a different color. Does the relationship between the two variable change over time?

https://rpubs.com/programeralebrijes/796778

Do a linear regression for these two variables. How much variability does the line explain?

Call:
lm(formula = packpc ~ year, data = Cigarette)

Residuals:
    Min      1Q  Median      3Q     Max 
-56.566 -13.853  -2.646  10.701  80.819 

Coefficients:
             Estimate Std. Error t value Pr(>|t|)    
(Intercept) 5927.5923   580.8610   10.21   <2e-16 ***
year          -2.9252     0.2919  -10.02   <2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 21.21 on 526 degrees of freedom
Multiple R-squared:  0.1603,	Adjusted R-squared:  0.1587 
F-statistic: 100.4 on 1 and 526 DF,  p-value: < 2.2e-16

The plot above does not adjust for inflation. You can adjust the price of a pack of cigarettes for inflation by dividing the avgprs variable by the cpi variable. Create an adjusted price for each row, then re-do your scatter plot and linear regression using this adjusted price.


Create a data frame with just the rows from 1985. Create a second data frame with just the rows from 1995. Then, from each of these data frames, get a vector of the number of packs per capita. Use a paired t-test to see if the number of packs per capita in 1995 was significantly different than the number of packs per capita in 1985.

In the process of doing this project, have any questions come to mind that this data set could answer? If so, pick one and do the analysis to find the answer to your question.
