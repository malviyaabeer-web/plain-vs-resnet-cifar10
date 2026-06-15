# Deep Residual Learning on CIFAR-10

This repository contains my implementation and reproduction of key ideas from the ResNet paper:

> Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun  
> **Deep Residual Learning for Image Recognition (2015)**

The goal of this project is to understand how residual connections help train deeper neural networks by comparing standard convolutional networks (Plain Networks) with Residual Networks (ResNets) on the CIFAR-10 dataset.

---

## Project Overview

This repository documents my learning journey in Deep Learning and Computer Vision through hands-on implementation and experimentation.

The experiments begin with a simple baseline CNN and progressively move toward deeper architectures inspired by the original ResNet paper.

The primary objective is to investigate:

- Why deep networks become difficult to optimize.
- How residual learning addresses the degradation problem.
- The performance difference between Plain Networks and Residual Networks of identical depth.

---

## Dataset

All experiments are performed on the CIFAR-10 dataset.

### CIFAR-10 Statistics

- 60,000 color images
- Image size: 32 × 32 × 3
- 10 object categories
- 50,000 training images
- 10,000 testing images

Classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

---

## Repository Structure

### 1. Baseline CNN

**Notebook:** `01_baseline_cnn_cifar10.ipynb`

A simple convolutional neural network used as a starting benchmark.

Architecture:

- Conv2D (32 filters)
- Conv2D (64 filters)
- Max Pooling
- Flatten
- Dense (128)
- Dense (10 Softmax)

Purpose:

- Understand the CIFAR-10 pipeline
- Establish a baseline for future experiments

---

### 2. Plain-20 vs ResNet-20

**Notebook:** `02_plain20_vs_resnet20_cifar10.ipynb`

This notebook reproduces one of the key comparisons from the ResNet paper.

Implemented:

#### Plain-20 Network

- 20-layer deep convolutional network
- Batch Normalization
- ReLU activations
- No shortcut connections

#### ResNet-20

- Residual Blocks
- Identity/Projection shortcuts
- Batch Normalization
- ReLU activations
- Global Average Pooling

The two networks are trained under the same conditions and compared directly.

---

## Key Concepts Explored

### Plain Networks

As network depth increases, optimization becomes more difficult and performance can degrade.

### Residual Learning

ResNet introduces shortcut connections:

F(x) + x

which allow gradients to flow more effectively through deep networks.

This helps:

- Faster optimization
- Better convergence
- Improved generalization

---

## Results

| Model | Test Accuracy |
|---------|---------:|
| Baseline CNN | ~66% |
| Plain-20 | ~74% |
| ResNet-20 | ~80% |

The ResNet architecture consistently outperformed the equivalent Plain Network, demonstrating the effectiveness of residual learning.

---

## Technologies Used

- Python
- NumPy
- Matplotlib
- TensorFlow
- Keras
- Google Colab

---

## What I Learned

Through this project I learned:

- CNN fundamentals
- Batch Normalization
- Global Average Pooling
- Functional API in TensorFlow/Keras
- Residual Connections
- Deep Network Optimization
- Research Paper Reproduction
- Experimental Comparison of Neural Architectures

---

## Future Work

Planned extensions:

- Plain-32 vs ResNet-32
- Data Augmentation
- Learning Rate Scheduling
- Training for More Epochs
- ResNet-56 Reproduction
- Comparison with Modern Architectures

---

## References

He, K., Zhang, X., Ren, S., & Sun, J.

**Deep Residual Learning for Image Recognition**

https://arxiv.org/abs/1512.03385

---

## Author

Abeer Malviya

Machine Learning and Deep Learning Enthusiast

GitHub: https://github.com/malviyaabeer-web
