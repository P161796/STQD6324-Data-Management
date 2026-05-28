# Iris Classification using Spark MLlib

## Project overview

This project uses Spark MLlib to classify iris flower species based on sepal and petal measurements. The dataset used is the Iris dataset, which contains three flower species and four numerical features.

Three classification models are developed and compared in this project:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier

Grid search and cross-validation are used to tune the hyperparameters of each model. The models are then evaluated using accuracy, precision, recall, and F1-score.

## Dataset Description

The dataset used in this project is the Iris dataset. It contains 150 samples of iris flowers from three different species:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

The dataset contains the following feature columns:

- SepalLengthCm
- SepalWidthCm
- PetalLengthCm
- PetalWidthCm

The target variable is:

- Species

The dataset was obtained from Kaggle:

https://www.kaggle.com/datasets/uciml/iris

## Methodology

The workflow of this project includes the following steps:

1. Load the Iris dataset into a Spark DataFrame.
2. Explore the dataset structure, summary statistics, and class distribution.
3. Check missing values.
4. Remove the Id column because it is only an identifier.
5. Convert the Species column into numerical labels using StringIndexer.
6. Combine the feature columns into a single features vector using VectorAssembler.
7. Split the dataset into training and testing datasets.
8. Train three classification models using Spark MLlib.
9. Apply grid search and cross-validation for hyperparameter tuning.
10. Generate predictions on the testing dataset.
11. Evaluate the models using accuracy, precision, recall, and F1-score.
12. Compare the models and select the most suitable model.

## Results and Key Findings

The table below summarises the model evaluation results obtained from the notebook.


| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| Decision Tree Classifier | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| Random Forest Classifier | 1.0000 | 1.0000 | 1.0000 | 1.0000 |

Based on the evaluation results, all three models achieved the same performance in this experiment. The models were able to correctly classify the testing samples.

This result may be because the Iris dataset is small, balanced, and the three species can be separated well using the sepal and petal measurements.

Although all three models achieved the same evaluation scores, Logistic Regression was selected as the most suitable model. This is because it achieved the same performance as the other models while being simpler, faster, and easier to interpret.

## How to Reproduce the Analysis

To reproduce this analysis, follow the steps below:

1. Open the notebook file in Google Colab.
2. Run the PySpark installation cell.
3. Upload the Iris.csv dataset when required.
4. Run all notebook cells from top to bottom.
5. View the model evaluation results and comparison.

## Files in This Repository

- `P161796_YANG_HUAN.ipynb` : Jupyter Notebook containing the full analysis and implementation.
- `Iris.csv` : Iris dataset used in this project.
- `README.md` : Project description and instructions.
