
# Bengali Spam Email Detection Using Machine Learning and Deep Learning


## Project Overview

Bengali Spam Email Detection is an advanced system developed to classify emails written in Bengali into Spam, Ham (non-spam), and Promotional categories using a combination of machine learning and deep learning techniques. This project addresses the gap in accurate spam detection tools for Bengali language emails—a major concern given the large Bengali-speaking population worldwide.

The system leverages classical ML classifiers, ensemble learning, and a state-of-the-art Bidirectional Long Short Term Memory (Bi-LSTM) deep learning model. The deep learning model achieved a remarkable test accuracy of **94.46%**, outperforming traditional ML models. This solution aims to significantly enhance email security, privacy, and user experience for Bengali users.

***

## Table of Contents

- [Background](#background)
- [Motivation](#motivation)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Methodology](#methodology)
    - [Data Collection \& Annotation](#data-collection--annotation)
    - [Data Preprocessing](#data-preprocessing)
    - [Feature Extraction](#feature-extraction)
    - [Machine Learning Models](#machine-learning-models)
    - [Deep Learning Model](#deep-learning-model)
- [Experimental Results](#experimental-results)
- [Limitations \& Future Work](#limitations--future-work)
- [Technologies Used](#technologies-used)
- [Authors](#authors)
- [Acknowledgments](#acknowledgments)
- [License](#license)

***

## Background

Email communication is widely used globally, including in Bangladesh, home to over 234 million Bengali speakers. However, spam emails pose serious security risks such as phishing, malware distribution, and fraud. Existing spam filters often fail to efficiently detect Bengali spam due to linguistic complexities and lack of localized datasets. This project fills that gap by developing a specialized detection system utilizing machine and deep learning methods.

***

## Motivation

- Enhance quality and safety of email communication for Bengali users.
- Protect users against phishing, malware-laden, and scam emails.
- Provide email service providers tools to reduce spam load and optimize resources.
- Address the scarcity of Bengali spam datasets and classifiers.
- Improve overall trustworthiness and user satisfaction in Bengali email ecosystems.

***

## Objectives

- Detect and classify Bengali emails as Spam, Ham, or Promotional.
- Build a comprehensive Bengali spam email dataset with annotations.
- Employ and compare multiple machine learning algorithms.
- Develop a deep learning Bi-LSTM model tailored for Bengali spam detection.
- Integrate ensemble learning strategies for optimal classification performance.
- Compare the proposed system’s performance against existing benchmarks.

***

## Dataset

### Collection \& Composition

The dataset is compiled from multiple real-world sources:

- **Spam emails**: 2992 (31.59%) collected from mobile spam folders, AI-generated samples, and surveys.
- **Ham emails**: 3084 (32.56%) gathered from blogs, personal emails, and AI-generated content.
- **Promotional emails**: 3396 (35.85%) obtained from email promotional folders, ad libraries, and surveys.


### Data Split

- 80% for training
- 20% for testing
The dataset was exhaustively annotated and cleaned to ensure high quality.

<img src="Project images/dataset percent.png">

***

## Methodology

### Data Preprocessing

- Removal of duplicates and handling missing data.
- Bengali text normalization including tokenization, punctuation and emoji removal.
- Stopword elimination to reduce noise.
- Label encoding for classification.


### Feature Extraction

- **TF-IDF Vectorization** having a maximum of 3000 features.
- **Bag-of-Words (BOW)** representation.
- **Word2Vec** embeddings for semantic text representation.


### Machine Learning Models

Classical ML algorithms tested include:

- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- Multinomial Naive Bayes
- Logistic Regression
- AdaBoost
- Bagging Classifier
- Extra Trees Classifier
- XGBoost Classifier

Ensemble methods (voting and stacking) combined models for improved accuracy.

<img src="Project images/Ensemble Model (Voting Classifier).png">


### Deep Learning Model

#### Bidirectional Long Short-Term Memory (Bi-LSTM)

- Embedding layer transforming words into vectors.
- Dual-direction LSTM layers (128 units each) to capture forward and backward context.
- Dropout layer (rate 0.5) to prevent overfitting.
- Flatten → Dense layers with ReLU and final softmax activation for classification.
- Trained over 60 epochs with Adam optimizer and categorical cross-entropy loss.

***

## Experimental Results

### Accuracy Comparison

| Model | Accuracy (%) |
| :-- | :-- |
| Logistic Regression | 84.16 |
| Extreme Gradient Boosting | 85.33 |
| Random Forest | 87.28 |
| Extra Trees Classifier | 88.97 |
| Ensemble (Stacking) | 88.91 |
| Ensemble (Voting) | **89.34** |
| Bi-LSTM Deep Learning | **94.46** |

### Bi-LSTM Performance Metrics

| Class | Precision | Recall | F1-Score |
| :-- | :-- | :-- | :-- |
| Ham | 0.92 | 0.92 | 0.92 |
| Spam | 0.98 | 0.95 | 0.96 |
| Promotional | 0.91 | 0.93 | 0.92 |


***

## Visualizations

### Architecture of Bi-LSTM Model

<img src="Project images/Architecture Of Our Model.jpg">

### Workflow of Machine Learning Model

<img src="/Project images/Workflow of our Machine Learning Model.jpg">

### Model Accuracy Comparison

<img src="Project images/Models Accuracy Comparison.png">

### ROC Curve for Bi-LSTM

<img src="Project images/Roc Curve.png">


## Limitations \& Future Work

- Dataset size constraints impact generalizability.
- False positives reduction needs further investigation.
- Scaling to multi-lingual and real-time systems is planned.
- Future enhancements: dataset expansion, transfer learning, production deployment, user feedback integration.


## Technologies Used

- **Languages:** Python 3.7+
- **Libraries:** TensorFlow, Keras, Scikit-learn, Pandas, NumPy, Matplotlib
- **Platforms:** Jupyter Notebook, Google Colab
- **Hardware:** Tesla T4 GPU (via Google Colab)

***

## Authors

- **Jannatul Ferdous** (ID: 1803510201665)
- **Saima Sultana** (ID: 1803510201689)
- **S M Tahnim Mahir** (ID: 1803510201691)

Supervised by Mr. Dhrubajyoti Das, Lecturer, Computer Science Engineering, Premier University, Chattogram.

***

## Acknowledgments

Thanks to Premier University, project supervisors, and contributors for their invaluable support and guidance throughout this research.

***
