<div align="center">

# Wine Classification with Power BI & Machine Learning

### Bringing machine learning directly into Power BI with Python.

[![Power BI](https://img.shields.io/badge/Power_BI-Data_Analytics-F2C811?logo=powerbi&logoColor=black)](https://www.microsoft.com/power-platform/products/power-bi)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Machine_Learning-F7931E?logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![Machine Learning](https://img.shields.io/badge/Machine_Learning-Classification-00897B)](https://en.wikipedia.org/wiki/Statistical_classification)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Developed by [Rui Ribeiro](https://github.com/ruialexrib)

</div>

---

## About

**Wine Classification with Power BI & Machine Learning** is a demonstration project showing how a machine learning model can be integrated directly into **Microsoft Power BI** using **Python** and **scikit-learn**.

The project uses physicochemical wine properties to classify each observation as **red** or **white**. The machine learning workflow is executed through a Python script in **Power Query**, demonstrating how predictive analytics can be incorporated into a Business Intelligence solution without requiring a separate machine learning application.

## Project Objectives

- Demonstrate the integration of Python and machine learning with Power BI
- Train a classification model using scikit-learn
- Classify wines as red or white from physicochemical properties
- Execute the predictive workflow inside Power Query
- Combine Business Intelligence and Machine Learning in a simple reproducible example

## Machine Learning Approach

The project uses the **Extra Trees (Extremely Randomized Trees)** ensemble classifier from scikit-learn.

The workflow follows these main steps:

1. Load and prepare the wine dataset
2. Separate the predictor variables from the target variable (`style`)
3. Split the dataset into training (70%) and test (30%) sets
4. Train the Extra Trees classifier
5. Evaluate model performance
6. Generate predictions for wine type
7. Make the resulting data available for analysis in Power BI

## Power BI Integration

The machine learning workflow is incorporated into **Power Query** using a Python script. This allows data preparation, model training and prediction to become part of the Power BI data transformation pipeline.

```text
Wine Dataset
     │
     ▼
Power Query
     │
     ▼
Python / scikit-learn
     │
     ▼
Extra Trees Classifier
     │
     ▼
Predicted Wine Type
     │
     ▼
Power BI
```

This architecture illustrates a practical way of extending traditional Business Intelligence workflows with predictive analytics.

## Technology

| Technology | Role |
| --- | --- |
| **Power BI** | Business Intelligence, data transformation and visualization |
| **Power Query** | Data preparation and Python integration |
| **Python** | Machine learning workflow |
| **pandas** | Data manipulation |
| **scikit-learn** | Extra Trees classification model |
| **Jupyter Notebook** | Model development and experimentation |

## Project Structure

```text
powerbi-wine-ml-demo/
├── src/
│   ├── wine_dataset.csv          # Wine dataset
│   ├── wine_ml_extratrees.ipynb  # Jupyter notebook
│   ├── wine_ml_extratrees.pbix   # Power BI report
│   └── requirements.txt          # Python dependencies
├── LICENSE
└── readme.md
```

## Requirements

The Python dependencies are intentionally minimal:

```text
pandas>=1.5.0
scikit-learn>=1.2.0
```

Install them with:

```bash
pip install -r src/requirements.txt
```

To execute Python scripts from Power BI Desktop, a local Python installation must also be configured in the Power BI Python scripting settings.

## Running the Demo

Clone the repository:

```bash
git clone https://github.com/ruialexrib/powerbi-wine-ml-demo.git
cd powerbi-wine-ml-demo
```

Install the Python dependencies and open `src/wine_ml_extratrees.pbix` with Power BI Desktop.

The accompanying Jupyter notebook, `src/wine_ml_extratrees.ipynb`, can be used to inspect and experiment with the machine learning workflow independently of Power BI.

## Use Case

This project is intended as a compact demonstration of how **Business Intelligence**, **data analytics** and **machine learning** can be combined in the same analytical workflow.

Although wine classification is used as the example, the same integration pattern can be adapted to business scenarios such as customer classification, churn prediction, risk analysis, demand forecasting and other predictive analytics use cases.

## License

Distributed under the [MIT License](LICENSE).

Copyright © 2026 [Rui Ribeiro](https://github.com/ruialexrib).
