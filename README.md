# Brain Tumor Classification Using Computer Vision

A computer vision project for classifying brain tumors from Magnetic Resonance Imaging (MRI) scans using deep learning.

## Problem Statement

Brain tumor detection can be challenging because tumors vary significantly in size, shape, location, and intensity. In early stages, tumor tissue may also resemble normal brain tissue, making accurate diagnosis more difficult.

The process can be time-consuming and places significant workload on radiologists, particularly in settings with limited access to skilled specialists. This project explores the use of computer vision and deep learning to assist in the classification and analysis of brain MRI images.

## Project Objective

The objective of this project is to develop and compare two convolutional neural network approaches for brain tumor classification:

* **Custom CNN** — A lightweight convolutional neural network designed specifically for the task.
* **ResNet50** — A transfer learning approach using a pre-trained ResNet50 architecture.

Both approaches classify MRI images into four brain tumor categories.

## Models

### Custom CNN

The custom CNN consists of three convolutional blocks using:

* Conv2D layers
* Batch normalization
* Max pooling
* Spatial dropout
* Global average pooling
* Dense layer
* Softmax classification layer

The network uses 32, 64, and 128 filters across the three convolutional blocks to progressively extract low-level, intermediate, and high-level visual features.

The model contains approximately **110,000 trainable parameters**, making it relatively lightweight for moderately sized MRI datasets.

### ResNet50

The second approach uses **ResNet50** with transfer learning from ImageNet.

The convolutional base is initially frozen and used as a feature extractor. Additional layers are added for the brain tumor classification task:

* Global average pooling
* Dense layer
* Dropout
* Softmax output layer

After initial training, the deeper layers are fine-tuned to adapt the pre-trained features to characteristics found in brain MRI images, such as tumor boundaries, texture irregularities, and intensity variations.

## Technologies

* Python
* TensorFlow / Keras
* Convolutional Neural Networks (CNN)
* ResNet50
* Computer Vision
* MRI Image Classification
* Google Colab

## Notebook

The included Google Colab notebook contains the implementation and experimentation for the brain tumor classification models.

> **Note:** This project is intended for educational and research purposes and is not a medical diagnostic system.
