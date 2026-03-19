# CNN Pneumonia Detector

This project develops and evaluates Convolutional Neural Network (CNN) models to detect pneumonia from chest X-ray images. The goal is to explore deep learning techniques for medical image classification and assess model performance using appropriate evaluation metrics.

## Problem Overview

Pneumonia is a serious lung infection that can be life-threatening if not detected early. Diagnosis typically requires expert analysis of chest X-rays, which can be time-consuming.

This project builds deep learning models to assist in detecting pneumonia from X-ray images, demonstrating how machine learning can support medical decision-making.

## Dataset

* Source: Kaggle – Chest X-Ray Images (Pneumonia)
* Total Images: 5,863
* Classes:

  * NORMAL
  * PNEUMONIA

The dataset is already split into:

* Training set
* Validation set
* Test set

Note: The validation set is very small (16 images), which may lead to unstable validation performance.

## Approach

The workflow is implemented in a single notebook and includes:

1. Data Preparation
* Image loading and resizing (128x128)
* Normalization (pixel scaling)
2. Exploratory Data Analysis (EDA)
* Visualization of sample images
* Inspection of image dimensions and values
3. Model Development
Three CNN models were built and compared:
* Model 1 (Baseline)

  * Single convolutional layer
  * Simple architecture for benchmarking
* Model 2

  * Additional convolutional layer
  * Modified filter sizes
* Model 3 (Final Model)

  * Two convolutional layers
  * Dropout layers (25%) to reduce overfitting
4. Evaluation
Models were evaluated using:
* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

## Results

The final model achieved:

* Test Accuracy: \~78.7%
* Pneumonia Recall: 0.99
* Pneumonia Precision: 0.75

Key insight:

* The model performs very well at detecting pneumonia cases (high recall)
* Performance on normal cases is weaker, indicating class imbalance or model bias

## Repository Structure

```text

CNN-Pneumonia-Detector/

│

├── data/

│   └── README.md

├── notebooks/

│   └── Pneumonia Detection.ipynb

├── src/

│   └── utils.py

├── requirements.txt

└── .gitignore

```

## How to Run

1. Clone the repository:
git clone https://github.com/Jorge-Barajas-Github/CNN-Pneumonia-Detector.git
2. Install dependencies:
pip install -r requirements.txt
3. Download dataset (see data/README.md) and place it in:
data/raw/chest\_xray/
4. Run the notebook:
jupyter notebook

## Limitations

* Very small validation set (16 images)
* No data augmentation applied
* Models are relatively simple CNN architectures

## Future Improvements

* Increase validation set size or use cross-validation
* Apply data augmentation
* Perform more extensive hyperparameter tuning

## References

* Kaggle Dataset: Chest X-Ray Images (Pneumonia)
* TensorFlow Documentation
* Scikit-learn Documentation

