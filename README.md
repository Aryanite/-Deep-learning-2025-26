# Deep Learning 2025-26 🧠

A comprehensive repository for Deep Learning coursework and projects for the academic year 2025-26.

## 📋 Overview

This repository contains Jupyter notebooks and code examples for deep learning concepts, including: 
- Dataset handling and preprocessing
- Working with image datasets (Tomato Disease Classification, MNIST)
- Google Colab integration
- Kaggle dataset integration

## 📁 Repository Contents

### Notebooks

1. **DeepLearning. ipynb**
   - Main deep learning notebook with dataset loading examples
   - Integration with Kaggle datasets
   - Google Drive mounting for data access

2. **DeepLearning (1).ipynb**
   - Extended version with additional examples
   - Tomato disease dataset processing
   - MNIST dataset handling

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- Required libraries: 
  ```python
  - pandas
  - kagglehub
  - numpy
  - matplotlib (for visualizations)
  ```

### Dataset Access Methods

This repository demonstrates three methods for loading datasets in Google Colab:

#### 1. **Uploading Files Directly to Colab**
```python
# Upload files directly to Colab session
from google.colab import files
uploaded = files.upload()
```

#### 2. **Mounting Google Drive**
```python
from google.colab import drive
drive.mount('/content/drive')

# Access files from your Google Drive
file_path = '/content/drive/MyDrive/Data sets/mnist_test.csv'
df = pd.read_csv(file_path)
```

#### 3. **Using Kaggle API Token**
```python
import kagglehub

# Download datasets directly from Kaggle
path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)
```

## 📊 Datasets Used

### Tomato Disease Dataset
- **Source**: Kaggle (noulam/tomato)
- **Purpose**: Plant disease classification
- **Format**:  Augmented image dataset

### MNIST Dataset
- **Source**: Kaggle (oddrationale/mnist-in-csv)
- **Purpose**: Handwritten digit recognition
- **Format**: CSV format with pixel values

## 💻 Usage

### Running Notebooks

1. **In Google Colab:**
   - Upload the notebook to Google Colab
   - Run cells sequentially
   - Mount Google Drive or use Kaggle API as needed

2. **Locally:**
   ```bash
   jupyter notebook DeepLearning.ipynb
   ```

### Example:  Loading MNIST Dataset

```python
import pandas as pd
import kagglehub

# Using Kaggle API
path = kagglehub.dataset_download("oddrationale/mnist-in-csv")
df = pd.read_csv(f"{path}/mnist_test.csv")
df.head()
```

### Example: Loading Tomato Disease Dataset

```python
import kagglehub
import os

# Download dataset
path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)

# Explore dataset structure
print(os.listdir(path))
print(os.listdir(path + "/New Plant Diseases Dataset(Augmented)/valid"))
```

## 🔧 Setup Instructions

### For Kaggle Integration:

1. Create a Kaggle account at [kaggle.com](https://www.kaggle.com)
2. Go to Account Settings → API → Create New API Token
3. Upload the `kaggle.json` file to your Colab environment or configure it locally
4. Install kagglehub: 
   ```python
   !pip install kagglehub
   ```

### For Google Drive: 

1. Mount your Google Drive in Colab
2. Upload datasets to a designated folder
3. Update file paths in the notebooks accordingly

## 📝 Course Topics Covered

- Data loading and preprocessing
- Working with image datasets
- CSV data manipulation
- Integration with cloud platforms (Colab, Kaggle)
- Dataset augmentation techniques
- Deep learning fundamentals

## 🤝 Contributing

This is a course repository.  If you're a fellow student or instructor: 
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📧 Contact

**Repository Owner**: [@Aryanite](https://github.com/Aryanite)

## 📄 License

This project is for educational purposes as part of the Deep Learning course 2025-26.

## 🙏 Acknowledgments

- Kaggle for providing open datasets
- Google Colab for computational resources
- Course instructors and peers

---

**Last Updated**: January 2026

⭐ Star this repository if you find it helpful! 
