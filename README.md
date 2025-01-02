# Multiclass-classification-of-Otitis-Media-
# Deep Learning-based Detection of Otitis Media Severity Stages

This repository contains the code for the multiclass classification model. This study explores the application of deep learning techniques to classify stages of Otitis Media (OM) using otoscopic images.

## Overview

Otitis Media (OM) is a middle-ear disorder with significant implications for children and adults. This research employs **EfficientNet B3** and **Inception V3** deep learning models to classify OM stages, providing an automated diagnostic aid for medical professionals.

Key Contributions:
- Classification of OM into **Acute Otitis Media (AOM-mild)**, **Acute Severe Otitis Media (ASOM-moderate)**, **Chronic Suppurative Otitis Media (CSOM-severe)**, and **Normal Tympanic Membrane (TM)**.
- Comparative analysis of model performance with respect to precision, recall, specificity, and F1-score.
- A curated dataset with 388 otoscopic images labeled under medical supervision.

---

## Dataset

The dataset consists of high-resolution otoscopic images categorized into:
1. **Normal Tympanic Membrane**  
2. **Acute Otitis Media (AOM)**  
3. **Acute Severe Otitis Media (ASOM)**  
4. **Chronic Suppurative Otitis Media (CSOM)**  

### Dataset Composition
- **Training Set:** 288 images
- **Testing Set:** 100 images
- Includes varied age groups and lighting conditions to ensure generalizability.

The dataset was gathered and annotated by medical experts at AIIMS Raipur.

---

## Methodology

### Preprocessing
- Images resized to uniform resolution and converted to grayscale.
- Stratified splitting into training and testing datasets to maintain class balance.

### Models
#### 1. **EfficientNet B3**
- Employs inverted residual blocks and global average pooling.
- Optimized for spatial information and feature recalibration.

#### 2. **Inception V3**
- Uses multi-scale convolution layers for enhanced feature extraction.
- Incorporates max-pooling and average-pooling for better abstraction.

### Training
- Models trained using the Adam optimizer and categorical cross-entropy loss.
- Last 50 layers made trainable; earlier layers frozen for fine-tuning.

---

## Results

### Model Performance
| Model           | Accuracy | Precision | Recall | F1-Score | Specificity |
|------------------|----------|-----------|--------|----------|-------------|
| EfficientNet B3  | 78.18%   | 81.53%    | 78.18% | 76.85%   | 70.44%      |
| Inception V3     | 78.18%   | 81.00%    | 78.00% | 79.00%   | 77.98%      |

- **EfficientNet B3** excelled in detecting ASOM but struggled with CSOM.
- **Inception V3** offered better recall for CSOM and overall specificity.

---

## Conclusion

Both models demonstrate potential in automating OM classification. This work provides a foundation for integrating AI into clinical diagnostics, offering reliable support for otolaryngologists.
