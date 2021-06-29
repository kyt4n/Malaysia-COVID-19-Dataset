## Malaysia COVID-19 Dataset
A free, publicly available Malaysia COVID-19 dataset


### Data Description
This dataset contains 28 variables, described in data description.csv

Column 1 to 23 are Twitter data, which the Tweets are retrieved from Health DG [@DGHisham](https://twitter.com/DGHisham) timeline with Twitter API. Data wrangling done in Python/Pandas, extracted numerical values with Regular Expression (RegEx).

Column 24 are data transcribed from MOH COVID-19 website. Specifically, the first image under TABURAN KES section in each Situasi Terkini daily page of http://covid-19.moh.gov.my/terkini

Column 25 to 28 are calculated data, where 
* ['people_tested'] = current row of ['cum_people_tested'] - the previous row
* ['case_avg'] = average of last 7 rows of [cases]
* ['pos_rate_perc'] = ['case']/['people_tested'] * 100
* ['pos_rate_perc_avg'] = average of last 7 rows of [pos_rate_perc]

This dataset is also available at Kaggle. [link](https://www.kaggle.com/yeanzc/malaysia-covid19-dataset)

## License

