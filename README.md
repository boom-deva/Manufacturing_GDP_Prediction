## Problem Statement
Gross domestic product (GDP) is the value of all products produced in a country. It is also widely used to assess whether a country's economic situation is healthy. The gross domestic product includes all industries, and we can study the economic structure of a country through data analysis of industry contribution to GDP.

I just want to focus on one industry, so I chose the manufacturing industry as the target for forecasting GDP. Why chose the manufacturing industry? Manufacturing is one of the basic industries such as infrastructure construction and upgrading, high-precision processing, and industry support. It provides an important institutional foundation for learning and development process skills and competencies that are increasingly intertwined with core R&D in some of the industries most important to the future of the country's economy.

## Executive Summary 
The entire modeling process is divided into three distinct parts. The first part is the data collection. In order to predict the GDP, I did some study and decided which features may affect the GDP of Manufacturing Industry and make sure I can gather them from the government open source websites. Thus, the data were from multiple sources with diversity formats. In this case, I preprocessed all the data and changed the index to be equal to the year. Then, I merged the data together for data analysis.

The second part is the exploratory data analysis. I use a heat map to check the correlation of each feature to GDP. Due to the size of the function, I chose 8 features that represent a larger picture, including import, export, trade balance, population, employees, GDP and investment as a new data framework. I use the line graph to look at the relationship between annual GDP, imports, exports, and trade balance. Use bar charts to see the annual population, employee and investment changes.

The third part is modeling, which can be divided into feature selection and model selection. During feature selection, I only select "Import" as my feature (X variable) because it shows that 0.98 is related to GDP in the heat map, and GDP is my target (y variable). Then I applied the R^2 score to test the quality of the model. In the model selection, I tried linear regression, Lasso, Ridge and Random Forest Regressor. The score is high, so I check all the other features in the new data frame. Finally, I chose three and five features to build the models and make predictions.

## Conclusions 
First, since 2009, except for 2009, the growth trend of GDP and total imports has increased. The huge decline in 2009 was due to the financial crisis that began in the United States and the global economic recession that caused the world's economic recession. Export trends fell twice in 2009 and 2015 to 2016. For the year 2015 to 2016, the weak global economy and the strengthening of the US dollar, exports have fallen, making US goods and services more expensive. Second, the ridge model with five features, which include 'trade_balance', 'year', 'inv', 'population', and 'employee', worked the best. It showed 99 percent of the GDP can be explained by the model. 

## Source
- GDP Data: https://www.bea.gov/data/gdp/gdp-industry
- GDP Calculate and affect feactors:
    - https://courses.lumenlearning.com/boundless-economics/chapter/comparing-real-and-nominal-gdp/
    - https://www.slideshare.net/syler333/balance-of-payments-46077319
    - https://blog.marketresearch.com/the-growing-pharmaceuticals-market-expert-forecasts-and-analysis
- Investment from/to abroad Data: https://www.bea.gov/data/intl-trade-investment/direct-investment-country-and-industry
- Import/Export Data: https://www.census.gov/foreign-trade/index.html
- Employee Data: https://www.bls.gov/web/empsit/cesprog.htm#Industry_Classification
- US population Data: https://data.worldbank.org/indicator/SP.POP.TOTL?locations=US