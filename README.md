AutoEDA is a simple, reusable Python class that automates the most common steps in exploratory data analysis and preprocessing.
It helps data analysts and data scientists quickly clean and prepare data for machine learning or analytics tasks — with just a few lines of code.

✅ Load data from CSV or directly from a pandas DataFrame
🔍 Data profiling: summaries, types, descriptive stats, and missing values
🧹 Missing value handling: drop or impute with median/mode
📈 Outlier detection & handling: identify and cap IQR-based outliers
🧠 Label encoding for categorical variables
📏 Standard scaling for numerical features
💾 Save cleaned data to a new CSV file
⚠️ Graceful error handling (optional: add try/except for robustness)

from auto_eda import AutoEDA  # assuming you've saved it as auto_eda.py

# Option 1: Load from CSV
eda = AutoEDA(filepath="your_data.csv")

# Option 2: Load from existing DataFrame
# eda = AutoEDA(dataframe=your_dataframe)

eda.profile()             # Basic info, describe, missing values
eda.handle_missing()      # Drop/impute missing values
eda.detect_outliers()     # Print number of outliers per column
eda.handle_outliers()     # Cap outliers using IQR method
eda.encode_categoricals() # Label encode categorical columns
eda.scale_numeric()       # Standard scale numerical columns
eda.save_cleaned()        # Save final cleaned data to CSV
