# RozeePK-Jobs Market Analysis & Functional Area Prediction (2024)

This project analyzes the 2024 job dataset from Rozee.pk and applies machine learning techniques to predict job functional areas based on required skills. It includes extensive data cleaning, visualizations, profiling, and model building for practical insights into the Pakistani job market.

---

# Dataset

**File**: `RozeePK-Jobs-2024.csv`  
Contains real-world job postings from Rozee.pk for the year 2024, including fields like:

- Job Title, Salary, Job Location
- Required Skills
- Functional Area
- Minimum Experience, Education
- Gender Preference, Job Type, Career Level

---

# Project Structure

## 1. **Data Cleaning & Preprocessing**
- Handled missing values and inconsistent formatting.
- Cleaned and converted salary ranges into numeric PKR values.
- Standardized experience into numerical format (e.g., "Fresh" → 0).
- Extracted primary city names from locations.
- Parsed skills into lists for analysis.

## 2. **Exploratory Data Analysis (EDA)**
- Visualized:
  - Salary distribution
  - Job counts by city and job type
  - Top functional areas
  - Experience vs Salary relationship
  - In-demand skills and gender preferences
- Highlighted salary insights for specific skills.

## 3. **Data Profiling**
- Used `ydata-profiling` to generate an in-depth HTML profiling report.
- Explored correlations, distributions, missing values, etc.

## 4. **Machine Learning Models**

### Model 1: Functional Area Prediction (Multi-feature)
- **Input**: Combined features (Skills + Education + Experience + Career Level + Job Type)
- **Model**: `RandomForestClassifier`
- **Preprocessing**: `CountVectorizer` for feature vectorization
- **Label Encoding**: Functional Area classes

### Model 2: Functional Area Prediction (Skills Only)
- **Input**: Skills only
- **Vectorization**: `TF-IDF`
- **Model**: `RandomForestClassifier`
- **Accuracy**: Reported with `accuracy_score` and classification report
- **Use Case**: Predicts job functional area for new skill sets (e.g., "Machine Learning, Python")

## 5. **Skill Insights**
- Analyzed most frequent skills in demand across job postings.
- Visualized with bar chart and word cloud.

---

# Sample Insights

- **Top Cities for Jobs**: Karachi, Lahore, Islamabad
- **Top Functional Areas**: Software Development, Sales, HR, Marketing
- **Top In-Demand Skills**: Communication, Sales, JavaScript, PHP, Python
- **Salary Trends**:
  - `Laravel`: PKR 100,000/month
  - `Civil Engineering`: PKR 250,000/month
  - `Basic Sales`: PKR 35,000/month

---

# Example Predictions

predict_job_market_from_skills("Machine Learning Python Data Analysis")
# ➤ Software & Web Development

predict_job_market_from_skills("Search Engine Optimization Content Marketing")
# ➤ Marketing

predict_job_market_from_skills("Civil Engineering AutoCAD Project Management")
# ➤ Engineering
