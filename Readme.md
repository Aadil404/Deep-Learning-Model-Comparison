# 🧠 Comparative Analysis of Deep Learning Architectures on MNIST and CIFAR-10

This project presents a **comparative analysis** of multiple deep learning architectures — **VGG16**, **AlexNet**, **GoogLeNet**, **RNN (LSTM)**, and **CNN** — trained and evaluated on benchmark datasets **MNIST** and **CIFAR-10**.  
The objective is to investigate how different **train-test splits** affect model performance and to analyze results using key evaluation metrics such as **accuracy**, **loss**, **confusion matrix**, **ROC curve**, and **AUC**.

---

## 📘 Table of Contents
- [Overview](#overview)
- [Architectures Compared](#architectures-compared)
- [Datasets Used](#datasets-used)
- [Experimental Setup](#experimental-setup)
- [Results Summary](#results-summary)
  - [MNIST Results](#mnist-results)
  - [CIFAR-10 Results](#cifar-10-results)
- [Analysis](#analysis)
- [Conclusion](#conclusion)

---

## 🧩 Overview

This study explores how **different deep learning architectures** perform on simple and complex visual datasets.  
Models were trained with **two validation splits (10% and 20%)** to evaluate how the amount of training data impacts generalization.

Each model’s performance was measured using:
- **Test Accuracy**
- **Test Loss**
- **Confusion Matrix**
- **ROC Curve**
- **AUC Score**

---

## 🏗️ Architectures Compared

| Model Type | Description |
|-------------|-------------|
| **AlexNet** | Early CNN architecture known for its simplicity and effectiveness on image classification tasks. |
| **VGG16** | Deep convolutional network with small receptive filters (3×3), emphasizing depth. |
| **GoogLeNet (Inception)** | Employs inception modules to capture multi-scale features efficiently. |
| **RNN (LSTM)** | Sequential model tested for visual data performance, exploring temporal dependency learning. |
| **CNN (Baseline)** | Traditional convolutional architecture serving as a control model. |

---

## 🧮 Datasets Used

| Dataset | Description | Image Size | Classes |
|----------|--------------|-------------|----------|
| **MNIST** | Handwritten digits (0–9) | 28×28 (Grayscale) | 10 |
| **CIFAR-10** | Natural color images (airplane, cat, car, etc.) | 32×32 (RGB) | 10 |

---

## ⚙️ Experimental Setup

- Framework: **TensorFlow / Keras (or PyTorch, if applicable)**
- Optimizer: **Adam**
- Learning Rate: **0.001**
- Batch Size: **128**
- Epochs: **30–50**
- Validation Splits: **10% and 20%**
- Metrics: **Accuracy, Loss, ROC-AUC**

---

## 📊 Results Summary

### 🧾 MNIST Results

| Model | Validation Split | Test Loss | Test Accuracy |
|--------|------------------|------------|----------------|
| **AlexNet (Simple)** | 10% | 0.022809 | 0.9921 |
| **AlexNet (Simple)** | 20% | 0.026478 | 0.9911 |
| **GoogLeNet (Simple)** | 10% | 0.035066 | 0.9885 |
| **GoogLeNet (Simple)** | 20% | 0.035241 | 0.9887 |
| **RNN (LSTM)** | 10% | 0.071020 | 0.9809 |
| **RNN (LSTM)** | 20% | 0.065692 | 0.9809 |
| **VGG16 (Simple)** | 10% | 0.019945 | 0.9937 |
| **VGG16 (Simple)** | 20% | **0.019748** | **0.9942** |

✅ **Best MNIST Model:** VGG16 (Val Split 20%)  
🟩 **Highest Accuracy:** 99.42%  
🟩 **Lowest Loss:** 0.0197  

---

### 🎨 CIFAR-10 Results

| Model | Validation Split | Test Loss | Test Accuracy |
|--------|------------------|------------|----------------|
| **AlexNet** | 10% | 0.812362 | 0.7879 |
| **AlexNet** | 20% | 1.008787 | 0.7647 |
| **GoogLeNet** | 10% | 0.623932 | **0.7941** |
| **GoogLeNet** | 20% | 0.624876 | 0.7903 |
| **RNN (LSTM)** | 10% | 1.214281 | 0.5842 |
| **RNN (LSTM)** | 20% | 1.206890 | 0.5753 |
| **VGG16** | 10% | 1.087513 | 0.6212 |
| **VGG16** | 20% | 1.094925 | 0.6198 |

✅ **Best CIFAR-10 Model:** GoogLeNet (Val Split 10%)  
🟩 **Highest Accuracy:** 79.41%  
🟩 **Lowest Loss:** 0.6239  

---

## 🔍 Analysis

- **VGG16** excelled on **MNIST**, leveraging its deep architecture to extract fine-grained spatial features.  
- **GoogLeNet** performed best on **CIFAR-10**, likely due to its **Inception modules** capturing multi-scale image features effectively.  
- **RNNs** underperformed, reaffirming that **sequential architectures** are not ideal for spatial image data.  
- A **10% validation split** generally yielded slightly better results on CIFAR-10, while **20%** improved generalization for MNIST.
- **Model depth** correlates positively with performance on simpler datasets, but for complex datasets like CIFAR-10, architectural efficiency (GoogLeNet) outperforms mere depth (VGG16).

---

## 🧠 Conclusion

| Dataset | Best Model | Accuracy | Key Observation |
|----------|-------------|-----------|----------------|
| **MNIST** | VGG16 (20%) | **99.42%** | Deep hierarchical features improve digit recognition. |
| **CIFAR-10** | GoogLeNet (10%) | **79.41%** | Multi-scale convolution paths enhance feature diversity. |

---




