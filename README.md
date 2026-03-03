# Automated Corneal Endothelium Analysis Using U-Net

## Overview
In this project, I developed an end-to-end AI pipeline for automated analysis of corneal endothelial images using deep learning and computer vision. This project implements a Python-based deep learning and machine learning pipeline for automated analysis of corneal endothelium using specular microscopy images.
Images are in Images and Labels folder



# Problem
Manual corneal endothelium analysis via specular microscopy is time-consuming and expertise-dependent.
 The goal was to:
- Automatically segment endothelial cells
- Extract clinically relevant morphometric features
- Classify images as Normal or Abnormal

 # Project Highlights
1. Image Preprocessing
- Converted raw microscopy images into normalized input tensors
- Transformed point annotations into pixel-wise masks using Voronoi-based region construction
- Prepared structured data for supervised learning

<img width="1222" height="349" alt="image" src="https://github.com/user-attachments/assets/3541285c-d45d-4238-a160-49dda7c237cf" />

2. U-Net Based Segmentation
- Implemented a full-image U-Net architecture for pixel-wise classification
- Segmented images into Background, Cell Interior, and Boundary
- Applied sliding window inference with overlapping patches
- Used watershed and morphological processing to isolate individual cells

  <img width="1216" height="315" alt="image" src="https://github.com/user-attachments/assets/7b6a69ee-10d8-40ba-9a13-feadc5bdd195" />


3.  Morphometric Feature Extraction
- From segmented masks, the system computes clinically relevant metrics:
- Endothelial Cell Density (ECD)
- Coefficient of Variation (CV) – Polymegathism
- Hexagonality % – Pleomorphism
These are the same features ophthalmologists rely on for diagnosis.

4. Clinical Classification
Extracted features are used for automated prediction of Normal vs Abnormal corneal endothelium using random forest.

Example output :
<img width="373" height="196" alt="image" src="https://github.com/user-attachments/assets/1ba06436-9b62-48e0-a984-d38cb317b5fc" />

# Model Performance & Next Steps
The system achieves an estimated 88–90% cell detection rate, showing strong performance for automated biomedical segmentation.

Next phase: strengthen validation using precision, recall, F1-score, and structured error analysis to further improve robustness and move toward clinically reliable AI-assisted corneal assessment.

# Tech Stack
Python • TensorFlow/Keras • OpenCV • Scikit-image • NumPy • Pandas • Classical ML models

# Model Performance & Next Steps
The system achieves an estimated 88–90% cell detection rate, showing strong performance for automated biomedical segmentation.

Next phase: 
-strengthen validation using precision, recall, F1-score, and 
- structured error analysis to further improve robustness and move toward clinically reliable AI-assisted corneal assessment.
- Smartphone-based deployment
- Real-time inference
- Expanded clinical dataset validation


---

## Author

Indhira Vadivel
