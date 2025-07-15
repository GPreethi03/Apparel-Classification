# 👕 Apparel Classification

An end-to-end multi-class image classification pipeline for apparel recognition, built using Big Data tools and deep learning. The model leverages Apache Spark, Hadoop HDFS, and transfer learning (ResNet50) to efficiently process and classify fashion product images from Kaggle.

---

## 📌 Project Overview

This project focuses on recognizing and classifying various types of apparel using image data. We use a combination of big data technologies and deep learning to:

- Process large volumes of image data  
- Preprocess and store it using HDFS and Spark  
- Train a robust image classifier using ResNet50  

---

## ⚙️ System Requirements

- Google Colab Pro+ (for GPU/TPU access)  
- Hadoop HDFS (for distributed file storage)  
- Internet access (to download datasets using Kaggle API)  

---

## 🛠️ Installation

### 1. Hadoop Setup

Install and configure Hadoop for distributed storage and processing.  
Start HDFS services using:  
`start-dfs.sh`

### 2. Install Required Libraries

Use the following pip command in Colab or your environment:  
`pip install numpy pandas pyspark tensorflow keras opencv-python-headless pillow matplotlib seaborn tqdm scikit-learn kaggle`

### 3. Download Dataset via Kaggle API

Ensure your Kaggle API key is configured in `~/.kaggle/kaggle.json`.  
Then download and extract:

- `enashed/fashion-dataset`  
- `paramaggarwal/fashion-product-images-dataset`  

Unzip using your environment’s unzip utility.

---

## 🚀 Usage Guide

### 🔸 Data Collection & Ingestion

- Set up Hadoop cluster and configure HDFS  
- Ingest image data using:  
  `hdfs dfs -copyFromLocal <local_src> <hdfs_dest>`  
- Apply appropriate file formats, compression, and access control  

### 🔸 Data Preprocessing

- Convert image data into a Spark DataFrame  
- Resize images while maintaining aspect ratio  
- Organize data into label-based folders  

### 🔸 Model Training

- Train a ResNet50-based model using TensorFlow/Keras  
- Perform train/validation/test split  
- Use transfer learning and fine-tuning  

### 🔸 Evaluation & Results

- Generate predictions and evaluate performance  
- Display actual vs. predicted labels  
- Plot training metrics and confusion matrix  

---

## ▶️ Running the Project

- Open the notebook `Apparel_Classification_Transfer_Learning.ipynb` in Google Colab  
- Run all cells in order to execute data ingestion, preprocessing, model training, and evaluation  

