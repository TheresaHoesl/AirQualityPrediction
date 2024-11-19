# AirQualityPrediction

In this project, weather data is used to predict the air quality of the next day for Ecke Taborstraße Glockengasse in Vienna, Austria. 
To train the model, air quality data from aqicn.org and weather data from open-meteo.org is fetched. Hopsworks is used to store the data.
* Notebook 1 covers the backfill of historical data into feature groups in Hopsworks
* Notebook 2 runs daily, gets todays air quality, weather data and the weather forecast and stores it into the existing feature groups
* Notebook 3 trains, validates a XGBRegressor and finally saves it
* Notebook 4 runs daily to predict the air quality for the next eight days using the weather forecast
  Additionally, we build another model which uses the mean of the previous three days air quality to predict air quality.

The forecast of the air quality for the next days as well as a hindcast to check how well the models predict can be found here: https://theresahoesl.github.io/AirQualityPrediction/
