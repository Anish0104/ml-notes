# ML Notes

Personal learning notes for Machine Learning and Data Science fundamentals. This repository contains concise explanations, formulas, and examples built while practicing ML concepts and building projects.

---

## 📈 Supervised Learning

### Linear Regression
* **Objective**: Minimize the Residual Sum of Squares (RSS) between observed and predicted values.
* **Cost Function**: $J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)})^2$
* **Optimization**: Solved via the Normal Equation $(X^T X)^{-1} X^T y$ for small datasets or Gradient Descent for large-scale production data.

### Logistic Regression
* **Mechanism**: Uses the Sigmoid function $\sigma(z) = \frac{1}{1 + e^{-z}}$ to map linear outputs to probabilities $(0, 1)$.
* **Loss Function**: Binary Cross-Entropy (Log Loss), which penalizes confident but wrong predictions.
* **Decision Boundary**: The hyperplane where the probability equals 0.5.

### Decision Trees & Ensembles
* **Splitting**: Uses Gini Impurity or Entropy (Information Gain) to find the feature and threshold that best separates the classes.
* **Random Forest**: Reduces variance by training multiple trees on bootstrapped samples (Bagging) and averaging results.
* **Boosting (XGBoost/LightGBM)**: Reduces bias by training trees sequentially, where each new tree focuses on the residuals of the previous model.

---

## 🔍 Unsupervised Learning

### K-Means Clustering
* **Algorithm**: Iteratively assigns points to the nearest centroid using Euclidean distance and recalculates centroids based on the mean of the clusters.
* **Elbow Method**: Used to determine the optimal number of clusters ($K$) by plotting inertia against $K$.

### Principal Component Analysis (PCA)
* **Mathematical Goal**: Identify the orthogonal axes (principal components) that capture the maximum variance in the data.
* **Application**: Dimensionality reduction to speed up training and remove noise/redundancy.

---

## 🧠 Core Concepts & Optimization

### Bias-Variance Tradeoff
* **Bias**: Error due to overly simple assumptions (Underfitting).
* **Variance**: Error due to excessive sensitivity to training data noise (Overfitting).
* **Regularization**: 
    * **L1 (Lasso)**: Adds $\lambda \sum |w|$ to the loss, encouraging weight sparsity (feature selection).
    * **L2 (Ridge)**: Adds $\lambda \sum w^2$ to the loss, preventing weights from becoming disproportionately large.

### Evaluation Metrics
* **Regression**: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and $R^2$ Score.
* **Classification**: Precision (Exactness), Recall (Completeness), and F1-Score (Harmonic Mean).
* [cite_start]**Retrieval (RAG)**: NDCG@10 and MRR, which measure the relevance of ranked search results[cite: 33, 34].

---

## 🛠️ Tools & Stack
* **Languages**: Python (NumPy, Pandas), SQL, JavaScript.
* **Frameworks**: PyTorch, TensorFlow, Scikit-learn, and FastAPI.
* [cite_start]**Deployment**: Docker, ChromaDB/Qdrant (Vector DBs), and Weights & Biases for experiment tracking[cite: 17, 19, 35].

---

## Goal
[cite_start]Maintain structured notes while practicing ML concepts and shipping production-grade AI systems, such as RAG pipelines and Reinforcement Learning agents[cite: 5, 32, 48].
