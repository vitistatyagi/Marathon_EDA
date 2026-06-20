
## Data Cleaning

* Identified and removed **282 duplicate records**.
* Found **35,848 entries with age = -1**, indicating that age information was missing. These values were retained as missing-age indicators for analysis.

## Exploratory Data Analysis (EDA)

### Dataset Overview

* The dataset contains marathon results from **2010 to 2019**.
* Participation is fairly evenly distributed across years, with each year contributing approximately **8–11%** of the total records.

### Performance Insights

* The **fastest marathon time** in the dataset was recorded in **2013**, with a finishing time of **7,425 seconds**.
* The **Chicago Marathon** accounts for **9 of the 10 fastest performances** recorded during the 10-year period.
* The **Top 10 fastest athletes** in the dataset are all male.

### Gender Comparison

* The average age of the **Top 10 male athletes** is **29.6 years**.
* The average age of the **Top 10 female athletes** is **29.0 years**.
* The difference between the fastest male and female marathon times is **619 seconds**.

### Age Bracket Analysis

* As expected, average finish times increase with age. Participants under 35 recorded the fastest average finish time of **16,242 seconds**, while runners aged **80 and above** recorded the slowest average finish time of **22,188 seconds**.

* When examining trends over time, the older age groups (75–79 and 80+) exhibit noticeable year-to-year fluctuations rather than a consistent increase or decrease in performance. For example, average finish times increased between **2010 and 2011**, indicating slower performances, before improving in subsequent years. A similar pattern is observed around **2016**, where finish times worsened before improving again.

* The **80+ age group recorded its slowest average finish time in 2018**, followed by an improvement in 2019. These fluctuations may be influenced by factors such as weather conditions, race-day circumstances, or differences in participant composition across years.


### Marathon-Level Analysis

* The **Marshall University Marathon** exhibits the smallest performance gap between men and women, with a difference of only **221 seconds**.
* The **Mo' Cowbell Marathon** ranks second, with a gap of **355 seconds**.


### Time Trends by Gender

* For male participants, average finishing times generally improved between **2010 and 2014**, followed by a decline in performance (higher finishing times) between **2015 and 2017**.
* Female participants exhibited a similar initial improvement; however, finishing times began increasing noticeably after **2014**, with a substantial increase of approximately **310 seconds**.
* Additionally, **2017 stands out as a relatively poor performance year across multiple age groups**, with higher average finish times observed throughout the dataset. Further investigation would be required to identify the factors contributing to this trend.

### Race-Level Analysis

- The top 5 races by participant count all exhibit right-skewed finishing-time distributions.
- Among these races, the Marine Corps Marathon shows the highest average finishing time.

### Participation Trends

- Participation peaked in 2013 before steadily declining through 2019.
- Male and female participation followed similar patterns:
  - Growth from 2010 to 2011
  - Significant increase in 2012
  - Peak participation in 2013
  - Consistent decline from 2014 to 2019
- More than 1,700 elite runners participated across the 10-year period.

### Player Analysis

- So here we trcaked a list of players who participated in races for more than 5 years. After looking at there median time for each year we came to the conclusion that the projectile trajectory was showing a genereal decline.
- Now look at the trend itself:
  - 2010 to 2012: times got faster (15047 → 14881)
  - 2012 to 2017: times steadily got slower (14881 → 15736)
  - 2017 to 2019: slight recovery (15736 → 15414)

### Data Quality Observation

* A notable inconsistency was found in the **Nike Women's Marathon**, where **1,565 male participants** were recorded.
* The analysis treated the **Gender** column as the source of truth. Possible explanations include:

  * Male pacers participating in the event
  * Unofficial participants
  * Incorrect race naming or labeling in the dataset

## Limitations

- The dataset does not contain a unique runner identifier.
- Performance analysis across multiple years can only be performed using participant names.
- Using names introduces ambiguity because:
  - Different runners may share the same name.
  - A runner's name may be recorded with spelling variations across races or years.
- As a result, longitudinal athlete-level analysis may contain inaccuracies.

## Project Status

🚧 Work in Progress

Current progress:
- Data cleaning completed
- Missing values analyzed
- Duplicate records removed
- Initial EDA completed
- Further analysis and visualizations in progress


