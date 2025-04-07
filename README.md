# 🎬 Netflix Show Type Prediction - ML Model

This project aims to predict whether a Netflix title is a **Movie** or a **TV Show** using machine learning techniques. It involves data cleaning, preprocessing, visualization, model training, and evaluation on a cleaned Netflix dataset.

---

## 📁 Dataset Overview

The dataset contains information about Netflix titles, including:
- `title`, `director`, `cast`, `country`
- `date_added`, `release_year`, `duration`
- `rating`, `listed_in`, and `description`

**Total Records:** 7787  
**Original Columns:** 12  
**Used Features:** Cleaned and engineered versions of the above columns.

---

## 🧹 Data Cleaning Tasks

Thorough cleaning was performed to prepare the data for modeling:

### 🔧 1. Handling Missing Values
- `director`, `cast`, `country`, and `rating` had missing values filled with `"Unknown"` or mode where appropriate.
- `date_added`: Missing values filled using forward fill method.

### 🔁 2. Removing Duplicates
- Removed duplicate entries using `.drop_duplicates()` to avoid data redundancy.

### 🧼 3. Column Standardization
- Converted all column names to lowercase with underscores instead of spaces.
- Removed special characters and ensured uniform naming.

### 📅 4. Date Formatting
- Converted `date_added` to `datetime` format.
- Extracted `year_added` and `month_added` from the date for temporal analysis.

### ⏱️ 5. Duration Column Cleaning
- `duration` split into `duration_int` and `duration_type` (e.g., 90 minutes → `90`, `minutes`).
- Ensured consistent formatting across duration values.

### 🌐 6. Text & Categorical Cleanup
- Trimmed and normalized text fields like `country`, `rating`, and `listed_in`.
- Ensured no trailing spaces or case inconsistencies.

### 🔣 7. Encoding Categorical Features
- Applied One-Hot Encoding on `country`, `rating`, `listed_in`, and `duration_type`.
- Label Encoding applied for target column `type` (Movie = 0, TV Show = 1).

### 📏 8. Feature Scaling
- Used `StandardScaler` to normalize numerical features (e.g., `duration_int`, `release_year`).

---

## 🛠️ Tech Stack

- **Python**
- **Pandas**, **NumPy** for data manipulation
- **Matplotlib**, **Seaborn** for visualization
- **Scikit-learn** for preprocessing, modeling, and evaluation

---

## 📊 Exploratory Data Analysis (EDA)

Visual insights include:
- Count of Movies vs TV Shows
- Top 10 Countries Producing Content
- Content Release Trends
- Genre and Rating Distribution

---

## 🤖 ML Model: Random Forest Classifier

- **Target:** `type` (0 = Movie, 1 = TV Show)
- **Train/Test Split:** 80/20
- **Accuracy:** ~XX% (depends on model run)
- **Feature Importance:** Visualized top contributing features

### 🔍 Evaluation Metrics
- Accuracy Score
- Precision, Recall, F1 Score
- Confusion Matrix

---

## 📌 Usage

1. Clone this repo or open it in Google Colab.
2. Upload `cleaned_netflix_dataset.csv`.
3. Run the notebook step-by-step to:
   - Explore the data
   - Train the model
   - Predict & Evaluate

---
