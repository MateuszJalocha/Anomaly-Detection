# Anomaly Detection

Meteorology is one of the fields using algorithms to find anomalies in a data set, and searching for weather anomalies using machine learning methods is the subject of numerous scientific works. The aim of this work is to create models which will be able to recognise weather anomalies in the best possible way. The study is based on data from Dublin Airport and includes hourly weather information from 1989 (00:00) to 31 October 2019 (23:00). The database is being updated with some delay, so the data we downloaded ends in October this year. This is unsupervised classification, so the observations are not defined in advance as weather anomalies, but this task is left to the classification methods. The potential outlier observations identified by the algorithms will then be verified on the basis of the weather description already included in the data set. The study was conducted in Python programming language. **K-Means**, **Isolation Forest** and **One-Class SVM** methods were used to create models to detect anomalies. **The Rand Index** method and a comparison of the results with the weather variables of the current and previous hour were used to select the method whose results turned out to be the best. Below are presented graphs with the location of weather anomalies on a two-dimensional dataset (K-means method) and a comparison of devpt variable density graphs for the anomaly and normal observations (Kmeans method). 

<p align="center">
<img align = "center" src ="Images/anomalyDetection_KMeans.png" /> <img align = "center" src ="Images/anomalyDetection_KMeans2.png" />
</p>

## Data

Data for Dublin airport is from the Irish Meteorological Service. These are hourly data collected from 1 January 1989 (00:00) to 31 October 2019 (23:00). The variables describing the weather at Dublin airport are:

- rain - Precipitation Amount (mm)
- temperature - Air Temperature (°C)
- wetb - Wet Bulb Air Temperature (°C)
- devpt - Dew Point Air Temperature (°C)
- vappr - Vapour Pressure (hPa)
- rhumidity - Relative Humidity (%)
- msl - Mean Sea Level Pressure (hPa)
- wdsp - Mean Hourly Wind Speed (kt)
- wddir - Predominant Hourly wind Direction (kt)
- sun - Sunshine duration (hours)
- vis - Visibility(m)
- clht - Cloud Ceiling Height - if none value is 999 (100s feet)
- clamt - Cloud Amount (okta)

In addition to the temperature measures mentioned above, the following values (which are not part of the dataset used to classification) are also present in the data set:

- w - Synop Code Past Weather
- ww - Synop Code Present Weather

SYNOP codes can take values from 0 to 99, they indicate the type of weather in the current and previous hours. Detailed meaning of all codes is given in the source files of the repository.

## Conclusions

On the basis of the results obtained in the study, it is not possible to clearly determine which method works best and to what extent it does it effectively. It should be taken into account that the detection of the anomaly does not necessarily involve the discovery of the beginning of weather changes to extremely dangerous. However, the results bring an informative value to the fact that the conditions are extremely abnormal and may be conducive to weather conditions that prove to be dangerous for nearby flights. Therefore, the models used in the project can be used to support the search, anticipation and prevention of situations that threaten the safety of people in the vicinity of Dublin airport. However, taking into account the analysis of variable distributions for the anomaly and its deficiencies, two-dimensional charts and weather analysis following the detected anomalies based on SYNOP codes, the Isolation Forest method seems to be the best in this case. The distribution of anomalies in two-dimensional diagrams is much more practical
than for the K-means method, due to the variance of the anomalies detected, while density distributions for selected variables differ greatly more than with the SVM method.

## Files

The analysis file is made in Polish, but comments in the files with code are in English.

- **Data directory** - you can find there a csv file with data and txt file with description of variables and Synops
- **PDF directory** - reasearch paper with analysis (polish language)
- **Images directory** - you can find there plots included in README
- **anomalyDetection.py** - project file

## Main libraries

- **sklearn** - Machine Learning

- **matplotlib.pyplot**, **seaborn**, **mpl_toolkits.mplot3d** - Visualization

- **pandas**, **numpy**, **dateutil**, **collections**, **itertools** - Generally useful libraries

## Contributors

- **Mateusz Jałocha** (mat.jalocha@gmail.com, https://www.linkedin.com/in/mateusz-jałocha/)
- **Jakub Ignatik** (https://github.com/JakubIg, https://www.linkedin.com/in/jakub-ignatik/)
- **Jakub Augustynek** (https://www.linkedin.com/in/jakub-augustynek-881a07188/)
