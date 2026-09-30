# COMP9517 Group Project

## Project Overview

This project investigates image classification on a subset of the iNaturalist 2021 dataset using both traditional computer vision methods and deep learning approaches.

We compare four approaches:

- Traditional HOG + Linear SVM
- CNN
- ResNet18
- Vision Transformer (ViT)

The dataset contains 500 selected species with fixed training, validation, and testing splits.

---

## Repository Structure

Code/

│

├── Data Preparation/

│   └── Data Preparation.ipynb

│

├── Traditional Model/

│   ├── Traditional HOG-SVM Baseline.ipynb

│   └── SVM-para-tuning.ipynb

│

├── ResNet/

│   ├── CNN.ipynb

│   ├── ResNet18_Scratch.ipynb

│   └── ResNet18_ImageNet.ipynb

│

└── Vision Transformer/

    └── COMP9517_ViT_Project.ipynb

---

## Notebook Description

### 1. Data Preparation

This notebook downloads the iNaturalist dataset, randomly selects 500 species, creates fixed train/validation/test splits, extracts image labels, and prepares all datasets used throughout the project.

Output:

- selected_500_species_dataset
- train_labels.csv
- validation_labels.csv
- test_labels.csv

---

### 2. Traditional HOG-SVM Baseline

This notebook performs:

- HOG feature extraction
- feature saving
- baseline Linear SVM (SGDClassifier) training
- model saving

Output:

- HOG feature files (.npy)
- baseline model
- training information

---

### 3. SVM Hyperparameter Tuning

This notebook performs:

- alpha tuning
- penalty comparison
- averaging comparison
- best model selection
- model saving

The best model is later reused for robustness evaluation without retraining.

---

### 4. CNN

This notebook trains a simple CNN from scratch as the first deep learning baseline.

---

### 5. ResNet18 Scratch

This notebook trains a ResNet18 model from scratch.

---

### 6. ResNet18 ImageNet

This notebook fine-tunes an ImageNet pretrained ResNet18.

---

### 7. Vision Transformer

This notebook fine-tunes a pretrained Vision Transformer (ViT) model for the same classification task.

---

## Running Order

The notebooks should be executed in the following order:

1. Data Preparation
2. Traditional HOG-SVM Baseline
3. SVM Hyperparameter Tuning
4. CNN
5. ResNet18 Scratch
6. ResNet18 ImageNet
7. Vision Transformer

---

## Environment

The project was developed using:

- Python 3.10
- Google Colab
- PyTorch
- torchvision
- scikit-learn
- OpenCV
- scikit-image
- NumPy
- pandas
- matplotlib

Google Drive was used for storing datasets, trained models, and experiment outputs.

---

## Notes

- Most experiments require Google Drive to be mounted.
- Several training notebooks require multiple hours to finish.
- Saved models are reused whenever possible to avoid unnecessary retraining.
- Random seed = 46 unless otherwise stated.
