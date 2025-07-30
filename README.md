# Gesture Recognition using CNN

This project implements a deep learning-based gesture recognition system using Convolutional Neural Networks (CNNs). The model is trained to classify video sequences into one of five gesture categories using frame-level data extracted from videos.

---

## 🎯 Objective

Build a gesture classification model using a 3D CNN architecture capable of identifying five different hand gestures from video sequences. The dataset is sourced from UpGrad's gesture recognition challenge.

---

## 📂 Dataset Overview

- **Source:** Provided by UpGrad
- **Train Set:** ~500 video folders (each containing 30 frames)
- **Validation Set:** ~100 video folders
- **Classes:** 5 gesture labels
- **Format:** 30-frame sequences extracted from videos, saved as image folders

Each video is represented as a folder of 30 images. We use 15 frames per video, selected at regular intervals to reduce memory load.

---

## 🔍 Preprocessing

- Resized all images to `160x160`
- Selected 15 frames per video (odd-numbered frames from 1–29)
- Normalized pixel values to `[0, 1]`
- Used image generators for feeding batches during training (saves memory)

---

## 🧠 Model Architecture

A custom 3D Convolutional Neural Network (3D CNN) was implemented:

- 3D Conv Layer → 3D MaxPooling
- ReLU activations
- Batch Normalization
- Fully Connected Dense Layers with Dropout
- Final Softmax output layer

---

## ⚙️ Training Details

- **Loss Function:** Categorical Crossentropy  
- **Optimizer:** Adam  
- **Epochs:** 30  
- **Batch Size:** 32  
- **Evaluation Metric:** Validation Accuracy and Loss  
- **Final Accuracy Achieved:** ~94% on validation set

---

## 📈 Results

- The model was able to generalize well with high validation accuracy
- Frame-based selection strategy avoided overfitting
- Achieved fast convergence with data generators and normalization

---

## 📦 Requirements

See `requirements.txt` for the exact package versions used.

---

## 🚀 Future Improvements

- Replace 3D CNN with a CNN+LSTM hybrid for better temporal context
- Explore real-time webcam-based inference pipeline
- Try MobileNet or EfficientNet for edge deployment
