# Lung and Colon Cancer Histopathological Image Analysis 🧬🖼️

This project uses the [Lung and Colon Cancer Histopathological Images dataset](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images) to train and evaluate machine learning models for cancer classification based on histopathological images.

## 📁 Dataset

- **Source:** Kaggle  
- **URL:** [https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images)  
- **Size:** ~1.95 GB  
- **Classes:**  
  - Colon Adenocarcinoma  
  - Colon Benign  
  - Lung Adenocarcinoma  
  - Lung Benign  
  - Lung Squamous Cell Carcinoma  

## 🧪 How to Download the Dataset in Google Colab

Follow these steps to download and extract the dataset in your Colab environment:

```python
# Step 1: Install Kaggle API
!pip install -q kaggle

# Step 2: Upload your Kaggle API key (kaggle.json)
from google.colab import files
files.upload()  # Upload kaggle.json file

# Step 3: Set up the Kaggle API credentials
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Optional: Mount Google Drive if needed
from google.colab import drive
drive.mount('/content/drive')

# Step 4: List available datasets (optional)
!kaggle datasets list

# Step 5: Download the dataset
!kaggle datasets download 'andrewmvd/lung-and-colon-cancer-histopathological-images'

# Step 6: Extract the zip file
from zipfile import ZipFile

data_path = 'lung-and-colon-cancer-histopathological-images.zip'

with ZipFile(data_path, 'r') as zip_ref:
    zip_ref.extractall()
    print('The data set has been extracted.')
