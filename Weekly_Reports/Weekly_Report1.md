## Report 1
# CBIR for Chest X-rays using Histogram and GLCM Features


**Team Members:**  
|Student Name | Enroll Number |
|--------------|---------------| 
| R Priscilla | AU2340001 |
|Pratiksha Dongare | AU2340123|
| Shreya Dhumal | AU2340123|


## Table of Content
- Introduction
- Problem Definition
- Objective
- Methodology
- Tools and Software Required
- Litreature Review
- References

## 1. Introduction

Content-Based Image Retrieval (CBIR) is a method used to retrieve images from a large database based on their visual features such as color, texture, or shape rather than text-based labels.  

In this project, we aim to design a CBIR system for **Chest X-ray images** using **Histogram** and **Gray Level Co-occurrence Matrix (GLCM)** features. These features help identify intensity patterns and texture properties in medical images, which are useful for finding similar X-rays in diagnostic systems.


## 2. Problem Definition

Medical image databases contain thousands of X-rays, and finding similar cases manually is difficult and time-consuming.  
This project focuses on developing a system that automatically retrieves similar Chest X-ray images based on extracted visual features.

## 3. Objective
To design and implement a CBIR system for Chest X-rays using Histogram and GLCM features for efficient and accurate image retrieval.

## 4. Methodology 

1. **Dataset Collection:**  
   - Collect Chest X-ray images from online sources such as Kaggle or NIH Dataset.  
   - Resize all images to a fixed resolution (e.g., 256×256).

2. **Preprocessing:**  
   - Convert images to grayscale (if not already).  
   - Normalize pixel values between 0 and 1.

3. **Feature Extraction (To be done in next report):**  
   - Extract Histogram features.  
   - Extract GLCM texture features (contrast, energy, homogeneity, correlation).

4. **Feature Storage:**  
   - Save extracted features in a CSV or NumPy file for faster retrieval.

5. **Image Retrieval:**  
   - Compare query image features with stored features using a distance measure (e.g., Euclidean distance).  
   - Display top matching images.


## 5. Tools and Software Required

| Tool | Purpose |
|------|----------|
| Python 3.x | Implementation |
| OpenCV | Image handling and histogram |
| scikit-image | GLCM feature extraction |
| NumPy, Pandas | Data handling |
| Matplotlib | Visualization |
| Jupyter Notebook / Google Colab | Development environment |

## 6. Litreature Review
| Year | Title | Method Used | Summary |
|------|--------|--------------|----------|
| 2020 | CBIR using Histogram | Histogram Features | Describes how intensity distribution can be used for image similarity. |
| 2021 | CBIR using Texture Features | GLCM Features | Highlights texture-based feature extraction for grayscale medical images. |
| 2022 | Medical Image Retrieval | Hybrid (Histogram + GLCM) | Combines multiple features for improved accuracy. |
| 2023 | CBIR for X-ray Images | GLCM and Statistical Features | Shows the effectiveness of texture analysis for disease identification. |

## 7. Plan for Next Report

- Implement feature extraction using Histogram and GLCM.  
- Store feature values for each image.  
- Develop a similarity measurement function.  
- Test retrieval for small dataset samples.

## 8. References

1. Haralick, R. M., et al. (1973). *Textural features for image classification.* IEEE Transactions on Systems, Man, and Cybernetics.  
2. Gonzalez, R. C., & Woods, R. E. (2018). *Digital Image Processing.*  
3. Kaggle Chest X-ray Dataset.  
4. Research papers on CBIR using Histogram and GLCM features.




