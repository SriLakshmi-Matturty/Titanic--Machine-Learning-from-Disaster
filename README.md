# 🌊 Titanic Survival Prediction using Decision Tree and Random Forest (From Scratch)

This project implements **Decision Tree** and **Random Forest** classifiers **from scratch** using the famous **Titanic Dataset** from Kaggle. It’s fully contained in a **single Colab Notebook**, and does not rely on external ML libraries like `scikit-learn` for the modeling part.

---

## 🚀 Overview

- Load & preprocess Titanic dataset
- Perform visualizations (e.g., survival by sex and class)
- Implement a Decision Tree classifier from scratch
- Implement a Random Forest classifier using multiple Decision Trees
- Evaluate model performance

---

## 🧠 Algorithms Implemented

### ✅ Decision Tree (From Scratch)

- Select best feature based on Information Gain
- Use recursive splitting with max depth and min samples
- Use Entropy for impurity
- Leaf node is based on most common label

### 🌲 Random Forest (From Scratch)

- Build multiple Decision Trees using bootstrapped samples
- Random feature selection per split
- Final prediction is based on majority voting

---

## 📁 Project Structure

```sh
├── Titanic_Model_From_Scratch.ipynb   
└── README.md                         
```

---

## 📦 Dependencies

```sh
- Python 3.8+
- NumPy
- Pandas
- Matplotlib
- collections.Counter (built-in)
```

> All libraries are standard and already available in Google Colab.

---

## 📊 Visualizations Included

```sh
- Bar plots: Survival Rate by Passenger Class
- Pie charts: Male vs Female survival percentages
```

---

## 🔍 Sample Code Snippets

### 🧼 Preprocessing

```python
X = pd.get_dummies(train[features])
X_test = pd.get_dummies(test[features])
y = train["Survived"]
```

### 🌳 Training a Random Forest

```python
forest = RandomForest(n_trees=10, max_depth=10)
forest.fit(X_train.to_numpy(), y_train.to_numpy())
predictions = forest.predict(X_test.to_numpy())
```

---

## 📈 Results

After training and testing:

- The custom Random Forest performs reasonably well
- Visualizations reveal survival patterns (e.g., higher for women and 1st class)

---

## 📌 Notes

- The models are built without `sklearn`
- This is meant to help understand how trees and forests work internally
- Can be extended to include Gini index or pruning techniques

---

## 🧑‍💻 Author

Built with ❤️ by a Titanic-obsessed ML learner!

---

## 📎 References

- [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic)
- Machine Learning theory from scratch
