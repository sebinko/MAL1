# 📌 Session: Introduction to Machine Learning & k-Nearest Neighbor (kNN)

---

## 🧠 What is Machine Learning (ML)?
- Traditional algorithms: Solve problems using fixed rules or formulas.
- ML: Learns patterns and rules from **examples (data)** instead of being explicitly programmed.
- The model **writes the algorithm** from the data it sees.

---

## 🔍 Types of ML Problems

### Supervised Learning (labeled data)
- **Classification**: Predict categories (e.g., spam vs. not spam).
- **Regression**: Predict continuous values (e.g., price, temperature).

### Unsupervised Learning (unlabeled data)
- **Clustering**: Group similar items (e.g., customer segments).
- **Dimensionality Reduction**: Reduce number of features (e.g., PCA for visualization).

---

## 🔄 The Train-Test Methodology
- Split your dataset into:
  - **Training data** – to build the model.
  - **Test data** – to evaluate how well the model generalizes.
- Use **train accuracy** and **test accuracy** to measure performance.

---

## 📈 Evaluating Model Outputs
- **Accuracy**: % of correct predictions.
- **Confusion Matrix**: Shows how predictions are distributed across true vs. predicted classes.
- Other metrics (covered later): **Precision**, **Recall**, **F1-score**.

---

# 🔍 k-Nearest Neighbors (kNN)

---

## 🧭 How It Works
- A *lazy learning* algorithm: No explicit training phase.
- To classify a new point:
  - Find the **k** closest training points (neighbors).
  - Use **majority vote** (for classification) or average (for regression) to decide output.

---

## 📏 Distance Metrics in kNN
Common distance metrics:
- **Euclidean** (straight-line)
- **Manhattan**
- **Minkowski**
- **Hamming**
- **Levenshtein**
- **Mahalanobis** (context-specific)

---

## 🔧 The "k" Parameter
- **Small k**: Model is more flexible (**low bias**, **high variance**).
- **Large k**: Model is more stable (**high bias**, **low variance**).
- Best value for k is usually found via **cross-validation**.

---

## ⚖️ Bias vs. Variance
- **Low bias** = model fits training data well.
- **Low variance** = model generalizes well to new data.
- kNN’s flexibility depends heavily on **k**.

---

## 📊 Data Normalization
- kNN uses **distance**, so **feature scales must match**.
- Normalize data to avoid one feature dominating:
  - **Standardization** (z-scores)
  - **Min-max scaling**

---

## ⚙️ Hyperparameters in ML
- **Hyperparameters**: Settings like **k** in kNN or the distance metric.
- Set **before training**.
- Found through **search or validation techniques**.

---

## 🧪 Hands-on: Training a kNN Model in `sklearn`
1. Load dataset (e.g., Titanic).
2. Preprocess features (normalize).
3. Use `KNeighborsClassifier` from `sklearn.neighbors`.
4. Fit model, predict, and evaluate.
