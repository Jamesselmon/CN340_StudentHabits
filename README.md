# Student Habits vs. Academic Performance Analysis

### Prerequisites
- Python 3.x
- Jupyter Notebook or Google Colab
- Kaggle account and API credentials

### Required Libraries
```
pandas
numpy
matplotlib
seaborn
scikit-learn
kaggle
```

### Step-by-Step Instructions

1. **Set up Kaggle API credentials**
   ```python
   from google.colab import userdata
   import os
   
   os.environ["KAGGLE_KEY"] = userdata.get('KAGGLE_KEY')  # or your actual Kaggle key
   os.environ["KAGGLE_USERNAME"] = userdata.get('KAGGLE_USERNAME')  # or your actual username
   ```

2. **Download and extract the dataset**
   ```python
   !kaggle datasets download -d jayaantanaath/student-habits-vs-academic-performance
   !unzip "student-habits-vs-academic-performance"
   ```

3. **Load and explore the dataset**
   ```python
   import pandas as pd
   
   df = pd.read_csv('student_habits_performance.csv')
   print("Dataset shape:", df.shape)
   print("\nData types:")
   print(df.dtypes)
   print("\nMissing values per column:")
   print(df.isnull().sum())
   ```

4. **Run the exploratory data analysis (EDA) section**
   - This generates visualizations for exam score distribution
   - Creates correlation matrix and scatterplots
   - Produces boxplots for categorical variables

5. **Execute the data preprocessing section**
   - Handles missing values
   - Separates features and target
   - Sets up preprocessing pipelines for numerical and categorical data
   - Splits data into training and testing sets

6. **Run the model implementation and evaluation sections**
   - Trains both Linear Regression and Random Forest models
   - Evaluates models using RMSE, MAE, R² and cross-validation
   - Analyzes feature importance
   - Compares model performance with visualizations

### Expected Output
- Summary statistics of the dataset
- Visual plots of exam score distributions and feature relationships
- Model performance metrics for both Linear Regression and Random Forest
- Feature importance ranking from the Random Forest model
- Comparative visualization of model performance
