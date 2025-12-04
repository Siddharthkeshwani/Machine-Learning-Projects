# Machine-Learning-Projects

# 🧠 Machine Learning Projects Portfolio

Welcome to my repository of Machine Learning and Data Science projects. Here, I document my journey of analyzing data, building predictive models, and deploying solutions.

## 📂 Project Index

| Project Name | Type | Description | Tech Stack | Status |
| :--- | :--- | :--- | :--- | :--- |
| **[Penguin Species Classification](./Penguin_Species_Classification)** | Classification | End-to-end analysis and prediction of Penguin species based on physical characteristics. | Python, Sklearn, Pandas, Seaborn | ✅ Completed |
| *Future Project* | *Regression* | *Description of next project...* | *Tools used...* | 🚧 In Progress |

---

## 🐧 Project 1: Penguin Species Classification

### 📖 Overview
This project focuses on classifying Palmer Penguins into three species (**Adelie, Chinstrap, Gentoo**) based on physical attributes like culmen length, depth, flipper length, and body mass. The goal was to perform EDA, preprocess the data, and build a robust classification model.

### 🔍 Key Steps
1.  **Exploratory Data Analysis (EDA):**
    * Analyzed species distribution (Adelie is the most common).
    * Discovered a strong correlation (0.87) between Flipper Length and Body Mass.
    * Visualized data using Seaborn (Heatmaps, Countplots).
2.  **Data Preprocessing:**
    * Handled missing values.
    * **Label Encoding** for Target (Species) and Sex.
    * **One-Hot Encoding** for Island location.
3.  **Model Building:**
    * Tested 4 algorithms: Logistic Regression, SVM, Decision Tree, and Random Forest.
    * **Best Model:** Random Forest Classifier.
4.  **Results:**
    * Achieved **100% Accuracy** on the test set.
    * Saved the model using `pickle` for future deployment.

### 🛠️ Libraries Used
* `Pandas` & `Numpy` (Data Manipulation)
* `Matplotlib` & `Seaborn` (Visualization)
* `Scikit-Learn` (Modeling & Evaluation)

### 🚀 How to Use the Model
The trained model is saved as `penguin_model.pkl`. You can load it in Python using:

```python
import pickle

# Load the model
with open('./Penguin_Species_Classification/penguin_model.pkl', 'rb') as file:
    model = pickle.load(file)

# Make a prediction (ensure input data is preprocessed similarly)
# prediction = model.predict(new_data)  
