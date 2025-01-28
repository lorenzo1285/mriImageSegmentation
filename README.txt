# MRI Image Segmentation using K-Means

This repository contains an implementation of MRI brain image segmentation using K-Means clustering. The model processes and segments multiple axial MRI slices, identifying different tissue types using unsupervised learning techniques.

## Project Overview

The goal of this project is to develop a **segmentation model** for 10 consecutive axial MRI slices of a human brain. The segmentation task is performed using **K-Means clustering**, with various preprocessing steps to improve accuracy.

### **Labels Used in Segmentation:**
- **Label 0**: Air
- **Label 1**: Skin/Scalp
- **Label 2**: Skull
- **Label 3**: Cerebrospinal Fluid (CSF)
- **Label 4**: Gray Matter
- **Label 5**: White Matter

## Methods

### **1. Data Preprocessing**
To enhance segmentation quality, several preprocessing techniques are applied:
- **Outlier removal** using Min-Max Scaling, Standard Scaling, and Quantile Transformation.
- **Gaussian Smoothing** to reduce noise while preserving important anatomical structures.
- **Edge Detection** using different techniques:
  - Sobel
  - Prewitt
  - Roberts
  - Laplace
  - Canny

### **2. K-Means Clustering for Segmentation**
K-Means clustering is chosen due to its **computational efficiency** and the lack of labeled data for supervised learning models.

- **Pixel grouping** based on intensity and edge features.
- **Iterative clustering** with centroid updates to minimize variance.
- **Final segmentation visualization**, overlapping segmented images with original MRI scans.

### **3. Evaluation Metrics**
- **F1-Score**: Measures the balance between precision and recall for each segmentation method.
- **Gaussian Optimization**: Used to fine-tune hyperparameters and preprocessing settings to maximize segmentation performance.

## Results

| Metric  | Value  |
|---------|--------|
| **F1 Score**  | **0.7902** |
| **K-Means Initiator**  | Random |
| **Best Preprocessing Transformation**  | Novel |
| **Gaussian Smoothing Sigma**  | 0.1477 |
| **Scaler Used**  | Quantile |

### **3D Segmentation Proposal**
A 3D segmentation approach is suggested to improve slice continuity and enhance segmentation performance. Possible future implementations include:
- **3D K-Means Clustering**
- **3D Convolutional Neural Networks (CNNs)**
- **Volumetric MRI Processing Techniques**

## Installation & Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/MRI_Kmeans_Segmentation.git
