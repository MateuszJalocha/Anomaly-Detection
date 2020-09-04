# Anomaly Detection

Meteorology is one of the fields using algorithms to find anomalies in a data set, and searching for weather anomalies using machine learning methods is the subject of numerous scientific works. The aim of this work is to create models which will be able to recognise weather anomalies in the best possible way. The study is based on data from Dublin Airport and includes hourly weather information from 1989 (00:00) to 31 October 2019 (23:00). The database is being updated with some delay, so the data we downloaded ends in October this year. The classification was carried out in an unsupervised manner, so the observation data are not defined in advance as weather anomalies, but this task is left to the classification methods. The potential outlier observations identified by the algorithms will then be verified on the basis of the weather description already included in the data set. The study was conducted in Python programming language. **K-Means**, **Isolation Forest** and **One-Class SVM** methods were used to create models to detect anomalies. The Rand Index method and a comparison of the results with the weather variables of the current and previous hour were used to select the method whose results turned out to be the best.

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

In addition to the temperature measures mentioned above, the following values, which are not part of the classification of observations, are also present in the data set:

- w - Synop Code Past Weather
- ww - Synop Code Present Weather

SYNOP codes can take values from 0 to 99, they indicate the type of weather in the current and previous hours. Detailed meaning of all codes is given in the source files of the work.

## Main libraries

- **sklearn** - Machine Learning

- **matplotlib.pyplot**, **seaborn**, **mpl_toolkits.mplot3d** - Visualization

- **pandas**, **numpy**, **dateutil**, **collections**, **itertools** - Generally useful libraries

## Contributors

- **Mateusz Jałocha** (mat.jalocha@gmail.com, https://www.linkedin.com/in/mateusz-jałocha-8942701b6/)
- **Jakub Ignatik** (https://github.com/JakubIg, https://www.linkedin.com/in/jakub-ignatik/)
- **Jakub Augustynek** (https://www.linkedin.com/in/jakub-augustynek-881a07188/)
