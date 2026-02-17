# Iris Species Classification with KNN & Feature Engineering

This project implements a K-Nearest Neighbors (KNN) classifier to identify Iris flower species. Beyond standard classification, this notebook explores **custom feature engineering** (calculating petal area and combined lengths) and validates model stability using **K-Fold Cross-Validation**.

## 🚀 Project Overview

The goal was to move beyond basic tutorial steps and investigate how engineered features impact classification accuracy.

* **Dataset:** Fisher's Iris Dataset (150 samples, 4 features).
* **Target:** 3 Species (Setosa, Versicolor, Virginica).
* **Key Focus:** Feature engineering, multivariate EDA, and performance reliability.

---

## 📊 Exploratory Data Analysis (EDA)

I performed an in-depth analysis of the features to understand class separation:

* **Univariate Analysis:** Used Box Plots to identify the range and outliers of sepal/petal dimensions.
* **Multivariate Analysis:** Utilized Pairplots and Heatmaps to identify a 96% correlation between petal length and width.
* **Feature Engineering:** * Created an `area` feature: 
* Created a `length` feature: Sum of Sepal and Petal lengths.



---

## 🛠️ Technical Stack

* **Language:** Python 3.x
* **Libraries:** * `Pandas` & `NumPy`: Data manipulation.
* `Seaborn` & `Matplotlib`: Statistical visualization.
* `Scikit-Learn`: Machine learning, scaling, and validation.



---

## 🧠 Modeling & Performance

I utilized a **K-Nearest Neighbors (KNN)** approach with  and feature scaling via `StandardScaler`.

### 1. Initial Results (Train-Test Split)

On a standard 80/20 split, the model achieved **100% accuracy**.

* **Confusion Matrix:**
```text
[[10  0  0]
 [ 0  9  0]
 [ 0  0 11]]

```



### 2. Validation (K-Fold Cross-Validation)

To ensure the 100% wasn't a "lucky" split, I implemented **5-Fold Cross-Validation**:

* **Mean Accuracy:** 95.0%
* **Standard Deviation:** ± 4.0%
* **Insight:** The variation in scores (90% to 100%) indicates that while the model is strong, it is slightly sensitive to specific data distributions in such a small dataset.

---

## 📈 Key Findings

1. **Linear Separability:** Iris-Setosa is perfectly separable from other species using almost any feature.
2. **Feature Importance:** Engineered features like `area` provide a strong signal but confirm that Versicolor and Virginica share a "fuzzy" boundary that requires non-linear classification.
3. **Stability:** Cross-validation is essential for small datasets to get a realistic picture of model performance.

---

## 📂 How to use

1. Clone the repo.
2. Ensure you have `scikit-learn`, `pandas`, and `seaborn` installed.
3. Run the `irish.ipynb` notebook.
