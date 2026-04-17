# 🐟 Fish Species Classification using Deep Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-API-red)
![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab)

## 📌 Overview
This repository contains a Deep Learning project aimed at classifying 9 different species of fish from images. The project implements a **Custom Deep Neural Network (DNN)** built from scratch using TensorFlow and Keras. It demonstrates end-to-end machine learning workflow, including data preprocessing, extensive data augmentation, model building, and evaluation.

## 🗂️ Dataset
The project uses the `NA_Fish_Dataset`, which includes images of the following 9 fish species:
1. Black Sea Sprat
2. Gilt-Head Bream
3. Horse Mackerel
4. Red Mullet
5. Red Sea Bream
6. Sea Bass
7. Shrimp
8. Striped Red Mullet
9. Trout

> **Note:** Images are resized to `128x128x3` (RGB format) before being fed into the neural network.

## 🧠 Model Architecture
The custom Deep Neural Network (DNN) is designed to extract patterns from flattened images. The architecture consists of:
* **Input Layer:** `Flatten` layer to convert `128x128x3` images into a 1D array of 49,152 features.
* **Hidden Layer 1:** Dense (512 neurons) + Batch Normalization + ReLU Activation + Dropout (0.4)
* **Hidden Layer 2:** Dense (256 neurons) + Batch Normalization + ReLU Activation + Dropout (0.3)
* **Hidden Layer 3:** Dense (128 neurons) + Batch Normalization + ReLU Activation + Dropout (0.2)
* **Output Layer:** Dense (9 neurons) with `Softmax` activation to output probabilities for each of the 9 species.

## 🔄 Data Augmentation
To prevent overfitting and make the model more robust, the following transformations are applied during training using `ImageDataGenerator`:
* **Rotation:** up to 40 degrees
* **Width/Height Shift:** 20%
* **Shear & Zoom:** 20%
* **Horizontal Flip:** Enabled
* **Fill Mode:** Nearest

## 🚀 How to Run on Google Colab

This project is optimized to run on **Google Colab** with GPU acceleration.

1. **Clone this repository** (or download the `.ipynb` file):
   ```bash
   git clone [https://github.com/abderrahmanefrt/Fish-Species-Classification-DNN.git](https://github.com/abderrahmanefrt/Fish-Species-Classification-DNN.git)
