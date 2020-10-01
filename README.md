# Interpreting Influence of 2020 Snapchat Political Ad Campaign Spending and Run Time on User Impressions 

## Background 
The election for year 2020 is predicted to have one of the most [influential impacts on our political and economic landscape](https://thehill.com/homenews/campaign/479580-on-the-trail-why-2020-is-the-most-important-election-in-our-lifetime#:~:text=Raising%20the%20stakes%20even%20more%2C%202020%20marks%20a,the%20power%20to%20draw%20legislative%20and%20congressional%20boundaries). Through the power of social media and technology, platforms such as Snapchat have the capability to influence users by running political ads. The public data set for 2020 provided by [Snapchat](https://www.snap.com/en-US/political-ads/) was further analyzed in effort to gain transparency and insight of ad influence on users. The data has been filtered to include spending by advertisers only in USD and all age/sex demographics for snapchat users. The specific variables of interest explored were political ad spending in USD spent by advertisers and ad campaign run length in days to see the effects on number of user impressions, the number of times ad has been viewed. 

## Business Question
Can the number of impressions for a political advertisement be predicted depending on ad spending and length of run time? 

## Excel Data Analysis  

Through the use of multiple linear regression, the variables of ad spending and run time were evaluated against number of impressions. 
![Summary Output](https://github.com/EuniceNamkoong/Snapchat-Political-Ads-2020/blob/master/Snapchat_Summary_Output.PNG) 

The values of interest are highlighted above. 

### R Square Value 
This value indicates the percentage of data that can be explained by a linear regression model. Therefore, because the value of 0.72085493 is close to 1, it can be concluded that about 72.10% of data can be explained by the model.

### Standard Error 
Standard Error is (Standard deviation) / (square root of total number of samples) which simply shows how spread out the data points are within the interval.

### Significance F
This value shows whether or not the predictor variables matter to linear regression model fit. In other words, the lower the value, the better it is since it shows that the variables of interest contribute to the outcome. Therefore, the significance value of 0 shows that the variables DaysTotal and Spend contribute to the model. 

### P-Value 
This value shows the probability that the null hypothesis that the probability there is no relationship between variables is true. Because the P-Values are all less than 0.05, the variables are significant in predicting the number of impressions. 

### Coefficients 
Because all the other values outlined above signify that the variables DaysTotal and Spend affect the number of impressions, the coefficients can be confidently used to create a formula to predict future values. 
### Number of Snapchat Impressions = -425463.019 + 8391.165265*(DaysTotal) + 422.5802905*(Spend) 

## Excel Data Visualization 

![Scatter_Plot](https://github.com/EuniceNamkoong/Snapchat-Political-Ads-2020/blob/master/Snapchat_Scatterplot_Spending.PNG)

This scatter plot visually represents the relationship of spend (USD) to the number of impressions. Although the linear regression is not as accurate the multiple linear regression, the R^2 value of 0.7161 shows that there is a relationship. The linear regression and visualization of TotalDays vs. impressions was not included because the R^2 value was 0.0236, indicating a weak relationship. 

## Data Interpretation 
The formula that was derived from the multiple linear regression analysis can be a vital tool used by advertisers on social media platforms to predict future user engagement. The variable that had a deeper footprint in determining the number of impressions is the amount spent (USD) by the advertisers, as shown by the <0.001 p-value and high R^2 value in the singular linear regression model. Advertisers can use this formula to determine the costs vs. benefits in their financial decisions in creating ads and their run times. For future analysis of social media political campaign ads, additional data such as political stance of users, stance of ads, and length of social media posts could be critical in evaluating effective marketing.  

# Step by Step 
1. Download data set from public snapchat data set for 2020
1. Copy and paste data set into new excel sheet 
1. Use only categories for impression, spend, and start and end dates. Filter out data points so that only USD values are shown. 
1. Insert an extra column next to the startdate and endate columns. Split text to column by deliminating with space which will split up the date and time. 
1. Create a column named totaldays with a formula that determines days of campaign (start - end)
1. Run data analysis regression with y input as impression and x input as totaldays and spending 
1. Create scatterplot visualization for spending vs. impression, add trendline and regression equation 
