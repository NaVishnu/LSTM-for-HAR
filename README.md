# LSTM-for-HAR
A Long Short Term Memory network model for Human Activity Recognition

Human Activity Recognition, or HAR for short, is the problem of predicting what a person is doing based on a trace of their movement using sensors. A standard HAR dataset is the "Human Activity Recognition Using Smartphones Data Set" made available in 2012. It was prepared and made available by Davide Anguita, et al. rom the University of Genova, Italy. The data was collected from 30 subjects aged between 19 and 48 years old performing one of six standard activities while wearing a waist-mounted smartphone that recorded the movement data. The six activities performed were,
                                        i) Walking
                                        ii) Walking Upstairs
                                        iii) Walking Downstairs
                                        iv) Sitting
                                        v) Standing
                                        vi) Laying        
                                        
The smartphone used was a Samsung Galaxy S II. The movement data recorded was the x, y, and z accelerometer data (linear acceleration) and gyroscopic data (angular velocity) from the smart phone. 

The dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). 

The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

A LSTM network model has been developed for the dataset. LSTM network models are a type of recurrent neural network that are able to learn and remember over long sequences of input data. They are intended for use with data that is comprised of long sequences of data, up to 200 to 400 time steps. They may be a good fit for this problem. The model can support multiple parallel sequences of input data, such as each axis of the accelerometer and gyroscope data.

The model learns to extract features from sequences of observations and how to map the internal features to different activity types. The benefit of using LSTMs for sequence classification is that they can learn from the raw time series data directly, and in turn do not require domain expertise to manually engineer input features. The model can learn an internal representation of the time series data and ideally achieve comparable performance to models fit on a version of the dataset with engineered features.
