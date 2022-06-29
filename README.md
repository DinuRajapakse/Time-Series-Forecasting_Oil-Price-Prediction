# Time Series Forecasting (Oil Price Prediction)
 
## Porblem Statement.

![image](https://user-images.githubusercontent.com/55726382/176496220-cc668bf6-8a3b-4d18-9176-7431d455ea86.png)

## Data formatting

The data was checked for seasonality and trend. Since there were none detected, the Date column was not considered a feature. However, since this is a time-series forecaster, in the name of good practice the Date column was converted to datetime format and set as index. Then all the NaN Date calues were removed from the data set. Figure 1 shows an section of the raw data.

![image](https://user-images.githubusercontent.com/55726382/176516341-eaa89ee6-fcb1-44d4-a3e7-a4c7cd4b59ca.png)

## Machine Learning Packages

All machine learning algorithms were programmed in Python using Jupyter Notebooks. Keras library, a wrapper for the Tensorflow, was used as the machine learning library to implement the said algorithms.
Two LSTM models were built: the baseline model and the alternative model. Both models only used ReLu as activation function.

## The Model, Results and Conclusion

### The Model
The baseline model did not include the Brent and WTI data. For comparison purposes, the model architecture was kept constant: 1 LSTM layer with 64 units, one intermediate dense layer with 32 nodes. The train and test set was split to the ratio of 70:30. The optimizer used was Adam. To evaluate the training and testing result for each product Root Mean Squared Error was used. The training prediction and testing prediction was plotted on the original data (Figure 2)

![image](https://user-images.githubusercontent.com/55726382/176516232-5d264271-fbe4-4eeb-a316-98d3f518c607.png)

### Results and Conclusion

To quantify the overall performance of the two models, the average testing and training scores of all 13 products was calculated. The results shows that the Brent and WTI data was not required to predict the sales prices of any of the products. The baseline model performed slightly better. But not significantly better. Summary of the results are shown below in Figure 3

![image](https://user-images.githubusercontent.com/55726382/176516094-ffa9aef2-04ab-4e52-b625-8162f0549374.png)






