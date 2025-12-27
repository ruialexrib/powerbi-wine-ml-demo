# Wine Classification with Power BI and Extra Trees

This project demonstrates how **machine learning** can be integrated into **Power BI** using **Python (scikit-learn)** to classify wine type (`red` or `white`) based on physicochemical properties.

The solution is implemented entirely inside a Power BI report using a Python script in **Power Query**.

## Files

- `wine_ml_extratrees.pbix`  
  Power BI report containing the full workflow:
  - Data loading
  - Train/test split
  - Model training with `ExtraTreesClassifier`
  - Evaluation (Accuracy, Precision, Recall, F1-Score)
  - Predictions stored in the dataset

- `wine_dataset.csv`  
  Dataset containing physicochemical wine features and the target variable `style`.

## Machine Learning Approach

The model is trained using the **Extra Trees** ensemble algorithm from scikit-learn.

Core steps:
1. Separate features and target variable
2. Split data into training (70%) and test (30%) sets
3. Train the model
4. Evaluate performance
5. Predict wine type

Example logic used in the Power BI Python script:

```python
from sklearn.model_selection import train_test_split
from sklearn.ensemble import ExtraTreesClassifier

y = dataset["style"]
X = dataset.drop("style", axis=1)

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.30
)

model = ExtraTreesClassifier()
model.fit(X_train, y_train)

dataset["Predict"] = model.predict(X)
