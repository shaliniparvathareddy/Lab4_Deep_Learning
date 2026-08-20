# Deep CNN Architectures and Transfer Learning

## Overview

This project is a practical study of the evolution of Deep Convolutional Neural Network (CNN) architectures and transfer learning using TensorFlow/Keras.

The experiment studies and compares major CNN architectures including:

- LeNet-5
- AlexNet
- VGG16
- GoogleNet / Inception
- ResNet50

The project also demonstrates transfer learning and fine-tuning of pretrained CNN models using the CIFAR-10 dataset.

---

## Objectives

The main objectives of this experiment are:

- Study the evolution of deep CNN architectures.
- Compare LeNet-5, AlexNet, VGG16, GoogleNet and ResNet50.
- Understand transfer learning.
- Implement transfer learning using pretrained CNN models.
- Fine-tune pretrained CNN models.
- Compare classification performance using different evaluation metrics.
- Study the effect of different hyperparameters on model performance.

---

## Dataset

The experiment uses the **CIFAR-10 dataset**.

### Dataset Information

| Property | Value |
|---|---|
| Training Images | 50,000 |
| Testing Images | 10,000 |
| Number of Classes | 10 |
| Image Size | 32 × 32 × 3 |

### Classes

The ten classes in CIFAR-10 are:

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

The CIFAR-10 dataset is automatically downloaded through TensorFlow/Keras.

---

## CNN Architectures Studied

### 1. LeNet-5

LeNet-5 is one of the earliest practical CNN architectures.

Main characteristics:

- Convolutional layers
- Average pooling
- Fully connected layers
- Small number of parameters
- Originally designed for handwritten digit recognition

---

### 2. AlexNet

AlexNet achieved a major breakthrough in image classification.

Major contributions:

- ReLU activation
- Dropout
- GPU-based training
- Data augmentation
- Deeper CNN architecture

---

### 3. VGG16

VGG16 demonstrated the effectiveness of using multiple small convolution filters.

Main characteristics:

- 3 × 3 convolution filters
- Deep architecture
- Repeated convolution blocks
- High feature extraction capability

---

### 4. GoogleNet / Inception

GoogleNet introduced the Inception module.

The Inception module performs multiple operations in parallel:

- 1 × 1 convolution
- 3 × 3 convolution
- 5 × 5 convolution
- Pooling

The outputs are then concatenated.

This allows the network to extract features at different scales while keeping the number of parameters relatively low.

---

### 5. ResNet50

ResNet introduced residual learning using skip connections.

Instead of directly learning:

H(x)

the network learns:

F(x) = H(x) - x

and produces:

Output = F(x) + x

Residual connections make it possible to train much deeper neural networks.

---

# Transfer Learning

Transfer learning uses a CNN that has already been trained on a large dataset such as ImageNet.

The general workflow is:

```text
Pretrained CNN
      ↓
Remove Original Classifier
      ↓
Freeze Convolutional Layers
      ↓
Add New Classification Layers
      ↓
Train on CIFAR-10
      ↓
Fine Tune Selected Layers
      ↓
Evaluate Model
