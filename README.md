# DS 4002: Project 3 - Is the Economy an Indicator of American Burnout?
## Contents

The Bureau of Labor and Statistics reported in 2020 that work-related stress drains the US economy by 300 billion dollars a year, making up 12% of our country’s GDP [1]. This study centers around the topic of chronic stress and ‘burnout’, a “syndrome conceptualized as resulting from chronic workplace stress that has not been successfully managed”, characterized by exhaustion and increased mental distance from one’s job [2]. This project seeks to investigate the relationship between workplace stress, productivity, and economic metrics, which indicate recessionary periods, periods of expansion, and unprecedented times (ex., dot com boom, COVID, etc.). These specific time periods of significant economic volatility are notable because they can be naturally stress-inducing. We use time series analysis to examine the relationship between Gallop’s stress index, organizational data for employee productivity, and the Bureau of Labor Statistics’ cost of labor index against quarter-over-quarter change in GDP [3-7].

Hypothesis: Workplace productivity measures and well-being indexes will be statistically significantly lower during recessionary periods compared to periods of growth according to quarter-over-quarter change in GDP per capita. 
Potenetial new hypothesis: Workplace productivity measures and stress indexes have a statistically significant synchronized relationship with quarter-over-quarter change in GDP per capita. 

### SRC


### Data

**Labor Productivity, Compensation, and Costs Data - Bureau of Labor and Statistics**
The data compiled from the [Bureau of Labor and Statistics]([https://stats.oecd.org/index.aspx?DataSetCode=ANHRS](https://data.bls.gov/cgi-bin/surveymost?bls) measures labor productivity per hour
two data sets were identified as reliable indicators of the American workforce, the Bureau of Labor and Statistics - Major Sector Productivity and Costs data, which includes real hourly labor productivity, real hourly compensation, and per unit labor costs by quarter from 1970-2022 in the US (1).
| Column      | Description   |
| :---        |    :---   |
| Year      | Year of recorded metric value (1970-2022)   |
| Quarter   | Quarter of recorded metric value (Q1-Q4)      |
| Metric   | The metric of the value in Value: <ul><li>“Labor Productivity” = Quantifiable output per hour from nonfarm business.</li><li>“Unit Labor Costs” = Unit labor costs from nonfarm business.</li><li>“Real Hourly Compensation” = Real hourly compensation from nonfarm business.     </li></ul>|
| Value   | Value of the metric |
| YrQtr   | Year and quarter of the metric value (i.e., 1970 Q1, 2022 Q3)      |


**Average Annual Hours Worked per Worker Data - OECD**
[Organisation for Economic Co-Operation and Development](https://stats.oecd.org/index.aspx?DataSetCode=ANHRS)
Data sourced by ncludes a measure of the average annual hours worked per American workers from 2010-2021 (2).

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
| Reference.Period.Code   | NA for all values      |
| Reference.Period   | NA for all values      |
| Value   | Total number of hours worked over the year divided by the average number of people in employment. The data are intended for comparisons of trends over time; they are unsuitable for comparisons of the level of average annual hours of work for a given year, because of differences in their sources.  Part-time workers are covered as well as full-time workers.      |
| Flag.Codes   | NA for all values      |
| Flags   | NA for all values      |


**Stress and Worry Data - Gallop Panel and National Health and Well-Being Index**
[Gallop Panel](https://www.gallup.com/174158/gallup-panel-methodology.aspx)
| Column      | Description   |
| :---        |    :----   |
| X.1      | Date survey was collected   |
| % Worry   | Percentage of american respondents who “frequently experience worry in daily life”      |
| % Stress   | Percentage of american respondents who “frequently experience stress in daily life”|

**Real GDP by Quarter - Fred Economic Research**
[Fred Economic Research](https://www.gallup.com/174158/gallup-panel-methodology.aspx](https://fred.stlouisfed.org/series/A191RL1Q225SBEA)
| Column      | Description   |
| :---        |    :----   |
| DATE      | Date in format YYYY-MM-DD    |
| A191RL1Q225SBEA   | Percent change in real gross domestic product from preceding period      |


### Figures

### References
[1] R. Cooke, “The Cost of Work Stress -- and How to Reduce it,” Ted, May, 2020. [Online]. Available: https://www.ted.com/talks/rob_cooke_the_cost_of_work_stress_and_how_to_reduce_it. [Accessed Nov. 2, 2022].
[2] “Burn-Out an “Occupational phenomenon": International Classification of Diseases,” World Health Organization, May 28, 2019. [Online.] Available: https://www.who.int/news/item/28-05-2019-burn-out-an-occupational-phenomenon-international-classification-of-diseases. [Accessed Nov. 2, 2022].
[3] “Top picks (most requested statistics),” U.S. Bureau of Labor Statistics. [Online]. Available: https://data.bls.gov/cgi-bin/surveymost?bls. [Accessed: 09-Nov-2022]. 
[4] L. Saad, “Eight in 10 Americans afflicted by stress,” Eight in 10 Americans Afflicted by Stress, 20-Dec-2017. [Online]. Available: https://news.gallup.com/poll/224336/eight-americans-afflicted-stress.aspx. [Accessed: 09-Nov-2022]. 
[5] D. Witters and S. Agrawal, “In U.S., poor life ratings reach record high,” Gallup.com, 22-Aug-2022. [Online]. Available: https://news.gallup.com/poll/397286/poor-life-ratings-reach-record-high.aspx. [Accessed: 09-Nov-2022]. 
[6] J. Ray, “Americans' stress, worry and anger intensified in 2018,” Gallup.com, 25-Apr-2019. [Online]. Available: https://news.gallup.com/poll/249098/americans-stress-worry-anger-intensified-2018.aspx. [Accessed: 09-Nov-2022]. 
[7] “Real gross domestic product,” FRED, 27-Oct-2022. [Online]. Available: https://fred.stlouisfed.org/series/A191RL1Q225SBEA. [Accessed: 09-Nov-2022]. 
[8] “Average annual hours actually worked per worker,” OECD. [Online]. Available: https://stats.oecd.org/index.aspx?DataSetCode=ANHRS. [Accessed: 09-Nov-2022]. 


