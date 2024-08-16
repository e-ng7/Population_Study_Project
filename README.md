# Introduction

This is a population research study conducted to determine the correlation of marriage and fertility rates. Through the extensive use of numpy, pandas and matplotlib libraries, datasets were clean, transform and visualise the statistical findings. Library functions such as 'diff' and 'corr' in the pandas library, were also used to compute the statistical measures required for this study. 

# Research Question: Is Singapore’s annual fertility rate less affected by marriages?

To investigate the looming population issues that Singapore faces, the Singapore government identifies the unwillingness to settle down or lack of marriages as a cause for plummeting fertility rates in the country. We aim to verify the cause of low fertility rates in Singapore by examining the association between marriages in Singapore and fertility rates. Using a combination of linear regression and ratio analysis, we derive two measures of correlations to gauge different aspects of the relationship between marriage and fertility in Singapore. The findings reveal that the relationship between marriage and fertility are still functional but not as relevant as before. There are also assumptions used in the approach of this study which needs to be further considered in the findings and other factors that may be more relevant to the fertility rates of Singapore.

# Statistical measurements used for this study
1) Coefficient of correlation
2) Ratio of % Change in Fertility Rate to % Change in Marriage Rates

# Data Cleaning & Transformation Performed
The datasets used in this study had many additional indices and words that had no value to the study. For instance, there was a row which detailed that the dataset was sourced from Singapore Department of Statistics. Since these additional rows were not useful to the study, I removed them by using the drop function and indicated the data frame index numbers. E.g. df = df.drop(df.index [22:26])

There were also other data quality issues in the fertility data set, where some columns had missing values. From earlier time periods like year 1961, there were no data collected and the only data input for no data collected was ‘na’. These missing data would be read in the data frames as ‘NaN’ and disrupt the results of the study. Thus, I should change all ‘na’ value to ‘0’. However, I chose to remove them with function drop.() again as most missing values were before year 1980 and outside the timeline used in this study.

After removing all the unwanted columns and index, we select the variables we want by using loc function and slice the variables by their names. The dataset was also not neatly organised with the years as columns and the variables like fertility rates as rows. To re-organise the dataset in the data frame, I transposed the data frame to invert the columns and rows. The variables name from the marriage dataset was also very lengthy and needed to be changed. Using df.rename(), I renamed the variables to a shorter name in the data frame. 

# Conclusion
From the measures calculated, we can conclude that the association between marriage and fertility is a direct one. A positive coefficient of correlation has shown that the act of marriage among Singaporeans will result in births and having more Singaporean women getting married would spur this trend even more than married Singaporean men. On the other hand, the deteriorating trend of sensitivity ratio between the two variables seem to raise an alarmingly trend of weakening effects of marriage on fertility rates. The sensitivity ratios are indicating that marriage may not be the strongest consideration for Singaporeans to have children anymore.

Yet, there are also limitations to this study that needs to be factored into the findings. Limitation includes the assumptions used in calculating the coefficient of correlation. Using Pearson’s correlation to compute the coefficient of correlation, we are assuming that marriage and fertility rates in the datasets should always be normally distributed and close to the mean. However, this may not always be the case as it is not entirely impossible to have very low marriage rates in some periods. 

The coefficient of correlation also assumes a linear relationship between the two variables. While this may be true when shown in the scatter plot (Figure 1), the sensitivity ratios indicate that the spread of the dots are likely to widen in the future and illustrate a less linear relationship. Hence, the assumption of a linear relationship may not be relevant in future studies. 

In summary, this study has shown that marriages in Singapore has led to higher births from 1980 to 2017. However, the influence of marriage in having children is waning and hints that marriage may not equate to children for Singaporeans. Marriage may still encourage Singaporeans to have children, but it is no longer the largest factor in the equation.

# See Also
[Source Code](./EMA.py) 
| 
[Full Research Report Study](https://drive.google.com/file/d/1vl-lwVDI0tsGcFcvrVDtkVm3OEMZZ5ZL/view?usp=sharing)
