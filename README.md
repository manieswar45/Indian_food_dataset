# Food Images Classification with Transfer Learning using ResNet50

This repository contains a project focused on fine-tuning a pre-trained ResNet50 model for the classification of food images into 80 different categories. The project leverages transfer learning to adapt the ResNet50 model, originally trained on ImageNet, to classify food images efficiently.

## Project Overview

The goal of this project is to build an image classification model that accurately categorizes food images into one of 80 different classes. We use the ResNet50 model pre-trained on ImageNet and fine-tune it on our specific dataset.

### Key Steps:
1. **Data Preprocessing**: 
   - Images are resized to `224x224` pixels.
   - Data augmentation techniques are applied to enhance the diversity of the training set.

2. **Model Architecture**:
   - We use the ResNet50 architecture with the top classification layer removed.
   - The base model is frozen to retain the pre-trained weights.
   - A custom classification head is added, consisting of a Global Average Pooling layer, a Dropout layer for regularization, and a Dense layer with 80 units and softmax activation for multi-class classification.

3. **Model Training**:
   - The model is compiled using the Adam optimizer with a learning rate of `0.0001`.
   - The loss function used is Categorical Crossentropy, and the performance metric is Categorical Accuracy.

4. **Evaluation**:
   - The model’s performance is evaluated on a validation set using accuracy as the primary metric.
