Deep Learning (2025–26)

A comprehensive repository for Deep Learning coursework and projects for the academic year 2025–26.

This repository provides well-structured Jupyter notebooks demonstrating core deep learning concepts, dataset handling techniques, and practical integrations with Google Colab, Google Drive, and Kaggle.

📌 Overview

The repository contains hands-on examples covering:

Dataset loading and preprocessing

Working with image and CSV-based datasets

Integration with Google Colab and cloud storage

Kaggle dataset access using API tokens

Foundational deep learning workflows

📁 Repository Structure
Notebooks
File	Description
DeepLearning.ipynb	Core notebook covering dataset loading, Kaggle integration, and Google Drive mounting
DeepLearning (1).ipynb	Extended notebook with additional examples including MNIST and Tomato Disease datasets
🚀 Getting Started
Prerequisites

Python 3.x

Jupyter Notebook or Google Colab

Required Libraries
pip install pandas numpy matplotlib kagglehub


Libraries used:

pandas

numpy

matplotlib

kagglehub

📊 Dataset Access Methods (Google Colab)

This repository demonstrates three standard approaches for loading datasets in Colab.

1️⃣ Upload Files Directly to Colab
from google.colab import files
uploaded = files.upload()

2️⃣ Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

import pandas as pd
file_path = '/content/drive/MyDrive/Data sets/mnist_test.csv'
df = pd.read_csv(file_path)

3️⃣ Use Kaggle API (Recommended)
import kagglehub

path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)

📚 Datasets Used
🍅 Tomato Disease Dataset

Source: Kaggle (noulam/tomato)

Purpose: Plant disease classification

Format: Augmented image dataset

🔢 MNIST Dataset

Source: Kaggle (oddrationale/mnist-in-csv)

Purpose: Handwritten digit recognition

Format: CSV (pixel values)

▶️ Usage
Running Notebooks in Google Colab

Upload the notebook to Google Colab

Run cells sequentially

Mount Google Drive or configure Kaggle API as required

Running Locally
jupyter notebook DeepLearning.ipynb

🧪 Examples
Load MNIST Dataset
import pandas as pd
import kagglehub

path = kagglehub.dataset_download("oddrationale/mnist-in-csv")
df = pd.read_csv(f"{path}/mnist_test.csv")
df.head()

Load Tomato Disease Dataset
import kagglehub
import os

path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)

print(os.listdir(path))
print(os.listdir(path + "/New Plant Diseases Dataset(Augmented)/valid"))

⚙️ Setup Instructions
Kaggle Integration

Create a Kaggle account at kaggle.com

Go to Account → API → Create New API Token

Upload kaggle.json to Colab or configure it locally

Install KaggleHub:

pip install kagglehub

Google Drive Integration

Mount Google Drive in Colab

Upload datasets to a designated folder

Update file paths inside notebooks accordingly

📖 Course Topics Covered

Data loading and preprocessing

Image dataset handling

CSV data manipulation

Cloud-based workflows (Colab, Kaggle)

Dataset augmentation concepts

Deep learning fundamentals

🤝 Contributing

This is a course repository. Contributions from students and instructors are welcome.

Fork the repository

Create a feature branch

Commit your changes

Push to your branch

Open a Pull Request

👤 Repository Owner

@Aryanite

📄 License

This project is intended strictly for educational purposes as part of the Deep Learning Course (2025–26).

🙏 Acknowledgments

Kaggle for open-access datasets

Google Colab for free computational resources

Course instructors and peers
