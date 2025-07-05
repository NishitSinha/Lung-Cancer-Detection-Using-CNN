# 🧠 Lung Cancer Image Classification

This project focuses on detecting and classifying histopathological images of lung tissues into cancerous and non-cancerous classes using machine learning techniques, particularly Convolutional Neural Networks (CNNs).

---

## 📌 Project Overview

Histopathological image analysis plays a vital role in early detection of cancer. This project uses a publicly available dataset from Kaggle containing thousands of labeled high-resolution images to:

- Build a robust image classification pipeline.
- Apply deep learning techniques (CNN) to identify cancerous tissue.
- Evaluate the model's performance using various metrics.
- Demonstrate the potential of AI in digital pathology.

---

## 🎯 Project Objectives

- ✅ Download and preprocess histopathological image data.
- ✅ Explore image augmentation techniques to improve generalization.
- ✅ Train deep learning models for binary and multiclass classification.
- ✅ Compare training performance and validation results.
- ✅ Visualize results using confusion matrices and performance graphs.

---

## 📁 Dataset

- **Source:** Kaggle  
- **Link:** [Lung and Colon Cancer Histopathological Images](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images)  
- **Total Size:** ~1.95 GB  
- **Image Classes:**  
  - Colon Adenocarcinoma  
  - Colon Benign  
  - Lung Adenocarcinoma  
  - Lung Benign  
  - Lung Squamous Cell Carcinoma

---
## Tools & Technologies

- Python
- TensorFlow / Keras
- OpenCV
- Matplotlib, Seaborn
- Google Colab / Jupyter Notebook

---
## 📊 Expected Outcomes


- Achieve a high-accuracy model for lung/colon cancer detection.
- Visualize class-wise prediction performance.
- Explore how deep learning can assist medical diagnosis.

## 💻 How to Get the Dataset in Google Colab

To access and use the dataset in Google Colab, follow the steps below:

```python
# Step 1: Install the Kaggle library
!pip install -q kaggle

# Step 2: Upload your kaggle.json API token
from google.colab import files
files.upload()  # Select kaggle.json

# Step 3: Setup Kaggle API credentials
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Optional: Mount Google Drive (if you want to save the dataset)
from google.colab import drive
drive.mount('/content/drive')

# Step 4: (Optional) List some Kaggle datasets
!kaggle datasets list

# Step 5: Download the dataset
!kaggle datasets download 'andrewmvd/lung-and-colon-cancer-histopathological-images'

# Step 6: Extract the dataset
from zipfile import ZipFile

data_path = 'lung-and-colon-cancer-histopathological-images.zip'

with ZipFile(data_path, 'r') as zip_ref:
    zip_ref.extractall()
    print('The data set has been extracted.')

