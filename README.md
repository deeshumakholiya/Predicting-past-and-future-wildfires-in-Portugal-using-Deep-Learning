# Predicting-past-and-future-wildfires-in-Portugal-using-Deep-Learning

The study’s primary purpose was to construct a supervised machine learning model for predicting the occurrence of wildfires. The first objective of this thesis was "to investigate the data presented for the Portugal region using long-term time series analysis". To accomplish this, a variety of steps were undertaken. 
 * Both predictor variables and response variables were acquired from dependable climatological sources. 
 *The available data included 10 years of monthly data for the fire predictor, from 2001 to 2014, 18 years of monthly data for the vegetation (fPAR) predictor, from 2000 to 2018, and 36 years of daily data for the meterological predictor.
 * The data is split into a 10-year timeframe, i.e., from 2001 to 2014, for both the predictor variable and the response variable, or into 4932 timesteps. Using the CDO remapbil function, all predictor variables were initially remapped to a 0.25◦latitude × 0.25◦longitude grid depending on the fire dataset. 
 * To reduce the number of features in the final dataset, relevant features were extracted from individual datsets. 
 * Each netcdf dataset was then transformed from three dimensions to two dimensions by extracting each grid point from the 3D matrix and transforming it into a 2D matrix where each column is a lat lon grid with the time as the index.
* After completing this data transformation, correlation between the predictor and response variable was determined.
* The dataframe was then split into train and test sets and rescaled using standard scalar function from the sklearn library to prepare the data for prediction model analysis.
* I used five machine learning algorithms i.e. *Random Forest*, *Linear Regression*, *Artificial Neural Network*, *Long short-term memory (LSTM)*, *Seasonal AutoRegressive Integrated Moving Average(SARIMA) *, *Deep ConvLSTM Model*, that were trained and constructed using the available dataset of past fires for comparative analysis where the performance of each algorithm was adjusted using hyperparameters and then evaluated using the metrics in order to find the optimal method for predicting and forecasting future vegetation wildfires. 
* After a comprehensive investigation, it was determined that SARIMA was the algorithm that delivered the most appropriate results.
* To create a model that could analyze past fires and forecast future ones, I’ve implemented the SARIMA model, which yielded encouraging results for predicting vegetation fires and identifying the worst months and worst year during the whole study period. 

***Results***
* The worst fires during the study period for the worst year and for the worst month each year have also been calculated respectively. 
* I have also assessed the features that have the largest and least impact on the fire and computed their mean threshold values, which may be used to predict the incidence of fire in a given area. Using the prediction function of the SARIMAmodel, the future fire for one week following the study sample period has been forecasted.

## Contributing
Pull requests are welcome. 
For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
