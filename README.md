
# Japan Weekly Tourism Forecast

My first "proper" data analytics project, done as my submission for graduating from General Assembly.

It is for those like myself, whom love visiting Japan and do not want to deal with massive crowds. Most forecasts online are on a monthly level which I found only somewhat useful. 

This project aims at starting a framework for forecasting on a weekly basis.


## Datasets and How to Use
The main data set can be obtained here: https://statistics.jnto.go.jp/en/graph/#graph--breakdown--by--country

Google Trends data can be obtained here: https://destinationinsights.withgoogle.com/intl/en-GB_ALL/?campaignid=201

Full set working files (including dashboard and report): https://drive.google.com/drive/folders/16FqPk6PJJyaLKXDFDtDKsDHEV-FpY1hv?usp=drive_link

Monthly arrival data was obtained from 2015-2024. The years 2020-2022 inclusive were removed due to severe affectations by Covid.

I used the Google trend data to create relative strength of each week and then to use that to disaggregate monthly arrivals into weekly via the Chow-Lin method. 

For the top 6 largest contributors to tourist numbers, I included their public holidays and weeks in which they occur, I set a business rule of 30% higher arrivals. 

Once the weekly numbers were obtained, I trained 2 models on the years 2015-2019 to test on 2023-2024. Taking the best MAPE score model, I used that to predict seasonality in 2025/2026.
## Limitations and Assumptions
1) Assumptions of tourism seasonality: We utilized Google trends as a proxy for tourism weekly trend breakdown. And retrospectively applied it to prior years. This may or may not be accurate. Furthermore, Google is mostly used in Western countries. It does not accurately track seasonality from places such as China which is the largest source of tourists to Japan.

2) Lack of public holiday data: Due to workload, we are not able to obtain public holiday data for all of the inbound countries. 

3) Years broken down into 48 weeks: To simplify model calculations and weekly breakdown, years are broken into 48 weeks which may not be accurately expanded into 52 weeks. 

4) No details of individual cities in Japan: Dataset is for Japan as a whole. It does not consider seasonality of tourism to each of Japan’s main cities. This is due to a lack of data for each of them except Tokyo. 

5) No details of domestic tourism: We do not have data for Japan domestic tourism which can account for a large number of internal tourists. 

## Acknowledgements

A very large thank you to John my lecturer whom went above and beyond to help me understand the intricacies of data analysis. To my fellow classmates Zi Chuan and Azri whom helped me through the very intense months of study. 

