# Book Recommendation System

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Recommender%20System-green)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-red)

## 📖 Overview

The **Book Recommendation System** is a machine learning-based application designed to help users discover books that match their interests and reading preferences. With the enormous number of books available online, readers often face information overload when searching for relevant titles.

This project leverages user ratings, book metadata, and user demographic information to generate personalized recommendations. Multiple recommendation techniques were implemented and compared, including:

* Popularity-Based Recommendation
* Content-Based Filtering
* Collaborative Filtering (KNN + Cosine Similarity)
* Matrix Factorization (SVD)

The system aims to improve user experience by providing accurate and meaningful book suggestions while reducing the effort required to discover new books.

---

## 🎯 Problem Statement

Readers today have access to millions of books across various genres and platforms. While this accessibility is beneficial, it creates challenges in identifying books that align with individual preferences.

The goal of this project is to build an intelligent recommendation system capable of:

* Understanding user preferences through historical ratings.
* Analyzing book metadata and user demographics.
* Providing personalized and relevant book recommendations.
* Improving book discovery and user engagement.

---

## 🚀 Objectives

* Clean and preprocess multiple datasets.
* Perform Exploratory Data Analysis (EDA).
* Build and compare different recommendation models.
* Generate personalized book recommendations.
* Evaluate recommendation quality using standard metrics.
* Create a scalable recommendation framework.

---

## 📂 Dataset Description

The project uses three datasets:

### 1. Books.csv

| Feature             | Description            |
| ------------------- | ---------------------- |
| ISBN                | Unique Book Identifier |
| Book-Title          | Title of the Book      |
| Book-Author         | Author Name            |
| Year-Of-Publication | Publication Year       |
| Publisher           | Publisher Name         |
| Image-URL-S         | Small Book Cover       |
| Image-URL-M         | Medium Book Cover      |
| Image-URL-L         | Large Book Cover       |

---

### 2. Users.csv

| Feature  | Description            |
| -------- | ---------------------- |
| User-ID  | Unique User Identifier |
| Location | User Location          |
| Age      | User Age               |

---

### 3. Ratings.csv

| Feature     | Description            |
| ----------- | ---------------------- |
| User-ID     | Unique User Identifier |
| ISBN        | Book Identifier        |
| Book-Rating | User Rating (0–10)     |

---

## 🏗️ Recommendation System Architecture

### Recommendation Taxonomy

```text
Recommendation Systems
│
├── Non-Personalized
│   └── Most Popular Books
│
└── Personalized
    ├── Content-Based Filtering
    ├── Collaborative Filtering
    │   ├── Memory-Based
    │   │   ├── User-Based
    │   │   └── Item-Based
    │   │
    │   └── Model-Based
    │       ├── KNN
    │       ├── SVD
    │       └── Matrix Factorization
    │
    └── Hybrid Approaches
```

---

## 🔍 Exploratory Data Analysis (EDA)

The following analyses were performed:

### User Analysis

* User age distribution
* Most active users
* User location analysis

### Book Analysis

* Most rated books
* Highest-rated books
* Publication year trends
* Top authors and publishers

### Rating Analysis

* Rating distribution
* Rating frequency by age groups
* User activity vs average rating

### Key Insights

* Most users belong to the 20–39 age group.
* Ratings are heavily skewed toward higher values.
* A small number of books account for most ratings.
* Popular authors receive significantly more engagement.
* User-book interactions exhibit a long-tail distribution.

---

## 🧹 Data Preprocessing

### Missing Value Handling

* Missing authors and publishers → replaced with `"Unknown"`
* Missing ages → replaced with median age
* Invalid publication years → corrected using median year

### Outlier Treatment

* Age values below 10 or above 100 were treated.
* Invalid publication years were corrected.

### Feature Engineering

Created:

* Encoded User IDs
* Encoded Book IDs
* Combined text content feature:

  * Book Title
  * Author
  * Publisher

Used for Content-Based Filtering.

---

## 🤖 Models Implemented

### 1. Popularity-Based Recommendation

Recommends books based on:

* Highest average ratings
* Highest rating counts

#### Advantages

* Simple
* Effective for new users
* Fast computation

---

### 2. Content-Based Filtering

Uses:

* Book Title
* Author
* Publisher

Technique:

```python
TF-IDF Vectorization
+
Cosine Similarity
```

#### Advantages

* Works for new books
* Explainable recommendations
* No dependency on user history

---

### 3. Collaborative Filtering

Implemented using:

* K-Nearest Neighbors (KNN)
* Cosine Similarity

#### Workflow

1. Build User-Item Matrix
2. Compute Similarity
3. Find Nearest Neighbors
4. Recommend Similar Books

#### Advantages

* Personalized recommendations
* Captures hidden user preferences

---

### 4. Matrix Factorization (SVD)

Singular Value Decomposition (SVD) was used to:

* Reduce sparsity
* Discover latent user-book relationships
* Improve recommendation quality

#### Advantages

* High scalability
* Better prediction accuracy
* Handles large datasets efficiently

---

## 📊 Model Evaluation

The models were evaluated using:

### Root Mean Squared Error (RMSE)

[
RMSE = \sqrt{\frac{\sum(y-\hat{y})^2}{n}}
]

Measures prediction error between actual and predicted ratings.

### Mean Absolute Error (MAE)

[
MAE = \frac{\sum |y-\hat{y}|}{n}
]

Measures average prediction deviation.

### Additional Evaluation

* Recommendation relevance
* Recommendation diversity
* User satisfaction analysis

---

## 🛠️ Technology Stack

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* SciPy
* Surprise
* TensorFlow (optional experiments)

### Recommendation Algorithms

* KNN
* Cosine Similarity
* TF-IDF
* SVD

---

## 📁 Project Structure

```
Book Recommendation System/
│
├── 📁 Dataset/
│   ├── Dataset Description.docx
│   └── LoyaltyVision Analytics Dataset.xlsx
│
├── 📁 Final Report/
│   └── Final Report.pdf
|
├── 📁 Notebook/
│   └── Book Recommendation System.ipynb
|
└── 📁 README.md
```

---

## 📈 Results

The recommendation system successfully:

✅ Identified popular books for general users

✅ Generated personalized recommendations using collaborative filtering

✅ Recommended similar books through content analysis

✅ Improved prediction quality using matrix factorization

### Key Findings

* Collaborative Filtering produced the most personalized recommendations.
* Content-Based Filtering handled cold-start books effectively.
* Popularity-Based Filtering worked well for new users.
* SVD improved rating prediction accuracy by capturing latent features.

---

## 🔮 Future Enhancements

* Hybrid Recommendation System
* Deep Learning-Based Recommenders
* NLP-based Book Description Analysis
* Real-Time Recommendation API
* Web Application Deployment (Flask/Streamlit)
* User Authentication and Profiles

---

## 🤝🏿 **Contributing**

This project represents my personal learning in Data Science. While this is primarily a showcase of my work, I welcome discussions, feedback, and collaborations on data science projects.

## 📧 **Contact**

**Sanketh Ks**  
- GitHub: [@Sankethks27](https://github.com/Sankethks27)
- LinkedIn: [Sanketh Ks](https://www.linkedin.com/in/sanketh-ks-181962273/)
- Email: sankethks27@gmail.com

---

⭐ **If you find this portfolio helpful or inspiring, please give it a star!** ⭐

---
