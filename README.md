## Malaysia COVID-19 Dataset
A free, publicly available Malaysia COVID-19 dataset


### Data Description
This dataset contains 28 variables, described in [data description.csv](https://github.com/kyt4n/Malaysia-COVID-19-Dataset/blob/main/data%20description.csv)

### Data Sources
Column 1 to 22 are Twitter data, which the Tweets are retrieved from Health DG [@DGHisham](https://twitter.com/DGHisham) timeline with Twitter API. Data wrangling are done in Python/Pandas, numerical values extracted with Regular Expression (RegEx). Missing data are added manually from Desk of DG ([kpkesihatan](https://kpkesihatan.com/)).

Column 23 is my own written remark regarding the Tweet status/content.

Column 24 are data transcribed from MOH COVID-19 website. Specifically, the first image under TABURAN KES section in each Situasi Terkini daily webpage of http://covid-19.moh.gov.my/terkini. If missing, the data from [CPRC KKM Telegram](https://t.me/s/cprckkm) or [KKM Facebook Live video](https://www.facebook.com/pg/kementeriankesihatanmalaysia/videos/) is used. Data in this column, dated from 1 March 2020 to 11 Feb 2021, are from [Our World in Data](https://github.com/owid/covid-19-data/tree/master/public/data), their data collection method as stated [here](https://ourworldindata.org/coronavirus-testing). 

Column 25 to 28 are calculated data, where 
* ['people_tested'] = current row of ['cum_people_tested'] - the previous row
* ['case_avg'] = average of last 7 rows of [cases]
* ['pos_rate_perc'] = ['case']/['people_tested'] * 100
* ['pos_rate_perc_avg'] = average of last 7 rows of ['pos_rate_perc']

### Download
This dataset is also available at Kaggle [link](https://www.kaggle.com/yeanzc/malaysia-covid19-dataset).

### License
This Malaysia COVID-19 Dataset is made available under the Public Domain Dedication and License v1.0 whose full text can be found at: http://opendatacommons.org/licenses/pddl/1.0/

