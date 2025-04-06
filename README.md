# TITANIC SURVIVAL PREDICTION USING DECISION TREES AND RANDOM FORESTS (FROM SCRATCH)

## 📌 Overview
```sh
This project demonstrates how to build and train Decision Tree and Random Forest classifiers from scratch in Python without using sklearn. We apply these models on the Titanic dataset from Kaggle to predict passenger survival.
```

## 📁 Dataset
```sh
We use the Titanic dataset from Kaggle:
- train.csv — contains labeled data to train the model
- test.csv — used to test predictions after training
```

## ⚙️ Requirements
```sh
- Python 3.6+
- numpy
- pandas
- matplotlib
- collections
```

## 🛠️ Installation
```sh
# 1. Clone the repository
git clone https://github.com/your-username/titanic-ml-from-scratch.git
cd titanic-ml-from-scratch

# 2. (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Linux/macOS
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt
```

## 🧠 Models Implemented
### Decision Tree
```sh
- Calculates entropy and information gain to split nodes
- Stops splitting based on max depth or minimum samples
- Uses recursion to grow the tree
```

### Random Forest
```sh
- Builds multiple decision trees on bootstrapped samples
- Uses random feature selection for each tree
- Combines predictions using majority voting
```

## 📊 Visualizations
```sh
- Survival Rate by Gender
- Survival Rate by Passenger Class
- Pie charts showing survival distribution
- Bar plots for class-based survival

These are useful for EDA and choosing meaningful features.
```

## 🧪 Key Functions

### Entropy Function
```sh
Calculates entropy of a target variable:
entropy = -Σ p * log2(p)
```

### Information Gain
```sh
Measures reduction in entropy after a split.
IG = entropy(parent) - [weighted entropy(left) + weighted entropy(right)]
```

### Data Preparation
```sh
- Uses pd.get_dummies to encode categorical variables
- Splits data into training and testing using custom function
```

### Tree Building
```sh
- Recursively split based on best info gain
- Create leaf node if stopping condition is met
```

### Random Forest
```sh
- Fit multiple trees using bootstrapped samples
- Each tree trained with random subset of features
- Final prediction: majority vote across trees
```

## 📂 Project Structure
```sh
├── train.csv                # Training dataset from Kaggle
├── test.csv                 # Test dataset from Kaggle
├── main.py                  # Main driver code
├── decision_tree.py         # Decision Tree class implementation
├── random_forest.py         # Random Forest class using multiple trees
├── preprocessing.py         # Data cleaning and transformation
├── visualizations.py        # Plotting survival rates and distributions
├── utils.py                 # Helper functions
└── README.md                # This file
```

## ▶️ How to Run
```sh
# Run the main script to start training and prediction
python main.py
```

## ✅ Sample Output
```sh
Training Decision Tree...
Accuracy on validation set: 80.5%

Training Random Forest with 10 trees...
Accuracy on validation set: 85.2%
```

## 🔍 Future Improvements
```sh
- Add support for Gini Impurity
- Include pruning strategies
- Cross-validation
- ROC-AUC and F1-score metrics
- Model saving/loading with pickle
```

## 🙌 Acknowledgements
```sh
- Kaggle for the Titanic dataset
- Blogs and resources that explain ML algorithms from scratch
```

## 🪪 License
```sh
This project is licensed under the MIT License.
```
