# 🐧 Penguin Species Classification

## 📌 Project Overview
This project involves building a Machine Learning model to predict the species of a penguin based on its physical characteristics. The dataset contains measurements for three species: **Adelie**, **Chinstrap**, and **Gentoo** collected from three islands in the Palmer Archipelago, Antarctica.

## 📂 File Description

* **`Penguin_ML_Project.ipynb`**: The Jupyter Notebook containing the complete source code for Data Cleaning, Exploratory Data Analysis (EDA), Model Building, and Evaluation.
* **`penguins_size.csv`**: The dataset used for training and testing the model.
* **`penguin_model.pkl`**: The final trained Random Forest model saved using `pickle`. This file can be loaded to make predictions on new data without retraining.

## 📊 Dataset Details
The dataset (`penguins_size.csv`) includes the following features:
* **Species:** Target variable (Adelie, Chinstrap, Gentoo).
* **Island:** Location where the penguin was observed (Dream, Torgersen, Biscoe).
* **Culmen Length (mm)** & **Culmen Depth (mm)**: Measurements of the beak.
* **Flipper Length (mm)**: Length of the wing.
* **Body Mass (g)**: Weight of the penguin.
* **Sex:** Male or Female.

## 🛠️ Approach & Methodology

1.  **Data Preprocessing:**
    * Handled missing values by dropping rows with nulls (missing data was < 5%).
    * Converted the 'Island' column using **One-Hot Encoding**.
    * Converted 'Sex' and 'Species' using **Label Encoding**.

2.  **Exploratory Data Analysis (EDA):**
    * Analyzed correlations between features (e.g., Flipper Length vs. Body Mass).
    * Visualized species distribution across islands.

3.  **Model Selection:**
    * We experimented with four different algorithms:
        * Logistic Regression (98.51% Accuracy)
        * Support Vector Machine (73.13% Accuracy)
        * Decision Tree (98.51% Accuracy)
        * **Random Forest Classifier (100.00% Accuracy)**

## 🏆 Results
The **Random Forest Classifier** was selected as the best model, achieving an accuracy score of **100%** on the test set.

## 🚀 How to Run
1.  Ensure you have Python installed with the following libraries:
    * `pandas`
    * `numpy`
    * `seaborn`
    * `matplotlib`
    * `scikit-learn`
2.  Open the notebook:
    ```bash
    jupyter notebook Penguin_ML_Project.ipynb
    ```
3.  Run all cells to see the analysis and training process.

## 🔮 Future Usage (Deployment)
To use the saved model (`penguin_model.pkl`) in a different script:

```python
import pickle

# Load the trained model
with open('penguin_model.pkl', 'rb') as file:
    model = pickle.load(file)

# Prediction logic here...
