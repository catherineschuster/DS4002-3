# DS 4002: Project 3 - Is the Economy an Indicator of American Burnout?
## Contents

The Bureau of Labor and Statistics reported in 2020 that work-related stress drains the US economy by 300 billion dollars a year, making up 12% of our country’s GDP [1]. This study centers around the topic of chronic stress and ‘burnout’, a “syndrome conceptualized as resulting from chronic workplace stress that has not been successfully managed”, characterized by exhaustion and increased mental distance from one’s job [2]. This project seeks to investigate the relationship between workplace stress, productivity, and economic metrics, which indicate recessionary periods, periods of expansion, and unprecedented times (ex., dot com boom, COVID, etc.). These specific time periods of significant economic volatility are notable because they can be naturally stress-inducing. We use time series analysis to examine the relationship between Gallop’s stress index, organizational data for employee productivity, and the Bureau of Labor Statistics’ cost of labor index against quarter-over-quarter change in GDP [3-7].

Hypothesis: Workplace productivity measures and well-being indexes will be statistically significantly lower during recessionary periods compared to periods of growth according to quarter-over-quarter change in GDP per capita. 
Potenetial new hypothesis: Workplace productivity measures and stress indexes have a statistically significant synchronized relationship with quarter-over-quarter change in GDP per capita. 

### SRC
Code Execution: The source code for this project contains two documents. (1) The code to compile, clean, and consolidate the source data into the data used in for EDA and preparation for timeseries analysis. This code is compatable with R Studio. (2) The code to conduct and analyze the timeseries forecasting process [2]. This code is compatible with python 3.0 or higher.

Code Usage: If you find our models or code useful, please add suitable reference to our project and in your work.

### Data

There are four datasets used in this project as follows:

#### **1. Labor Productivity, Compensation, and Costs Data - Bureau of Labor and Statistics**

