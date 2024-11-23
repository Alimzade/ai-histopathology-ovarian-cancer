# AI for Histopathology: Ovarian Cancer Subtype Classification

## Abstract

This repository contains code for ovarian cancer subtype classification using Whole Slide Images (WSI) and Tissue Microarrays (TMA). We explore multiple approaches, including a Multiple Instance Learning (MIL) classifier for WSI, encoder and tile-based majority voting for TMA. The MIL classifier demonstrates strong performance, while TMA methods show potential despite generalization challenges. This study emphasizes AI's role in advancing diagnostics and calls for larger datasets and innovative architectures to improve precision and patient outcomes.


## Contributors

- **Anar Alimzade** - Implementation of WSI MIL classifier and TMA tile-based majority voting.
- **Ali Alper Sakar** - Development of TMA Encoder-based classification approach


## Details

This study focuses on classifying subtypes of ovarian cancer using Whole Slide Images (WSI) and Tissue Microarrays (TMA) data from the [UBC-OCEAN Kaggle competition](https://www.kaggle.com/competitions/UBC-OCEAN). The task is to classify ovarian cancer images into the following subtypes:

- **Clear Cell Carcinoma (CC)**
- **Endometrioid Carcinoma (EC)**
- **High-grade Serous Carcinoma (HGSC)**
- **Low-grade Serous Carcinoma (LGSC)**
- **Mucinous Carcinoma (MC)**
- **Other** (Note: This class is absent in the training set but present in the test set.)

The dataset consists of images from different hospitals, with the test set containing images from institutions not represented in the training set, adding a challenge of domain shift.

<img width="1520" alt="OCEAN-Optional-Figure" src="https://github.com/user-attachments/assets/95c01abd-6f40-4f13-bdea-1cddcdfb7199">

## Data Description

- **WSI (Whole Slide Images):** Large images (up to 100,000 x 50,000 pixels) at 20x magnification. The average file size is 1-2 GB.
- **TMA (Tissue Microarrays):** Smaller images (~4,000 x 4,000 pixels) at 40x magnification, but there are relatively fewer TMA samples in the dataset.

## Results

**Best Approach:** 
The MIL classifier approach, treating WSI images as bags of instances, yielded the best performance with 80% accuracy.
