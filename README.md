### Unit-14-Homework-Neural-Net
We will be using deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the 'nth' closing price while the second model will use a window of closing prices to predict the 'nth' closing price.


Each model will use 70% of the data for training and 30% of the data for testing.
We will apply a MinMaxScaler to the X and y values to scale the data for the model.
Finally, we will reshape the X_train and X_test values to fit the model's requirement of samples, time steps, and features. (example: X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1)))

We will then evaluate the performance of each model.
Finally, use the testing data to evaluate each model and compare the performance.
Use the above to answer the following:

### Which model has a lower loss?
The loss is .09 on the FNG indicator model, whereas the loss on the closing price rolling window model is only .02 making it the clear winner. Even a glance at the line chart will show that it better maps the performance of the coin. In contrast, the fear and greed model predicted rolling waves but no breakout in price.
### Which model tracks the actual values better over time?
The fear and greed model predicted rolling waves but no breakout in price, remaining low despite the increase in the value of the currency. In contrast, the rolling closing price model correctly predicted a breakout in price and mapped the value of the coin much more accurately over the testing period.
### Which window size works best for the model?
Running with window size 4 and 8 with the COLAB "run all" command did not yeild better results for either model. Window size of 10 is displayed in the code attached here.
