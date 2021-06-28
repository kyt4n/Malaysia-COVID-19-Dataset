## Malaysia COVID-19 Dataset
A free, publicly available Malaysia COVID-19 dataset\
\
\
This dataset contains 28 variables. Most are self-explanatory.

| No. | Variable           | Description                                                                         |
|-----|--------------------|-------------------------------------------------------------------------------------|
| 1   | date               | Date                                                                                |
| 2   | recovered          | Number of patients recovered                                                        |
| 3   | cum_recovered      | Cumulative number of patients recovered                                             |
| 4   | cum_recovered_perc | Cumulative number of patients recovered, out of all cumulative cases, in percentage |
| 5   | case               | Daily new cases                                                                     |
| 6   | cum_case           | Cumulative daily new cases                                                          |
| 7   | case_active        | Active cases                                                                        |
| 8   | case_local         | Local cases                                                                         |
| 9   | case_local_wn      | Local cases whom patient is a citizen                                               |
| 10  | case_local_bwn     | Local cases whom patient is a non-citizen                                           |
| 11  | case_import        | Import cases                                                                        |
| 12  | case_import_wn     | Import cases whom patient is a citizen                                              |
| 13  | case_import_bwn    | Import cases whom patient is a non-citizen                                          |
| 14  | death              | Deaths                                                                              |
| 15  | death_wn           | Deaths whom patient is a citizen                                                    |
| 16  | death_bwn          | Deaths whom patient is a non-citizen                                                |
| 17  | cum_death          | Cumulative deaths                                                                   |
| 18  | cum_death_percent  | Cumulative deaths out of all cumulative cases, in percentage                        |
| 19  | icu                | Number of patients in ICU                                                           |
| 20  | intubated          | Number of patients in ICU who are intubated                                         |
| 21  | tweet_id           | Tweet ID of the Tweet                                                               |
| 22  | link               | t.co shorten URL of the Tweet                                                       |
| 23  | remark             | brief remark, if any, about the Tweet status                                        |
| 24  | cum_people_tested  | Cumulative people tested                                                            |
| 25  | people_tested      | Daily people tested                                                                 |
| 26  | case_avg           | Number of new cases (7 day rolling average)                                         |
| 27  | pos_rate_perc      | Daily positivity rate, in percentage                                                |
| 28  | pos_rate_perc_avg  | Positivity rate percentage (7 day rolling average)                                  |


Column 1 to 23 are Twitter data, which the Tweets are retrieved from Health DG [@DGHisham](https://twitter.com/DGHisham) timeline with Twitter API. Data wrangling done in Python/Pandas, extracted numerical values with Regular Expression (RegEx).

Column 24 are data transcribed from MOH COVID-19 website. Specifically, the first image under TABURAN KES section in each Situasi Terkini daily page of http://covid-19.moh.gov.my/terkini

Column 25 to 28 are calculated data, where 
* [people_tested] = current row of [cum_people_tested] - the row before
* [case_avg] = sum of last 7 rows of [cases] / 7
* [pos_rate_perc] = ([case]/[people_tested]) * 100
* [pos_rate_perc_avg] = sum of last 7 rows of [pos_rate_perc] / 7

This dataset is also available at Kaggle. [link](https://www.kaggle.com/yeanzc/malaysia-covid19-dataset)

## License

