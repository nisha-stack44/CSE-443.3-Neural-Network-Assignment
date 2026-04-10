** Problem Set 01: Pneumonia Detection from Chest X-Ray Images using CNN

** Objective
The main aim of this project is to build a CNN-based model that can identify whether a chest X-ray image belongs to a NORMAL patient or a PNEUMONIA patient. This type of system can be helpful in assisting medical professionals for faster and more reliable diagnosis.

**Dataset
The dataset used in this project consists of around 5,800+ chest X-ray images. It is organized into three main folders:

- train
- val
- test

Inside each folder, there are two categories:
- NORMAL
- PNEUMONIA

The images are taken from pediatric patients and are already arranged in a structured format, which makes them easy to use for training deep learning models.

**Methodology

** Data Preparation
At first, all images were scaled to bring pixel values between 0 and 1. This helps the model learn more efficiently.

To improve the training process, some augmentation techniques were applied on the training dataset such as slight rotation, zooming, and horizontal flipping. These steps help the model become more robust and reduce overfitting.

For validation and testing, only rescaling was applied to keep the evaluation fair.

**Data Loading
The dataset was loaded using `flow_from_directory`, which automatically assigns labels based on folder names. All images were resized to 150×150 pixels and processed in batches.

** Model Design
A simple CNN model was built step by step:

- Convolution layers were used to capture image patterns
- MaxPooling layers reduced the size of feature maps
- A Flatten layer converted the output into a vector
- A Dense layer helped in learning deeper relationships
- Dropout was added to reduce overfitting
- Finally, a sigmoid layer was used for binary classification

**Training Process
The model was trained using the Adam optimizer and binary crossentropy loss. Training was done for 15 epochs while observing validation performance after each epoch.

**Evaluation Metrics
To understand how well the model performs, the following metrics were used:

- Accuracy
- Loss
- Confusion Matrix
- Precision, Recall, and F1-score

** Results

** Test Performance
- Test Accuracy: **84.46%**
- Test Loss: **0.487**

**Model Behavior
The model performed very well on training data, achieving around 96% accuracy. However, validation accuracy was not very stable and kept changing across epochs. This indicates that the model might be slightly overfitting.

**Confusion Matrix
**text
[[142  92]
 [  5 385]]