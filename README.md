# Automated Corneal Endothelium Analysis Using U-Net

## Overview

This project implements a Python-based deep learning and machine learning pipeline for automated analysis of corneal endothelium using specular microscopy images.

The system performs:
- Endothelial cell segmentation using U-Net
- Morphometric feature extraction
- Normal vs abnormal classification

The goal is to provide an objective, reproducible, and quantitative approach to endothelial assessment.

---

## Pipeline Architecture

### 1. Image Acquisition
- Input: Specular microscopy images
- Preprocessing:
  - Grayscale conversion
  - Normalization
  - Resizing

### 2. U-Net Segmentation
- Pixel-wise segmentation of endothelial cells
- Generates binary or labeled masks
- Enables detection of individual cells

### 3. Post-Processing
- Connected component labeling
- Morphological cleanup
- Full mask reconstruction (if patch-based inference)

### 4. Feature Extraction

From the labeled segmentation mask:

- **Endothelial Cell Density (ECD)**
- **Coefficient of Variation (CV)** (polymegathism)
- **Hexagonality (H)** (pleomorphism)

### 5. Machine Learning Classification
- Input features: Density, CV, Hexagonality
- Output: Normal / Abnormal classification
- Models: Logistic Regression / Random Forest / SVM

---

## Technologies Used

- Python
- TensorFlow / Keras
- U-Net architecture
- OpenCV
- scikit-image
- scikit-learn
- NumPy

---

## Clinical Significance

The system computes standard ophthalmic biomarkers used in clinical practice:

- Cell Density (cells/mm²)
- CV (cell size variability)
- Hexagonality (% hexagonal cells)

These parameters help assess corneal endothelial health and detect pathological changes.

---

## Future Work

- Smartphone-based deployment
- Real-time inference
- Expanded clinical dataset validation
- End-to-end deep learning classification

---

## Author

Your Name
