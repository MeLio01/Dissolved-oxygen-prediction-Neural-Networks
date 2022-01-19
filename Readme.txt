first.ipynb : This notebook contains the final model. It was trained on the given data.
final.ipynb :  This notebook contains the same model as above. But the dataset was modified to get better results.

Model:
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


Conclusion:
- The model showed good results with the original data itself.
- For further improvement, the dataset was modified.
- The results would also have been better by increasing the epochs, neurons, or number of layers in the Neural Network. But after doing this, there would have been chances of  Overfitting.
