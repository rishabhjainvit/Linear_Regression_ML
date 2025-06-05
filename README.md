# Amazon Clothes Price Prediction Using Linear Regression

## Project Overview

This repository demonstrates how to build a simple linear regression model to predict Amazon clothing prices based on product features. We use a curated subset of the Amazon “Clothing, Shoes & Jewelry” dataset, perform basic preprocessing, and train a scikit-learn linear regression model. The goal is to illustrate end-to-end steps, from data cleaning to model evaluation.

---

## Table of Contents

- [Dataset](#dataset)  
- [Features](#features)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
- [File Structure](#file-structure)  
- [Data Preprocessing](#data-preprocessing)  
- [Model Training](#model-training)  
- [Evaluation](#evaluation)  
- [Results](#results)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Dataset

We use a subset of the Amazon “Clothing, Shoes & Jewelry” dataset available on [Kaggle](https://www.kaggle.com/PromptCloudHQ/amazon-product-reviews). The dataset has been pre-filtered to include only clothing items with numeric price labels. The cleaned CSV (`amazon_clothes_cleaned.csv`) is included in the `data/` folder.

- **Original Source**: PromptCloud’s Amazon Product Reviews (Clothing)  
- **Filtered Columns**:  
  - `product_id`  
  - `title`  
  - `brand`  
  - `category`  
  - `price` (target variable)  
  - `rating`  
  - `reviews_count`  
  - `description_length`  

> **Note:** If you wish to re-download or expand the dataset, place your raw CSV in `data/raw/` and adjust paths in the preprocessing notebook accordingly.

---

## Features

For this demonstration, we engineer a handful of features to feed into our linear regression model:

1. **Brand (Categorical)**  
2. **Category (Categorical)**  
3. **Rating (Numerical)**  
4. **Number of Reviews (Numerical)**
5. **Description Length** (Character count of product description—Numerical)

Categorical features (`brand` and `category`) are one-hot encoded before training.

---

## Prerequisites

- Python 3.8 or higher  
- Recommended virtual environment tool (e.g., `venv` or `conda`)  

### Python Libraries

- `pandas`  
- `numpy`  
- `scikit-learn`  
- `matplotlib`  
- `seaborn` (optional, for extra visualizations)  
- `jupyter` (to run notebooks)

All dependencies are listed in `requirements.txt`.

---

## Installation

1. **Clone this repository**  
   ```bash
   git clone https://github.com/<your-username>/amazon-clothes-linear-regression.git
   cd amazon-clothes-linear-regression
