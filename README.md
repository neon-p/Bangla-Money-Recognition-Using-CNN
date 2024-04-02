# About
This project was part of a competition focused on image recognition, hosted by the "NEUB ICT Fest."
Our task was to develop a model capable of recognizing Bangla currency.
We processed raw images along with their corresponding labels.
To optimize computational efficiency, we resized all images to 120x250 pixels and converted them to grayscale.
These images were then represented as arrays to be fed into our model.
We used one-hot encoding for the output labels to categorize them into nine classes.
Our model architecture involved a Convolutional Neural Network (CNN) with multiple convolutional and max-pooling layers, followed by densely connected layers.
This architecture was chosen for its effectiveness in capturing spatial patterns and features within images.

## Dataset
- Source: [Bangla Money](https://www.kaggle.com/datasets/nsojib/bangla-money)

Train: 1637 samples

Test: 333 samples

Class: 9 classes

Image size: (120,250,3).

## Model Configuration
| Layer Type       | Configuration            |
|------------------|--------------------------|
| Input            | Input Shape: (120, 250, 1) |
| Convolutional    | Filters: 32, Kernel Size: (3, 3), Activation: ReLU, MaxPooling: Pool Size (2, 2) |
| Convolutional    | Filters: 64, Kernel Size: (3, 3), Activation: ReLU, MaxPooling: Pool Size (2, 2) |
| Convolutional    | Filters: 128, Kernel Size: (3, 3), Activation: ReLU, MaxPooling: Pool Size (2, 2) |
| Convolutional    | Filters: 256, Kernel Size: (3, 3), Activation: ReLU, MaxPooling: Pool Size (2, 2) |
| Flatten          | -                        |
| Fully Connected  | Units: 256, Activation: ReLU |
| Dropout          | Dropout Rate: 0.2         |
| Output           | Units: 9, Activation: Softmax |

## Result
We achieved an accuracy of 0.95299 followed by CNN model architecture.
