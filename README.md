# 🛍️ AI-Powered Product Review Sentiment Analysis

## 📌 Project Overview

This project analyzes customer product reviews and classifies them into three sentiment categories:

* 😊 Positive
* 😐 Neutral
* 😞 Negative

The project uses a **pre-trained Sentence Transformer (`all-MiniLM-L6-v2`)** to convert product reviews into meaningful sentence embeddings. These embeddings are then used as input features for traditional machine learning models.

## 🎯 Objective

The main objective is to build a sentiment classification system that can automatically identify customer opinions from product reviews and support data-driven business decisions.

## 📊 Dataset

The dataset contains **1,007 rows and 3 columns**:

* **Product ID** – Unique identifier for products
* **Product Review** – Customer's written review
* **Sentiment** – Sentiment category of the review

### Data Cleaning

* Checked for missing values
* No missing values were found
* Identified **2 duplicate records**
* Removed duplicate records
* Reset the DataFrame index

## 🔍 Exploratory Data Analysis

The sentiment distribution was analyzed to understand the dataset.

* Positive reviews form the majority of the dataset.
* Neutral and negative reviews are comparatively fewer.
* The dataset therefore has an **imbalanced sentiment distribution**.

## 🤖 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Sentence Transformers

## 🧠 Methodology

The project follows these steps:

1. Load the product review dataset
2. Perform data inspection and cleaning
3. Analyze sentiment distribution
4. Load the pre-trained `all-MiniLM-L6-v2` Sentence Transformer
5. Convert product reviews into sentence embeddings
6. Split the dataset into **80% training and 20% testing**
7. Train machine learning classifiers
8. Evaluate models using Accuracy and F1 Score
9. Compare model performance
10. Select the best-performing model

## 🔄 Model Architecture

**Product Review → Sentence Transformer → Sentence Embedding → Machine Learning Classifier → Sentiment Prediction**

## 📈 Models Used

### 1. Random Forest + Transformer

The Random Forest classifier was trained using the Transformer-generated embeddings.

* Training Accuracy: **100%**
* Training F1 Score: **1.00**
* Test Accuracy: **86.57%**
* Test F1 Score: **81.80%**

### 2. Gradient Boosting + Transformer

Gradient Boosting was also trained using the generated sentence embeddings.

* Training Accuracy: **99.88%**
* Training F1 Score: **99.87%**
* Test Accuracy: **84.08%**
* Test F1 Score: **80.33%**

## 🏆 Final Model

**Random Forest + Transformer embeddings** was selected as the final model because it achieved better testing performance than Gradient Boosting.

| Model                           | Test Accuracy | Test F1 Score |
| ------------------------------- | ------------: | ------------: |
| Random Forest + Transformer     |    **86.57%** |    **81.80%** |
| Gradient Boosting + Transformer |        84.08% |        80.33% |

## 📌 Key Findings

* Transformer embeddings provide meaningful numerical representations of customer reviews.
* Random Forest performed better than Gradient Boosting on the test dataset.
* Random Forest achieved approximately **86.6% test accuracy**.
* The difference between training and testing performance indicates some generalization gap.
* The approach demonstrates that Transformer embeddings can be effectively combined with traditional machine learning algorithms for sentiment classification.

## 🚀 Future Improvements

The model can be further improved by exploring:

* XGBoost
* Support Vector Machines (SVM)
* Sequential Neural Networks
* Fine-tuned Transformer models
* Better handling of class imbalance
* Hyperparameter tuning
* Larger and more diverse datasets



## 🏁 Conclusion

This project demonstrates how **Transformer-based sentence embeddings** can be combined with traditional machine learning algorithms to perform product review sentiment analysis. Among the evaluated models, **Random Forest + Transformer embeddings** provided the best test performance with **86.57% accuracy and 81.80% F1 score**.
