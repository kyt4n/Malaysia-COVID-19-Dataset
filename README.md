## Malaysia COVID-19 Dataset
A free, publicly available Malaysia COVID-19 dataset

### Data Description
This dataset contains 28 variables, described in [data description.csv](https://github.com/kyt4n/Malaysia-COVID-19-Dataset/blob/main/data%20description.csv)

### Data Sources
Column 1 to 22 are Twitter data, which the Tweets are retrieved from Health DG [@DGHisham](https://twitter.com/DGHisham) timeline with Twitter API. [A typical COVID-19 situation update Tweet](https://twitter.com/DGHisham/status/1379730335328444416) is written in a relatively fixed format. Data wrangling are done in Python/Pandas, numerical values extracted with Regular Expression (RegEx). Missing data are added manually from Desk of DG ([kpkesihatan](https://kpkesihatan.com/)).

Column 23 ['remark'] is my own written remark regarding the Tweet status/content or other data.

Column 24 ['cumul_people_tested'] data is transcribed from an image on MOH COVID-19 website. Specifically, the [first image](http://covid-19.moh.gov.my/user/pages/02.terkini/01.2021/06.06/situasi-terkini-covid-19-di-malaysia-27062021/taburankes-all.jpg) under TABURAN KES section in each Situasi Terkini daily webpage of http://covid-19.moh.gov.my/terkini. If missing, the image from [CPRC KKM Telegram](https://t.me/s/cprckkm) or [KKM Facebook Live video](https://www.facebook.com/pg/kementeriankesihatanmalaysia/videos/) is used. Data in this column, dated from 1 March 2020 to 11 Feb 2021, are from [Our World in Data](https://github.com/owid/covid-19-data/tree/master/public/data), their data collection method as stated [here](https://ourworldindata.org/coronavirus-testing#malaysia). 

Column 25 to 28 are calculated data, where 
* ['people_tested'] = current row of ['cumul_people_tested'] - the previous row
* ['case_avg'] = average of last 7 rows of [cases]
* ['pos_rate'] = ['case']/['people_tested'] * 100
* ['pos_rate_avg'] = average of last 7 rows of ['pos_rate']

### Download
This dataset is also available at Kaggle [link](https://www.kaggle.com/yeanzc/malaysia-covid19-dataset).

### Guide on how to create this
* [Part 1 (Intro and Problem Statement)](https://kyle-tan.medium.com/malaysia-covid-19-dataset-creation-and-visualization-part-1-d2ca8b1f4c60?sk=56407b7afb3d41a35d7fbe287a73415a)
* [Part 2 (Workflow and Implementation)](https://kyle-tan.medium.com/malaysia-covid-19-dataset-creation-and-visualization-part-2-e65dbd9d856a?sk=150fdc9bc7338e78b7cbe13e50cc3630)
* Part 3 (Data Visualization with Tableau and Dashboard Publication)

### Why this dataset exist?
Ministry of Health (MOH) Malaysia does not provide the COVID-19 public health data in any easily accessible format. They only provide the raw numbers and text as is, along with infographics that are hardly informative. 

**UPDATE:
As of 23 Jul 2021, MOH Malaysia starts to to make their data public at https://github.com/MoH-Malaysia/covid19-public. However, it is still evolving and addition of scope and granularity of data is in progress.**

### Visualization on [Tableau Public](https://public.tableau.com/app/profile/tanky/viz/MalaysiaCovid-19Visualization/Overview)


