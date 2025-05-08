# 🚀 Predicting Start-up Success and Failure

This project analyzes U.S. startup data to predict whether a company will succeed, fail using features like founding date, funding history, and website presence.


---

## 🧠 Project Overview

- 🎯 **Goal**: Predict startup outcome (operating, closed, acquired)
- 🧰 **Tech Stack**: Python, pandas, seaborn, scikit-learn, XGBoost
- 📦 **Features Used**: Funding amount, rounds, company age, website status
- ⚖️ **Imbalance Handling**: `class_weight='balanced'` (RF), `scale_pos_weight` (XGBoost)

---

## 🧹 Feature Engineering

- `company_age`: Company lifetime (in years)
- `funding_density`: Total funding / (rounds + 1)
- `founded_at_missing`: Whether founding date is missing
- `funding_gap_days`: Time between first and last funding
- `has_website`: Binary feature for website presence

---

## 📊 Exploratory Data Analysis (EDA)

### 1. Startup Status Distribution by Category
> Shows top 10 startup categories with their success, operating, and failure distribution.
<img src="project1/Categories by Status Group.png" width="700"/>

### 2. Funding Total by Status Group
> Total funding amount grouped by startup outcome.
<img src="project1/Funding Total USD by Startup Status Group.png" width="700"/>

### 3. Global Distribution of Startups
> The U.S. leads globally in number of startups, followed by other key regions.
<img src="project1/Global dis.png" width="700"/>

---

## 🤖 Model Training & Evaluation

### Models Used

- **Random Forest Classifier**
  - Handles class imbalance via `class_weight="balanced"`
  - Feature importance analysis per target class
- **XGBoost Classifier**
  - Uses `scale_pos_weight` to boost minority class
  - Multi-class classification with `softprob` output

---

## 📌 Feature Importance

### 1. Random Forest - All Features
<img src="project1/Feature Importance for Predicting Multiclass classification (rf).png" width="700"/>
### 2. XGBoost - All Features
<img src="project1/Feature Importance for Predicting Multiclass classification (xgb).png" width="700"/>

### 3. Random Forest - Success Class
<img src="project1/Feature Importance for Success (rf).png" width="700"/>
### 4. XGBoost - Success Class
<img src="project1/Feature Importance for Success (xgb).png" width="700"/>

### 5. Random Forest - Failure Class
<img src="project1/Feature Importance for Failure (rf).png" width="700"/>
### 6. XGBoost - Failure Class
<img src="project1/Feature Importance for Failure (xgb).png" width="700"/>

---

## 📁 Files

- `Project01.ipynb`: Full notebook with all analysis and modeling
- `project1/`: Folder containing all visual outputs
- `README.md`: You’re reading it

---

## ▶️ How to Run

```bash
git clone https://github.com/Chiaohsinch/Predicting-Start-up-Success-and-Failure.git
cd Predicting-Start-up-Success-and-Failure
jupyter notebook Project01.ipynb
