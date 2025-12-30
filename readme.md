# Wine Classification with Power BI and Extra Trees

This project demonstrates how **machine learning** can be integrated into **Power BI** using **Python (scikit-learn)** to classify wine type (`red` or `white`) based on physicochemical properties.

The solution is implemented entirely inside a Power BI report using a Python script in **Power Query**.

## Files

- `wine_ml_extratrees.pbix`  
  Power BI report containing the full workflow.

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


## License

This project is provided for educational and demonstration purposes.