The data compiled from the [Bureau of Labor and Statistics]([https://stats.oecd.org/index.aspx?DataSetCode=ANHRS](https://data.bls.gov/cgi-bin/surveymost?bls) measures labor productivity per hour, real hourly compensation, and per unit labor costs by quarter form 1970-2022 in the United States. This data set was identified as a useful and reliale mea and health of the Arican workforce, which wmeill contribute to 
two data sets were identified as reliable indicators of the American workforce, the Bureau of Labor and Statistics - Major Sector Productivity and Costs data, which includes real hourly labor productivity, rele indicator of the producityal hourly compensation, and per unit labor costs by quarter from 1970-2022 in the US (1).
| Column      | Description   |
| :---        |    :---   |
| Year      | Year of recorded metric value (1970-2022)   |
| Quarter   | Quarter of recorded metric value (Q1-Q4)      |
| Metric   | The metric of the value in Value: <ul><li>“Labor Productivity” = Quantifiable output per hour from nonfarm business.</li><li>“Unit Labor Costs” = Unit labor costs from nonfarm business.</li><li>“Real Hourly Compensation” = Real hourly compensation from nonfarm business.     </li></ul>|
| Value   | Value of the metric |
| YrQtr   | Year and quarter of the metric value (i.e., 1970 Q1, 2022 Q3)      |


#### **2. Average Annual Hours Worked per Worker Data - OECD**

This data sourced by the [Organisation for Economic Co-Operation and Development](https://stats.oecd.org/index.aspx?DataSetCode=ANHRS) contains a measure of the average annual hours worked per American workers from 2010-2021 [8]. This metric is used to compare the current state of American work against the backdrop of historical working trends.

| Column      | Description   |
| :---        |    :----   |
| COUNTRY      | Country of hours recorded (abbreviation)   |
| country   | Country of hours recorded      |
| EMPSTAT   | Type of Employment (abbreviation):   <ul><li>"DE” = “Dependent employment"</li><li>“TE” = "Total employment"</li></ul>|
| Employment.status   | Type of Employment:   <ul><li>“Dependent employment"</li><li>"Total employment"</li></ul>|
| FREQUENCY   | Frequency of metric recorded (abbreviation). “A” = "Annual" for all measures.      |
| Frequency   | Frequency of metric recorded. "Annual" for all observations.      |
| TIME   | Year      |
| Time   | Year      |
| Unit.Code   | Unit of annual hours worked value. “HOURS” for all observations.      |
| Unit   | Unit of annual hours worked value. “Hours” for all observations.      |
| PowerCode.Code   | 0 for all values      |
| PowerCode   | "Units" for all values      |
| Referencsur  | Date in format YYYY-MM-DD    |
| A191RL1Q225SBEA   | Percent change in real gross domestic product from preceding period      |

#### **3. Stress and Worry Data - Gallop Panel**

This dataset from the [Gallop Panel](https://www.gallup.com/174158/gallup-panel-methodology.aspx) contains American
survey data measuring important indicators of health and well-being. The Gallup Panel allows for a quick "pulse" of U.S. adults' opinions on some of the most pressing issues. The data of interest for this project includes the 

| Column      | Description   |
| :---        |    :----   |
| X.1      | Date survey was collected   |
| % Worry   | Percentage of american respondents who “frequently experience worry in daily life”      |
| % Stress   | Percentage of american respondents who “frequently experience stress in daily life”|


#### **4. Quarterly Real Gross Domestic Product Data - FRED Economic Data**

This Real GDP Data sourced by (FRED Economic Research)[https://fred.stlouisfed.org/series/A191RL1Q225SBEA] contains the percent change in real gross domestic product from 1949 to the present day. This metric will be used as the indicator of the health of the American economy.

| Column      | Description   |
| :---        |    :----   |
| DATE      | Date in format YYYY-MM-DD   |
| A191RL1Q225SBEA   | Percent change in real gross domestic product from preceding period      |


### Figures
Figures used include exploratory data analysis visualizations used to assess long term history trends in stress, real GDP, and labor metrics. Additionally, some figures included are graphical representations of our timeseries forecasting. 

### References
[1] R. Cooke, “The Cost of Work Stress -- and How to Reduce it,” Ted, May, 2020. [Online]. Available: https://www.ted.com/talks/rob_cooke_the_cost_of_work_stress_and_how_to_reduce_it. [Accessed Nov. 2, 2022].
[2] “Burn-Out an “Occupational phenomenon": International Classification of Diseases,” World Health Organization, May 28, 2019. [Online.] Available: https://www.who.int/news/item/28-05-2019-burn-out-an-occupational-phenomenon-international-classification-of-diseases. [Accessed Nov. 2, 2022].
[3] “Top picks (most requested statistics),” U.S. Bureau of Labor Statistics. [Online]. Available: https://data.bls.gov/cgi-bin/surveymost?bls. [Accessed: 09-Nov-2022]. 
[4] L. Saad, “Eight in 10 Americans afflicted by stress,” Eight in 10 Americans Afflicted by Stress, 20-Dec-2017. [Online]. Available: https://news.gallup.com/poll/224336/eight-americans-afflicted-stress.aspx. [Accessed: 09-Nov-2022]. 
[5] D. Witters and S. Agrawal, “In U.S., poor life ratings reach record high,” Gallup.com, 22-Aug-2022. [Online]. Available: https://news.gallup.com/poll/397286/poor-life-ratings-reach-record-high.aspx. [Accessed: 09-Nov-2022]. 
[6] J. Ray, “Americans' stress, worry and anger intensified in 2018,” Gallup.com, 25-Apr-2019. [Online]. Available: https://news.gallup.com/poll/249098/americans-stress-worry-anger-intensified-2018.aspx. [Accessed: 09-Nov-2022]. 
[7] “Real gross domestic product,” FRED, 27-Oct-2022. [Online]. Available: https://fred.stlouisfed.org/series/A191RL1Q225SBEA. [Accessed: 09-Nov-2022]. 
[8] “Average annual hours actually worked per worker,” OECD. [Online]. Available: https://stats.oecd.org/index.aspx?DataSetCode=ANHRS. [Accessed: 09-Nov-2022]. 


