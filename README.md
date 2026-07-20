# Loan Default Data - EDA & Preprocessing

This repository contains the Exploratory Data Analysis (EDA) and data preprocessing steps for a Loan Default dataset. The goal of this project is to clean the raw data and prepare it for machine learning models.

## Files in this Repository
* `Loan_default.csv`: The raw dataset containing customer loan information.
* `preprocessing.ipynb`: The Jupyter Notebook containing all the Python code for data cleaning and visualization.

## Tools & Libraries Used
* **Python** 
* **Pandas** (for data manipulation)
* **NumPy** (for numerical operations)
* **Matplotlib & Seaborn** (for data visualization)
* **Scikit-Learn** (for encoding and scaling)

## Preprocessing Steps Performed
Based on standard data cleaning practices, the following steps are implemented in the notebook:
1. **Understanding the Data**: Checking the shape, data types, and basic information.
2. **Cleaning Columns**: Converting column names to lowercase and dropping unnecessary columns like `loanid`.
3. **Handling Missing Values & Duplicates**: Checking for empty cells and removing duplicate records.
4. **Outlier Detection**: Using the Interquartile Range (IQR) method to remove extreme values from columns like `income`.
5. **Categorical Encoding**: Using `LabelEncoder` to convert text columns (e.g., education, employment type, marital status) into numerical values.
6. **Feature Scaling**: Applying `MinMaxScaler` to bring numerical features (e.g., age, income, loan amount) to a standard range between 0 and 1.
7. **Data Visualization**: 
   - **Histograms** for data distribution
   - **Box Plots** to check for outliers
   - **Scatter Plots** to observe relationships between variables
   - **Bar and Pie Charts** to analyze categorical data

## How to Run
1. Clone this repository to your local machine using Git.
2. Open the project folder in VS Code or Jupyter Notebook.
3. Make sure you have the required libraries installed (`pip install pandas numpy matplotlib seaborn scikit-learn`).
4. Run the cells in `preprocessing.ipynb` sequentially.

## Future Scope

Currently, this project covers the data preprocessing and exploratory analysis phases. The future roadmap to make this a complete, live application includes:

1. **Model Training & Evaluation:** 
   - Train various machine learning classification models (like Logistic Regression, Random Forest, or XGBoost) on this cleaned dataset.
   - Evaluate the models using accuracy, precision, and recall to find the best-performing one for predicting loan defaults.

2. **Backend API Development:**
   - Export the trained model and the scalers/encoders using a tool like `pickle` or `joblib`.
   - Build a simple Python backend API (using Flask or FastAPI) that can receive new data and return prediction results.

3. **Live Web Frontend:**
   - Develop an interactive frontend interface (using JavaScript, HTML, and CSS) where users can input their loan details like income, loan amount, and credit score.
   - Connect the frontend to the backend API so it can display real-time predictions on whether a loan might default.

4. **Deployment:**
   - Host the web application and the model on a cloud platform (like Render or Heroku) so it can be accessed live on the internet.
