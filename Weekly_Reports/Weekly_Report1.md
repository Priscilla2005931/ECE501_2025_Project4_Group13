## Report 1
# CBIR for Chest X-rays using Histogram and GLCM Features


**Team Members:**  
|Student Name | Enroll Number |
|--------------|---------------| 
| R Priscilla | AU2340001 |
|Pratiksha Dongare | AU2340123|
| Shreya Dhumal | AU2340123|
| Krissa Gandhi | AU2340055|


## Table of Content
- Introduction
- Problem Definition
- Objective
- Methodology
- Tools and Software Required
- Plan for Next Report
- References

## 1. Introduction

Content-Based Image Retrieval (CBIR) is a technique through which images are retrieved from a vast image database based on their visual attributes like color, texture, or shape instead of text data.

In this project, we intend to present a CBIR system for **Chest X-ray images** based on **Histogram** and **Gray Level Co-occurrence Matrix (GLCM)** features. These features can be employed to detect intensity patterns and texture features from the medical images that can be utilized to search similar X-rays in diagnosis applications.


## 2. Problem Definition

There are many thousands of X-rays in medical image databases, and it is tiresome and laborious to search manually through similar cases.
The objective of this project is to create automatically retrieval of Chest X-ray images such as the query image based on visual features extracted.

## 3. Objective
To design and implement CBIR system for Chest X-rays using Histogram and GLCM features to retrieve images effectively and efficiently.

## 4. Methodology 

1. **Dataset Collection:**
- Download Chest X-ray images from either Kaggle or NIH Dataset.
- Rescale all images to a standard dimension (e.g., 256×256).

2. **Preprocessing:**
- If images are not in grey-scale, convert them.
- Normalize pixel values in the range 0 to 1.

3. **Feature Extraction (To be done in next report):**
- Extract Histogram features.
- Extract GLCM texture features (contrast, energy, homogeneity, correlation).

4. **Feature Storage:**
- Store features stored in CSV or a NumPy file for quicker loading.

5. **Image Retrieval:**
- Match query image features with stored features according to similarity measure (e.g., Euclidean distance).
- Show top similar images.

## 5. Tools and Software Required

| Tool | Purpose |
|------|----------|
| Python 3.x | Implementation |
| OpenCV | Image handling and histogram |
| scikit-image | GLCM feature extraction |
| NumPy, Pandas | Data handling |
| Matplotlib | Visualization |
| Jupyter Notebook / Google Colab | Development environment |


## 7. Plan for Next Report

- Histogram and GLCM feature extraction.
- Store each image's feature values.
- Invoke a similarity measure function.
- Experiment retrieval on a small subset of the data set.

## 8. References

1. https://www.kaggle.com/datasets/nih-chest-xrays/data
2. https://www.researchgate.net/figure/Example-of-CBIR-using-the-combination-of-shape-histogram-and-moment-based-features_fig6_6487005
3. https://share.google/e8woXFD2PXG4vskwA














