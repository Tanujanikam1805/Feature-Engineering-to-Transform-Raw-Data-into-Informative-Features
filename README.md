## ⚙️ Feature Engineering Steps

### **1. Data Loading and Exploration**
- Loaded the dataset using `pandas`.
- Displayed the first few rows, data types, shape, and checked for missing values.
- This helped understand which features were numeric or categorical.

### **2. Handling Missing Data**
- **Numeric Columns:** Replaced missing values with the **mean**.  
- **Categorical Columns:** Filled missing values with the **mode (most frequent value)**.  
- Ensured there were no null values left after cleaning.

### **3. Encoding Categorical Variables**
- Used **One-Hot Encoding** via `pd.get_dummies()` for categorical columns (if any).  
- This converted text data into numeric form for modeling.

### **4. Feature Scaling**
- Applied **Standardization** using `StandardScaler` to normalize numeric features.  
- This ensures all features have a similar scale and improves model performance.

### **5. Feature Extraction (PCA)**
- Used **Principal Component Analysis (PCA)** to reduce dimensionality and extract key components.  
- Two main principal components (PCA1 and PCA2) were created to capture most of the variance in data.

### **6. Feature Selection**
- Applied **Variance Threshold** to remove low-variance features.  
- Used **SelectKBest** (with `f_regression`) to select the top 5 most important numerical features related to the target variable.
