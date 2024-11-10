# ENGG680-Fall2024-CNNTraficSignRecognitionProject
Collaborative Project for ENGG680 Fall 2024 
Real-Time Traffic Sign Recognition Using Convolutional Neural Networks to Address Emerging Traffic Violations

---

## Dataset Acess
https://drive.google.com/drive/folders/1WvWtjCpbGw3fflmX5QV_4UYIvEXDLDIt?usp=sharing

This repository contains a structured version of the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset. The dataset is divided into three main folders: **Metadata**, **Test**, and **Train**, which are organized as follows:

## Folder Structure:

### 1. **Metadata**
   - Contains the original README files from GTSRB.
   - Includes all CSV files related to the dataset (both training and testing data).
   - Provides key information such as image dimensions, location of signs within images (ROI), and traffic sign class IDs.

### 2. **Train**
   - Contains the training images for the dataset.
   - Organized into 43 directories (00000 - 00042), one for each traffic sign class.
   - Each directory includes images and has a corresponding CSV file with annotations (e.g., `GT-00000.csv`) found in Metadata.
   - Image filenames follow the format `XXXXX_YYYYY.ppm`, where:
     - `XXXXX` represents the track number (images from the same physical traffic sign).
     - `YYYYY` is the running number within the track.

### 3. **Test**
   - Contains the test images (12,630 images in total).
   - The images are numbered sequentially from `00000.ppm` to `12629.ppm` without any track or class information.
   - A single annotation file (`GT-final_test.test.csv`) provides the image metadata, including the sign's class and ROI, found in Metadata.

## Annotations Format:
- All annotations are stored in CSV format, with the following fields:
  - **Filename**: Name of the image file.
  - **Width, Height**: Image dimensions.
  - **Roi.x1, Roi.y1, Roi.x2, Roi.y2**: Coordinates of the traffic sign within the image.
  - **ClassId**: The class of the traffic sign (used for classification).

## Accessing the Dataset:
- **Google Drive**: Due to the large size of the dataset, the entire dataset is hosted on Google Drive. Use the provided link to access and download the dataset.

---
