# E-Commerce-Furniture-Sales-Analysis
This project analyzes an e-commerce furniture dataset to predict sales. It covers data preprocessing, EDA, feature engineering (TF-IDF), and regression modeling (Linear Regression, Random Forest). Models currently show poor performance, indicating a need for advanced techniques and more data.

Project Overview
This project aims to build and evaluate machine learning models to predict the number of furniture items sold (sold) based on various product attributes from an e-commerce dataset. The goal is to understand the factors influencing sales and develop predictive capabilities.

Dataset
The dataset used in this project comprises 2,000 entries, detailing a variety of furniture products. It captures key sales metrics and product details, offering a snapshot of consumer purchasing patterns and market trends in the online furniture retail space.

Key Columns:

productTitle: The name of the furniture item.

originalPrice: The original price of the item before any discounts.

price: The current selling price of the item.

sold: The number of units sold (Target Variable).

tagText: Additional tags associated with the item (e.g., "Free shipping").

Project Structure & Steps
The project follows a standard machine learning workflow:

Data Collection: Loading the ecommerce_furniture_dataset_2024.csv file.

Data Preprocessing:

Handling missing values (e.g., imputing originalPrice, filling tagText).

Converting data types (price to float).

Grouping and encoding categorical features (tagText).

Exploratory Data Analysis (EDA):

Visualizing distributions of key numerical features (price, sold).

Analyzing relationships between variables (e.g., price vs. sold).

Examining the distribution of product tags.

Feature Engineering:

Transforming productTitle into numerical features using TF-IDF (Term Frequency-Inverse Document Frequency).

Model Selection & Training:

Splitting data into training and testing sets.

Training two regression models:

Linear Regression

Random Forest Regressor

Model Evaluation:

Assessing model performance using Mean Squared Error (MSE) and R-squared (R^2) metrics on the test set.

Setup and Installation
To run this project, you'll need Python and the following libraries. It's recommended to use a virtual environment.

Clone the repository:

git clone <your-repository-url>
cd <your-repository-name>

Create a virtual environment (optional but recommended):

python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

Install dependencies:

pip install pandas numpy seaborn matplotlib scikit-learn

Download the dataset:
Ensure the ecommerce_furniture_dataset_2024.csv file is placed in the root directory of your project.

How to Run
The code is structured into sequential blocks, ideal for execution in a Jupyter Notebook or similar interactive environment.

Start Jupyter Notebook:

jupyter notebook

Open the notebook file (e.g., ecommerce_sales_prediction.ipynb if you save the blocks into one file).

Execute each code cell sequentially from Block 1 to Block 9.

Results and Conclusion
The models were evaluated using Mean Squared Error (MSE) and R-squared (R^2).

Linear Regression: MSE: [MSE Value], R2: [R2 Value]

Random Forest Regressor: MSE: [MSE Value], R2: [R2 Value]

(Note: Replace [MSE Value] and [R2 Value] with the actual output from your model evaluation block.)

Both models exhibited poor performance, indicated by negative R-squared values. This suggests that the current features and models are not effectively capturing the underlying patterns in the sold data. The target variable (sold) is highly skewed, which poses a significant challenge for standard regression models.

Future Improvements
To enhance model performance, consider the following:

Target Variable Transformation: Apply transformations like np.log1p() to the sold column to handle its skewed distribution.

Advanced Feature Engineering:

Explore more sophisticated NLP techniques for productTitle (e.g., word embeddings).

Create interaction terms between existing features.

Incorporate external data (e.g., seasonality, marketing spend, customer reviews).

Author - Ashhar04
Hyperparameter Tuning: Optimize model parameters using techniques like GridSearchCV or RandomizedSearchCV.

Explore Other Models: Experiment with more robust models such as XGBoost, LightGBM, or deep learning architectures.

Outlier Analysis: Investigate and handle outliers in numerical features.

Error Analysis: Analyze where the models make the largest errors to gain insights.
