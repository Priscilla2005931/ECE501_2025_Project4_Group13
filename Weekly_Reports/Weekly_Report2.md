## Report 2
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
- Objective
- Methodology
- Code
- Results
- Plan for Next Report
- References

## 1. Introduction

This week, we are implementing a generalized code for processing Chest X-ray images, thereby extracting features such as histogram analysis and  Gray Level Co-occurrence Matrix (GLCM) texture features. This is the foundation for the Content-Based Image Retrieval (CBIR) system. 



## 2. Objective
- Develop a Python basic code using libraries in Google Colab to process images from a dataset. 
- Extracts intensity histogram and GLCM features while capturing texture information. 
- Show extracted features as output. 
- Working with Google Colab initially for easy understanding and good compatibility. 



## 3. Methodology 

1. **Preprocessing of Images**
Preprocess the images initially to acquire clean and consistent input data.  

*Reading the images and Grayscale Conversion:*  
Read the chest X-ray images of data in grayscale format by OpenCV format in Google Colab because image texture and intensity features are highly interested in grayscale intensities in medical images.  

*Resizing:*
All images resized with fixed resolution.  
256×256 pixels (default input size).  
It is required as CBIR features like histograms and GLCM need same size in dataset.​

*Normalization:*
Pixel values are further normalized between 0 and 1 by division with 255.  
Normalization stabilizes numerical range for feature extraction from image functions and enhances algorithmic consistency. ​  
This pre-processing is done with the aim of removing variability like size and range of intensity, which can be a source of conflict in doing feature matching accuracy.

2. **Histogram Feature Extraction**
Pixel intensity across an image in terms of histogram features are used to characterize general brightness and contrast features:  

Histogram is computed using OpenCV's calcHist function, summing pixels by intensity bin (256 bins over intensity range 0-255).  
It is normalized such that values of features are scale-independent, scaling raw counts into probability distributions.  
Histograms are robust but low-level features that are commonly employed in CBIR for grayscale images.

3. **GLCM Texture Feature Extraction**
Texture is a significant feature of medical images, and one of the statistical measures for texture in terms of frequency of co-occurrence of pairs of pixel values at a specified spatial relationship is the Gray Level Co-occurrence Matrix (GLCM).  

The code uses skimage.feature.greycomatrix to compute the GLCM at a specified distance and angle (default distance=1 pixel, angle=0 degrees).  
Some statistical features derived from the GLCM using greycoprops are:  
- **Contrast:** It is a measure of the intensity difference between a pixel and the neighboring pixel.  
- **Energy:** Correlation that represents smoothness or uniformity of texture.  
- **Homogeneity:** Elements in the GLCM being close to the diagonal.  
- **Correlation:** It measures linear gray level dependency between pairs.  

These characteristics represent fine pattern texture information that is useful for abnormal or pattern detection in Chest X-rays.

4. **Feature Combination and Storage**
For every image:  

Histogram and GLCM features are integrated into a single feature vector.  
The vector is combined with the file path of the image to maintain image-feature mapping.  
A list of such dictionaries is converted into a Pandas DataFrame to store and retrieve easily later.  
The DataFrame is stored in a cache as a CSV to load up fast during similarity search. Modular design allows it to scale up to big data without changing the primary functions.

## 4. Code




## 5. Plan for Next Report

- Histogram and GLCM feature extraction.
- Store each image's feature values.
- Invoke a similarity measure function.
- Experiment retrieval on a small subset of the data set.

## 6. References

1. https://www.kaggle.com/datasets/nih-chest-xrays/data
2. https://www.researchgate.net/figure/Example-of-CBIR-using-the-combination-of-shape-histogram-and-moment-based-features_fig6_6487005
3. https://share.google/e8woXFD2PXG4vskwA
