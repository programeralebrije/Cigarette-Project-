install.packages("Ecdat")
library(Ecdat)
head(Cigarette)


# Create a boxplot of the average number of packs per capita by state. 

ggplot(Cigarette, aes(x=state, y=packpc)) + geom_boxplot()

# Which have the lowest?

Cigarette %>% group_by(packpc) %>% summarise(Mean=(state)) %>% 
  arrange(Mean)


Cigarette %>% group_by(packpc) %>% summarise(Mean=(state)) %>% 
  arrange(desc(Mean))

Cigarette %>% select(year, packpc) %>% group_by(year) %>% summarise(meanPacks = mean(packpc))
medianpackpc <- Cigarette %>% group_by(year) %>% summarise(Median=(packpc))
#Plot this median value for the years from 1985 to 1995.
unique(Cigarette$packpc)   
#Create a scatter plot of price per pack vs number of packs per capita for all states and years.
ggplot(Cigarette, aes(x=avgprs, y=packpc)) + geom_point() +
  geom_smooth(method = lm)
#Change your scatter plot to show the points for each year in a different color.
#Does the relationship between the two variable change over time?
ggplot(Cigarette, aes(x=avgprs, y=packpc, color=year)) + geom_point() +
  geom_smooth(method = lm)

#Do a linear regression for these two variables. How much variability does the line explain?

regression <- lm (packpc~year,Cigarette)
summary(regression)

#Call:
#lm(formula = packpc ~ year, data = Cigarette)

#Residuals:
#Min      1Q  Median      3Q     Max 
#-56.566 -13.853  -2.646  10.701  80.819 

#Coefficients:
#Estimate Std. Error t value Pr(>|t|)    
#(Intercept) 5927.5923   580.8610   10.21   <2e-16 ***
# year          -2.9252     0.2919  -10.02   <2e-16 ***
---
  #Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
  
  #Residual standard error: 21.21 on 526 degrees of freedom
  #Multiple R-squared:  0.1603,	Adjusted R-squared:  0.1587 
  #F-statistic: 100.4 on 1 and 526 DF,  p-value: < 2.2e-16
  
  #The plot above does not adjust for inflation. 
  #You can adjust the price of a pack of cigarettes for inflation by dividing the avgprs variable by the cpi variable. 

  Cigarette %>% mutate(avgprs= avgprs / cpi)
#Create an adjusted price for each row, then re-do your scatter plot and linear regression using this adjusted price.

ggplot(Cigarette, aes(x=avgprs, y=cpi)) + geom_point() +
  geom_smooth(method = lm)



