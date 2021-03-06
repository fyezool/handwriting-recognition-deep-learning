# Hand Written Digit Recognition
 Hand Written Digit Recognition using javascript library tensorflowjs
 
## Live Demo
https://deeplearning.faizul.me

## Model training
The model used here trained using Google Colab due to my development machine is not powerful. 

## Post training
Export the model as tensorflowjs compatible and use it in the script


## Start Predicting Hand Written Digit
* Draw on the canvas with your mouse on desktop or your finger on your mobile
* Click "Predict" to get result of the hand written digit prediction
* Click "Clean" to start drawing again

## Pre-trained model 
Use MNIST dataset from Keras with CNN (Convolutional Neural Network)
```python
model = keras.Sequential([
    keras.layers.Conv2D(32, (5, 5), padding="same", input_shape=[28, 28, 1]),
    keras.layers.MaxPool2D((2,2)),
    keras.layers.Conv2D(64, (5, 5), padding="same"),    
    keras.layers.MaxPool2D((2,2)),    
    keras.layers.Flatten(),   
    keras.layers.Dense(1024, activation='relu'),    
    keras.layers.Dropout(0.2),   
    keras.layers.Dense(10, activation='softmax')
])

model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
```

## Library
* [jquery](https://code.jquery.com/jquery-3.3.1.min.js) - JQuery
* [tensorflowjs](https://github.com/tensorflow/tfjs) - JavaScript library for training and deploying machine learning models
* [Chart.js](https://github.com/chartjs/Chart.js) - JavaScript library for display charts


