Deep Learning 2025–26

A comprehensive repository for Deep Learning coursework and projects for the academic year 2025–26.

Overview

This repository contains Jupyter notebooks and code examples for deep learning concepts, including:

Dataset handling and preprocessing

Working with image datasets (Tomato Disease Classification, MNIST)

Google Colab integration

Kaggle dataset integration

Repository Contents
Notebooks

DeepLearning.ipynb

Main deep learning notebook with dataset loading examples

Integration with Kaggle datasets

Google Drive mounting for data access

DeepLearning (1).ipynb

Extended version with additional examples

Tomato disease dataset processing

MNIST dataset handling

Getting Started
Prerequisites

Python 3.x

Jupyter Notebook or Google Colab

Required Libraries

pandas

kagglehub

numpy

matplotlib (for visualizations)

Dataset Access Methods

This repository demonstrates three methods for loading datasets in Google Colab.

1. Uploading Files Directly to Colab
from google.colab import files
uploaded = files.upload()

2. Mounting Google Drive
from google.colab import drive
drive.mount('/content/drive')

file_path = '/content/drive/MyDrive/Data sets/mnist_test.csv'
df = pd.read_csv(file_path)

3. Using Kaggle API Token
import kagglehub

path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)

Datasets Used
Tomato Disease Dataset

Source: Kaggle (noulam/tomato)

Purpose: Plant disease classification

Format: Augmented image dataset

MNIST Dataset

Source: Kaggle (oddrationale/mnist-in-csv)

Purpose: Handwritten digit recognition

Format: CSV format with pixel values

Usage
Running Notebooks

In Google Colab:

Upload the notebook to Google Colab

Run cells sequentially

Mount Google Drive or use Kaggle API as needed

Locally:

jupyter notebook DeepLearning.ipynb

Example: Loading MNIST Dataset
import pandas as pd
import kagglehub

path = kagglehub.dataset_download("oddrationale/mnist-in-csv")
df = pd.read_csv(f"{path}/mnist_test.csv")
df.head()

Example: Loading Tomato Disease Dataset
import kagglehub
import os

path = kagglehub.dataset_download("noulam/tomato")
print("Path to dataset files:", path)

print(os.listdir(path))
print(os.listdir(path + "/New Plant Diseases Dataset(Augmented)/valid"))

Setup Instructions
Kaggle Integration

Create a Kaggle account at kaggle.com

Go to Account Settings → API → Create New API Token

Upload the kaggle.json file to your Colab environment or configure it locally

Install kagglehub:

pip install kagglehub

Google Drive Integration

Mount Google Drive in Colab

Upload datasets to a designated folder

Update file paths in the notebooks accordingly

Course Topics Covered

Data loading and preprocessing

Working with image datasets

CSV data manipulation

Integration with cloud platforms (Colab, Kaggle)

Dataset augmentation techniques

Deep learning fundamentals

Contributing

This is a course repository. Contributions are welcome from students or instructors.

Fork the repository

Create a feature branch

Commit your changes

Push to the branch

Open a Pull Request

Contact

Repository Owner: @Aryanite

License

This project is for educational purposes as part of the Deep Learning course 2025–26.

Acknowledgments

Kaggle for providing open datasets

Google Colab for computational resources

Course instructors and peers
