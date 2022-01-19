## Contents:
first.ipynb : This notebook contains the final model. It was trained on the given data.
final.ipynb :  This notebook contains the same model as above. But the dataset was modified to get better results.


## Data:
Initially, the distribution looked like this:
– Y-axis is the number of fields in the data, and the x-axis is the values of DO. 
– This plot shows how many fields are there for the given DO.
– It clearly shows that for DO>4, the frequency of data is significantly less. This will lead to more error for this portion of the data as our model will not be able to train itself sufficiently.

– It can be verified from this graph. Here the x-axis is the actual label for the training data, and the y-axis is the absolute difference between predicted and actual value.
– The difference is more for DO>4.
To minimize this error, data duplication was used. 
The data points between DO>=4 and DO<7 were replicated three times in the original dataset. And the data points between DO>=7 and DO<10 were repeated eight times.
After the duplication, the distribution looked like this:
– Here, the frequencies are more, and the data is more evenly distributed than earlier.
– This led to better results from the model.
– The difference error is relatively more minor as compared to earlier.
Therefore, this modified dataset was used for the final model.


## Model:
- A Neural Network regression model is used.
- It contains three layers. Each has 150, 450,100 neurons, respectively. The number of neurons was selected on a random basis by training the model with different neurons.
- Relu is used as the activation function for the hidden layers as it is a non-linear function.
- Root Mean Squared Error is the loss function.
- This model was trained with 1000 epochs.
- The result after training the model with the original dataset is: 
    loss: 0.6157 - rmse: 0.5921
    And the result after training the model with a modified dataset is:
    loss: 0.2854 - rmse: 0.2741
    Here the error is relatively less.


## Conclusion:
- The model showed good results with the original data itself.
- For further improvement, the dataset was modified.
- The results would also have been better by increasing the epochs, neurons, or number of layers in the Neural Network. But after doing this, there would have been chances of  Overfitting.
