# Gesture Recognition Using CNN

This deep learning project aims to classify hand gestures from image frames using a Convolutional Neural Network (CNN).

## ✋ Problem Statement
Accurately identify static hand gestures (A-E) from preprocessed video frames.

## 📸 Dataset
- Image frames (converted from videos)
- Grayscale input, resized to 64x64 pixels
- 5 classes: A, B, C, D, E

## ⚙️ Approach
- CNN architecture with dropout and max pooling
- Used data augmentation for robustness
- Trained with categorical crossentropy loss

## 🏆 Results
- Accuracy: ~91% on test set
- Confusion matrix shows strong class separation

## 🧰 Tech Stack
`Python`, `TensorFlow`, `Keras`, `OpenCV`, `Matplotlib`
