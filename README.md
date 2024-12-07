# ENGG680-Fall2024-CNNTraficSignRecognitionProject
Collaborative Project for ENGG680 Fall 2024 
Real-Time Traffic Sign Recognition Using Convolutional Neural Networks to Address Emerging Traffic Violations.

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

## Accessing the Dataset from Google Drive

### If you don’t have the dataset locally:
1. Ensure you have the necessary Python packages installed for downloading from Google Drive:
   ```bash
   !pip install gdown
   ```

2. Download the dataset from the shared Google Drive link using `gdown`. Here is the command to download the dataset:

   ```python
   import gdown

   # Google Drive folder URL
   gdrive_url = 'https://drive.google.com/drive/folders/1WvWtjCpbGw3fflmX5QV_4UYIvEXDLDIt?usp=sharing'
   
   # To download from Google Drive, use the gdown link with the folder id.
   # Replace '/uc?id=' with the folder id and download using this URL.
   gdown.download_folder(gdrive_url, quiet=False)
   ```

3. Unzip the dataset if necessary (depending on the file format). If it's a zipped file, use the following command:
   ```bash
   !unzip dataset.zip -d ./path_to_extract/
   ```

4. Verify that the dataset is available in the extracted folder. The structure should resemble:
   ```
   ./path_to_extract/
   ├── Metadata
   ├── Test
   └── Train
   ```

5. Once the dataset is unzipped and in the correct directory, you can proceed with running the code that references this path. Update the code paths as needed to point to the dataset location, for example:

   ```python
   # Example path to the dataset for your code
   train_data_path = './path_to_extract/Train/'
   test_data_path = './path_to_extract/Test/'
   ```

### Note:
Make sure the file paths in the code correspond to where the dataset has been extracted!

---
