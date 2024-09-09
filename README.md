# Plant Disease Classification Using Machine Learning

This project focuses on classifying plant diseases based on leaf images using machine learning techniques. The aim is to assist farmers in identifying common diseases in crops by developing a model capable of recognizing different types of plant diseases through visual symptoms on leaves.

## Table of Contents
- [Introduction](#introduction)
- [Problem Analysis](#problem-analysis)
- [Methodology](#methodology)
  - [Feature Extraction](#feature-extraction)
  - [Model Training](#model-training)
  - [Results and Evaluation](#results-and-evaluation)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction
In agriculture, crop yield is influenced by multiple factors such as weather, care techniques, and disease. This project aims to help identify diseases affecting plants by analyzing images of leaves. The model developed is capable of classifying leaves into four categories: **Combinations**, **Healthy**, **Rust**, and **Scab**.

## Problem Analysis
The diseases of interest in this project include:
- **Rust**: Characterized by yellow or orange spots on leaves.
- **Scab**: Identified by brown streaks on leaves.
- **Multiple diseases**: A combination of both yellow spots and brown streaks.

Due to an imbalance in the dataset, the "multiple-diseases" class has fewer examples compared to other classes, leading to potential challenges in training the model effectively.

## Methodology
The project involves several steps:

### Feature Extraction
The **VGG16** convolutional neural network (CNN) is used for feature extraction. VGG16, pre-trained on ImageNet, has been widely adopted for image classification tasks. It uses convolutional layers with a kernel size of 3x3, followed by pooling layers to reduce the feature map size, and ends with fully connected layers for classification.

### Model Training
After extracting features, a **Support Vector Machine (SVM)** is trained on the dataset. The data is split into training and test sets with an 80/20 ratio. SVM is an effective algorithm for image classification tasks and works by finding an optimal boundary between different classes using a kernel function.

### Results and Evaluation
The model performed well overall, but the **multiple-diseases** label was less accurately predicted due to data imbalance. Techniques like oversampling the minority class, undersampling the majority classes, or using ensemble methods could help improve the model's performance on this class.

## Conclusion
Image classification tasks like plant disease identification are becoming increasingly important in various fields. By recognizing symptoms early, farmers can take appropriate actions to mitigate the effects of diseases. This project highlights the importance of data preprocessing, choosing appropriate machine learning models, and addressing data imbalance issues to improve prediction accuracy.

## References
1. [Plant Disease Identification using SVM](https://ijcrt.org/papers/IJCRT2203059.pdf)
2. [Transfer Learning with CNN (VGG16) as Feature Extractor and Random Forest Classifier](https://www.youtube.com/watch?v=IuoEiemAuIY)
3. [Pattern Recognition and Experimental Applications - AI Recognition](https://www.youtube.com/watch?v=Pfd9vGIlB9c)
