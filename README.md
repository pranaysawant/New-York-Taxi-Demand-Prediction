# New-York-Taxi-Demand-Prediction
![NYC Taxi](http://www.nyc.gov/html/tlc/images/features/fi_about_photo_trip_records.png)


Source: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page

The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC)
Note we have consider 2016 dataset. We have experimented on Jan 2016, Feb 2016 and March 2016 datasets.

## Medium Blog:
https://medium.com/@passionatedevs/taxi-demand-prediction-on-time-series-data-with-holt-winter-forecasting-loss-0-02-2bcdeec48499

<href src="https://medium.com/@passionatedevs/taxi-demand-prediction-on-time-series-data-with-holt-winter-forecasting-loss-0-02-2bcdeec48499">

<href src="https://medium.com/@passionatedevs/taxi-demand-prediction-on-time-series-data-with-holt-winter-forecasting-loss-0-02-2bcdeec48499" click me>

## Information on taxis:

<h5> Yellow Taxi: Yellow Medallion Taxicabs</h5>
<p> These are the famous NYC yellow taxis that provide transportation exclusively through street-hails. The number of taxicabs is limited by a finite number of medallions issued by the TLC. You access this mode of transportation by standing in the street and hailing an available taxi with your hand. The pickups are not pre-arranged.</p>

<h5> For Hire Vehicles (FHVs) </h5>
<p> FHV transportation is accessed by a pre-arrangement with a dispatcher or limo company. These FHVs are not permitted to pick up passengers via street hails, as those rides are not considered pre-arranged. </p>

<h5> Green Taxi: Street Hail Livery (SHL) </h5>
<p>  The SHL program will allow livery vehicle owners to license and outfit their vehicles with green borough taxi branding, meters, credit card machines, and ultimately the right to accept street hails in addition to pre-arranged rides. </p>
<p> Credits: Quora</p>

<h5>Footnote:</h5>
In the given notebook we are considering only the yellow taxis for the time period between Jan - Mar 2015 & Jan - Mar 2016


# Data Collection
We Have collected all yellow taxi trips data from jan-2015 to dec-2016(Will be using only 2015 data)
<table>
<tr>
<th> file name </th>
<th> file name size</th>
<th> number of records </th>
<th> number of features </th>
</tr>
<tr>
<td> yellow_tripdata_2016-01 </td>
<td> 1. 59G </td>
<td> 10906858 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-02 </td>
<td> 1. 66G </td>
<td> 11382049 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-03 </td>
<td> 1. 78G </td>
<td> 12210952 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-04 </td>
<td> 1. 74G </td>
<td> 11934338 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-05 </td>
<td> 1. 73G </td>
<td> 11836853 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-06 </td>
<td> 1. 62G </td>
<td> 11135470 </td>
<td> 19 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-07 </td>
<td> 884Mb </td>
<td> 10294080 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-08 </td>
<td> 854Mb </td>
<td> 9942263 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-09 </td>
<td> 870Mb </td>
<td> 10116018 </td>
<td> 17 </td>
</tr>

<tr>
<td> yellow_tripdata_2016-10 </td>
<td> 933Mb </td>
<td> 10854626 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-11 </td>
<td> 868Mb </td>
<td> 10102128 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2016-12 </td>
<td> 897Mb </td>
<td> 10449408 </td>
<td> 17 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-01 </td>
<td> 1.84Gb </td>
<td> 12748986 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-02 </td>
<td> 1.81Gb </td>
<td> 12450521 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-03 </td>
<td> 1.94Gb </td>
<td> 13351609 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-04 </td>
<td> 1.90Gb </td>
<td> 13071789 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-05 </td>
<td> 1.91Gb </td>
<td> 13158262 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-06 </td>
<td> 1.79Gb </td>
<td> 12324935 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-07 </td>
<td> 1.68Gb </td>
<td> 11562783 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-08 </td>
<td> 1.62Gb </td>
<td> 11130304 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-09 </td>
<td> 1.63Gb </td>
<td> 11225063 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-10 </td>
<td> 1.79Gb </td>
<td> 12315488 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-11 </td>
<td> 1.65Gb </td>
<td> 11312676 </td>
<td> 19 </td>
</tr>
<tr>
<td> yellow_tripdata_2015-12 </td>
<td> 1.67Gb </td>
<td> 11460573 </td>
<td> 19 </td>
</tr>
</table>

#### Problem statement :

Predicting Taxi Demand in New York city for future 10 minutes
# ML Problem Formulation
<p><b> Time-series forecasting and Regression</b></p>
<br>
-<i> To find number of pickups, given location cordinates(latitude and longitude) and time, in the query reigion and surrounding regions.</i>
<p> 
To solve the above we would be using data collected in Jan - Mar 2015 to predict the pickups in Jan - Mar 2016.
</p>


# Performance metrics
1. Mean Absolute percentage error.
2. Mean Squared error.

## Data Cleaning

All below points has outlier's points

1. Pickup Latitude and Pickup Longitude
2. Dropoff Latitude & Dropoff Longitude
3. Trip Durations
4. Speed
5. Trip Distance
6. Total Fare

When we plot BoxCox plot we observe outliers in above column so we simply remove those outliers

## Data Preprocess
#### Segmentation

We divide whole city into 40 parts and segmentation was done depends on no of frequecy for taxi demand. If certain segment has more numbers of trips then area of that segment is relatively small, if numbers of trip are less then area of that segment is large. 

We has used KMeans algorithm for segmentation of  whole new york city.

### Time Bin
As we divided whole city into segments, we also have divided time bin into parts.

### Baseline Model
As we know that we are dealing with time series data. we have to consider statistic terminological based model.

1. Simple Moving Average
2. Weighted Moving Average
3. Exponential Weighted Moving Averages



##  Train and Test Datasets
As we know that it is Time Series problem we cannot randomize the data, 70% data will use for training and 30% data we will use as test data.


# Machine Learning Models

<br> Exponential Model MAPE : 0.1349 </br>
<br> Liner Regression MAPE : 0.13468 </br>
<br> Random Forest MAPE: 0.13438 </br>
<br> XGBoost MAPE : 0.1392 </br>

# Feature Engineering
**Holt Winter forecasting**

Then we used "Triple Exponential Smoothing" and then again train on Random Forest and XGBOOST.

Random Forest MAPE: 0.04657
<br> XGBoost MAPE : 0.02932 </br>
# Conclusion

- Holt-Winter forecasting, triple exponential forecasting is tremendous feature for this task. Even hyperparam tunig in holt winter is also crucial. It reduce MAPE to 0.02 which is brillint.
- Without Holt-Winter feature, MAPE value was not reducing more than 13. Even with LSTM model.
