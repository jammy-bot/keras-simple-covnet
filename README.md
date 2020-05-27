# keras-simple-covnet
MNIST CNN with Keras, on Cloud (Google Colab) GPU

!["Image of a toasted sandwich cut in half and stacked, showing lettuce, tomatoes, and cheese."](./images/eiliv-sonas-aceron-mAQZ3X_8_l0-unsplash.jpg "width=200")*Just a few layers*

This project focuses on building a simple convolutional neural network model with Keras for cloud training.

## The Dataset

The project makes use of the MNIST image classification dataset, which consists of 60000 training samples and 10000 test (validation) samples. The dataset comprises 28x28 pixel grayscale images of handwritten digits in 10 classes, between 0 and 9.

## Objectives

The successfully validated model will be converted to a TPU Keras model.

#### Data Preparation

We load MNIST into our project notebook via the keras library's native `keras.dataset` package, which downloads the dataset from Amazon Web Service. From this point, we only need to split the data into train/ test sets and reshape the data vectors into matrices for GPU/ TPU backend training.

#### Modeling

The sequential model includes a hidden, convolutional layer with relu activation, followed by a max pooling layer and a dropout layer. These layers are then flattened. A hidden dense layer is next, followed by a dropout layer. A final, dense output layer uses softmax activation, which is appropriate for the multi - classification task.

#### Evaluation


The odel achieves an accuracy of 99.21\% on the test set, with a loss of 2.60\%.

# Technologies
* framework: Google Colaboratory/ Jupyter Notebook
* languages: Python
* libraries and modules:
  - Keras:
    * datasets
    * models
    * layers
    * backend
