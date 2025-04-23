# Linear-Regression-Time-Series-Aanalysis
A LINEAR MODEL TIME SERIES ANALYSIS is a kind of time series analysis prediction that forcasts time by creating a shift in the time 
thereby using the time shift created to predict the air-quality for the future
The Readings we predicted was the Air-Quality by using time stamp and the already recorded PM2.5 readings in the data
the dataset used had some columns....
imported all the libraries needed for the analysis...

sensor_id.....the sensor identity number

sensor_type.......the type of sensor that was used in the measurements

location.........location where the measurement was collected

lat..............latitude

lon...............longitude

timestamp...........time and date the measurement was collected

value_type...........the kind of measurement [P1, HUMIDITY, P2, TEMPERATURE, PRESSURE. HDOP]

value..............the values of the measurement 

before filtering te data records in the data was recorded using count visualizations

in this analysis...A shift in time(new column[P2.LI]) was created from the PM2.5 readings to be used as a predictor in the data 
both columns showed a strong correlation of 0.83 which showed a relatively strong predictio strength
a scatter plot was always used to show the relationship between both features
I had to filter out the data that wasn't being used...the timestamp was converted to a datetime format because it came as an object,
and the timezone had to be converted to the designated city [NAIROBI] in africa timezone...after that i needed to resample the data into 1HOUR INTERVALS and used forward fill to fill out the nan values
i could not fill the nan values with mean oe median bcause in time series analysis we can't fill with that...its like judging the present using the past and the future that we haven't lived.
converted the data into dataframe
a visualization of a rolling 7 days window was shown in the data to see how the air-quality fluctuates during the week
the data was splitted 80% for training set and 20% for testing sets
the mean values, mae baseline, training_mae and testing_mae values were collected.....the testing_mae value is higher than the training_mae which shouldn't be,
but because of the low data that was used in testing the data the mean_absolute_error was bigger tha thetraining mae

