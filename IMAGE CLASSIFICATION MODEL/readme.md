Company: CODTECH IT solutions

Name: Archita Paul

Intern ID:CITSOD42

Domain: Machine Learning

Duration: 4 weeks

Mentor: Neela Santosh


### Image Classification on CIFAR-10 using Neural Networks

This project focuses on classifying images from the CIFAR-10 dataset using both an Artificial Neural Network (ANN) and a Convolutional Neural Network (CNN). The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 different classes, such as airplanes, cats, ships, and trucks.

1. Data Loading and Visualization
The dataset was loaded using TensorFlow's built-in CIFAR-10 loading function, which provided training and testing data. Initial exploration confirmed the data shapes, and sample images were visualized using Matplotlib to understand the nature of the dataset. A helper function was defined to display any image along with its class label.

2. Data Normalization
To improve model performance, the pixel values of images (ranging from 0 to 255) were normalized by dividing them by 255. This scaling helps speed up training and improves convergence in neural networks.

3. ANN Model (Baseline)
An Artificial Neural Network was built using Keras’ Sequential API. The model architecture included:

* A Flatten layer to convert 3D image input into 1D.
  
* Two Dense layers with 3000 and 1000 neurons respectively, both using ReLU activation.
  
* An output Dense layer with 10 units and softmax activation for multiclass classification.

* The model was compiled using Stochastic Gradient Descent (SGD) and trained for 5 epochs. After training, predictions were made on the test set, and model performance was evaluated using a classification report and confusion matrix. However, the accuracy was limited due to the ANN's inability to capture spatial features in images.

4. CNN Model (Improved)
To improve accuracy, a Convolutional Neural Network (CNN) was implemented. The CNN architecture included:

* Two Convolutional layers (with 32 and 64 filters respectively) followed by MaxPooling layers to downsample spatial dimensions

* A Flatten layer to convert the 3D output into 1D

* A Dense layer with 64 neurons and ReLU activation

* A final Dense layer with 10 units and softmax activation

The CNN was compiled using the Adam optimizer and trained for 3 epochs. This model was more effective in extracting spatial hierarchies and patterns from the images.

5. Evaluation and Prediction
The CNN was evaluated on the test dataset, showing significantly improved accuracy over the ANN. Predictions were visualized by displaying test images along with predicted labels. A list of predicted classes was generated using argmax to interpret the softmax output probabilities.
