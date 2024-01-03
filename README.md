## 1. Neural Network Model

- The neural network model architecture is designed for image segmentation tasks using convolutional and deconvolutional layers.
- Batch normalization is used for normalization, and the ReLU activation function is applied after each convolutional layer.
- The model is compiled using the Adam optimizer and mean squared error as the loss function.

## 2. Training the Model

- The training data is loaded from pickle files (`full_CNN_labels.p` and `full_CNN_train.p`).
- The data is preprocessed, normalized, and split into training and validation sets.
- The model is trained using the `fit` method, specifying batch size, number of epochs, and validation data.
- Training progress is monitored using accuracy and loss metrics for both training and validation sets.

## 3. Training Progress (Epochs 1-20)

- The accuracy and loss values for each epoch are printed.
- The model's performance improves over epochs, as seen by decreasing loss and increasing accuracy for both training and validation sets.
- Training accuracy reaches approximately 96%, and validation accuracy reaches around 96.1%.
- The loss decreases, indicating that the model is learning the patterns in the data.

## 4. Visualization of Training History

- A plot is generated to visualize the training and validation loss over epochs.
- Another plot shows the training and validation accuracy over epochs.
- Both plots indicate that the model is learning well and not overfitting.

## 5. Model Evaluation

- The final accuracy is evaluated on both the training and validation sets.
- Training Accuracy: 96.16%
- Validation Accuracy: 96.12%

## 6. Saving and Loading the Model

- The trained model is saved to a file named 'full_CNN_model.h5'.
- The model summary is displayed.
- The saved model is loaded using `load_model` from `keras.models`.

## 7. Prediction on Validation Images

- Random images from the validation set are selected.
- The original images and the corresponding predicted images are displayed side by side.

## 8. Curve Detection and Measurement

- A function for curve detection (`detect_curve`) is provided.
- The length of the detected curve in pixels is measured using the `measure_length` function.
- The length is then converted to centimeters.

## 9. Interactive Image Annotation

- An interactive script allows the user to draw circles on an image by clicking the left mouse button.
- The script uses OpenCV and provides the coordinates of the clicked points.

## 10. Lane Detection Visualization

- Lane coordinates are manually specified, and lines are drawn on an image to represent lanes.
- The processed image is then displayed.

# Dataset

You can download the training dataset and labels from the following links:

- [Download full_CNN_train.p](https://www.dropbox.com/s/rrh8lrdclzlnxzv/full_CNN_train.p?dl=1)
- [Download full_CNN_labels.p](https://www.dropbox.com/s/ak850zqqfy6ily0/full_CNN_labels.p?dl=1)

