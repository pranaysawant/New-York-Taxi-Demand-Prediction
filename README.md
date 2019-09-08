# New-York-Taxi-Demand-Prediction
![NYC Taxi](http://www.nyc.gov/html/tlc/images/features/fi_about_photo_trip_records.png)




Predicting the demand for taxi in a interval of 10 minute
Requirements

Python-3.6.0

numpy--1.15.0

pandas--0.18.1

scikit-learn--0.19.0

dask--0.18.2

I have collected the data from http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml and can downloaded easily.

As pandas reads sequentially and requires a lot of ram for reading large csv files. So, I used Dask as it can be parallelized and is faster than pandas.

After the preprocsessing, trained a window based simple model and then trained various Regression models such as Random-Forest and XGBoost for reducing MAPE to less than 13%.

Concluding, I would say that the simple moving window model and its variants performed quite well and were very close to Regression models in terms of reducing MAPE.
