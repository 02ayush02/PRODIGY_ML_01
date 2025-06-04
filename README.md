# 🏠 House Price Prediction using Linear Regression

This project demonstrates a simple yet effective approach to predicting house sale prices using a **Linear Regression** model. It uses selected numerical features from a housing dataset to build a baseline model and evaluate its performance.

## 📂 Dataset

- **train.csv**: Contains house features and the target variable `SalePrice`.
- **test.csv**: Contains house features for which predictions are to be made.

## 📌 Features Used

The model uses the following features:
- `GrLivArea` (Above ground living area in square feet)
- `BedroomAbvGr` (Number of bedrooms above ground)
- `FullBath` (Number of full bathrooms)

## 🧹 Data Cleaning & Preprocessing

- Removed duplicate entries.
- Dropped rows with missing values in selected features for training.
- Filled missing values in the test set using median imputation.
- Removed outliers with `GrLivArea > 4000` to reduce model skewing.

## 🧠 Model: Linear Regression

- Trained using `scikit-learn`'s `LinearRegression` model.
- Split the dataset into training and validation sets (80:20).
- Evaluated using RMSE and R² score.

## 📈 Results

- **Validation RMSE**: ~$47,000  
- This corresponds to ~26.23% of the average house price.
- Basic scatter plots and bar charts were used for exploratory analysis.

## 🔍 Limitations

- The model is trained using only 3 numerical features.
- Linear regression cannot model complex or nonlinear relationships in data.
- High RMSE indicates underfitting.

## 🚀 Future Improvements

- Include more impactful features (e.g., `OverallQual`, `YearBuilt`, `GarageArea`).
- Try nonlinear models such as Random Forest or Gradient Boosting.
- Perform hyperparameter tuning and cross-validation.
- Apply feature engineering and scaling.

## 📁 Output

- A submission CSV file `output.csv` is generated containing predicted sale prices for the test data.

## 🛠️ Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- matplotlib

Install dependencies:
```bash
pip install -r requirements.txt
