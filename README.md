# Customer Purchase Prediction with Class Imbalance Handling

## Project Overview
This project aims to predict customer behavior, specifically whether a customer will make their next purchase. Using machine learning techniques, this project addresses class imbalance and emphasizes precision, recall, and F1-scores over accuracy to ensure robust predictions for the minority class.

The solution combines data preprocessing, feature engineering, model optimization, and evaluation to improve predictions, especially for rare events (next purchase prediction).

## Key Features

- **Handling Class Imbalance**: The project tackles class imbalance by focusing on metrics like precision, recall, and F1-score.
- **Data Preprocessing**: Includes handling missing values, encoding categorical features, and converting date columns to datetime format.
- **Model Training**: The models used are **XGBoost** and **Random Forest**, which are trained on the data to predict customer behavior.
- **Evaluation**: Classifiers are evaluated using metrics suited for imbalanced datasets, such as recall and F1-score, along with confusion matrix analysis.
- **Final Output**: The predictions are saved in a CSV file containing `User_Key` and predicted `Next_Purchase`.

## Dataset
- **Training Dataset**: `participants_training_dataset.csv`
- **Test Dataset**: `participants_test_dataset.csv`

## Requirements
To run the project, you'll need to install the following dependencies:

- pandas
- numpy
- matplotlib
- seaborn
- xgboost
- scikit-learn

You can install the required libraries with the following:

```bash
pip install -r requirements.txt
```

## Data Preprocessing Steps

1. **Handle Missing Values**: Missing values in columns like `Annual_Income` are filled with the mean value.
2. **Encoding Categorical Variables**: `Edu_Level` is encoded using `OrdinalEncoder` to represent education levels in an ordered manner.
3. **Date Conversion**: `Reg_Date` is converted into a datetime format and transformed into days since the Unix epoch for machine learning processing.
4. **Handling Rare Categories**: Rare categories in `Family_Status` are replaced with their frequency counts and then the column is dropped.

## Model Training

### XGBoost Model
- Used for its high performance with large datasets and handling of imbalanced data.
- Optimized using precision, recall, and F1-score.

### Random Forest Model
- Used to evaluate feature importance and handle class imbalance.

Both models are evaluated and compared to ensure optimal performance for both classes.

## Evaluation Metrics

The models are evaluated using the following metrics:
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

The focus is placed on improving the recall of the minority class to ensure that critical purchases are predicted correctly.

## Final Predictions

The final predictions are saved in a CSV file containing the `User_Key` and predicted `Next_Purchase` value:

```csv
User_Key, Next_Purchase
1001, 1
1002, 0
...
```

## How to Run

1. Clone the repository to your local machine.
2. Install the required libraries.
3. Load your training and test datasets.
4. Preprocess the data as described in the **Data Preprocessing Steps** section.
5. Train the model and evaluate the performance.
6. Make predictions on the test data and output results to a CSV file.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- **XGBoost**: For efficient gradient boosting.
- **Scikit-learn**: For easy-to-use machine learning tools.
- **Pandas**: For data manipulation and analysis.
- **Matplotlib/Seaborn**: For data visualization.
```

