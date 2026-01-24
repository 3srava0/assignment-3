# assignment-3
Real Estate Investment Advisor - ML-powered property investment analysis and recommendation system using Google Colab and Hugging Face datasets

## 🗓️ 7-Day Project Timeline

### Day 1: Environment Setup & Exploratory Data Analysis (EDA)
**Status**: ✅ In Progress

#### Tasks
1. ✅ **GitHub Repository Setup**
   - Repository created: `assignment-3`
   - Initial commit with README, .gitignore (Python), and MIT License
   - Repository structure planned

2. 🔄 **Google Colab Environment Setup**
   ```python
   # Install required packages
   !pip install pandas numpy matplotlib seaborn plotly
   !pip install scikit-learn xgboost lightgbm
   !pip install datasets  # Hugging Face datasets
   !pip install mlflow
   !pip install shap
   ```

3. 🔄 **Dataset Loading from Hugging Face**
   ```python
   from datasets import load_dataset
   
   # Option 1: Load from Hugging Face Hub (if public)
   # dataset = load_dataset('your-username/india-housing-prices')
   
   # Option 2: Load from local file and create dataset
   from datasets import Dataset
   import pandas as pd
   df = pd.read_csv('india_housing_prices.csv')
   dataset = Dataset.from_pandas(df)
   ```

4. 🔄 **Exploratory Data Analysis**
   - Dataset overview (shape, columns, dtypes)
   - Missing value analysis
   - Statistical summary
   - Distribution analysis (20+ visualizations)
   - Correlation heatmap
   - Outlier detection
   - Feature relationships

#### Deliverables
- ✅ GitHub repo initialized
- 🔄 Colab notebook: `01_EDA_and_Data_Cleaning.ipynb`
- 🔄 Clean dataset saved
- 🔄 EDA report with 20+ visualizations

---

### Day 2: Feature Engineering
**Status**: ⏳ Pending

#### Tasks
1. Create 15+ new features
2. Handle missing values
3. Encode categorical variables
4. Feature scaling/normalization
5. Create target variables (classification & regression)
6. Train-test split

#### Deliverables
- Notebook: `02_Feature_Engineering.ipynb`
- Processed dataset with engineered features
- Feature documentation

---

### Day 3: Model Training
**Status**: ⏳ Pending

#### Tasks
1. Set up MLflow tracking
2. Train 4 classification models
3. Train 4 regression models
4. Log metrics to MLflow
5. Compare model performance

#### Deliverables
- Notebook: `03_Model_Training.ipynb`
- 8 trained models
- MLflow experiment logs
- Performance comparison report

---

### Day 4: Hyperparameter Tuning
**Status**: ⏳ Pending

#### Tasks
1. Grid/Random search for top models
2. Cross-validation
3. Fine-tune best models
4. Final model selection

#### Deliverables
- Notebook: `04_Hyperparameter_Tuning.ipynb`
- Optimized models
- Tuning results

---

### Day 5: Prediction Pipeline & Explainability
**Status**: ⏳ Pending

#### Tasks
1. Create prediction functions
2. SHAP explanations
3. Confidence intervals
4. Pipeline testing

#### Deliverables
- Module: `predictor.py`
- Notebook: `05_Prediction_and_SHAP.ipynb`
- SHAP visualizations

---

### Day 6: Streamlit App Development
**Status**: ⏳ Pending

#### Tasks
1. Create multi-page Streamlit app
2. Prediction interface
3. Analytics dashboard
4. Property comparison tool
5. Model explanation page

#### Deliverables
- `streamlit_app.py`
- `requirements.txt`
- App screenshots

---

### Day 7: Testing & Deployment
**Status**: ⏳ Pending

#### Tasks
1. Write unit tests
2. Integration testing
3. Deploy to Streamlit Cloud
4. Final documentation
5. GitHub release (v1.0.0)

#### Deliverables
- Test files
- Live Streamlit app URL
- Complete documentation
- Final GitHub commit

---

## 📁 Repository Structure

```
assignment-3/
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
├── notebooks/
│   ├── 01_EDA_and_Data_Cleaning.ipynb
│   ├── 02_Feature_Engineering.ipynb
│   ├── 03_Model_Training.ipynb
│   ├── 04_Hyperparameter_Tuning.ipynb
│   └── 05_Prediction_and_SHAP.ipynb
├── src/
│   ├── predictor.py
│   ├── preprocessing.py
│   └── utils.py
├── streamlit_app.py
├── tests/
│   ├── test_preprocessing.py
│   └── test_prediction.py
└── data/              # Excluded from git
    └── sample_100rows.csv  # Small sample for testing
```

---

## 🛠️ Tech Stack

- **Development**: Google Colab (free GPU/TPU)
- **Dataset**: Hugging Face Datasets
- **ML Libraries**: scikit-learn, XGBoost, LightGBM
- **Experiment Tracking**: MLflow
- **Explainability**: SHAP
- **Deployment**: Streamlit Cloud
- **Version Control**: GitHub

---

## 📊 Dataset Information

**Source**: GUVI - India Housing Prices
- Dataset is **not publicly redistributable** as per GUVI terms
- Dataset stored separately (private Hugging Face repo or Google Drive)
- Small sample (100 rows) included for testing only

### How to Get the Dataset
1. Enrolled learners: Download from GUVI platform
2. Others: Contact GUVI or use alternative housing datasets

---

## 🚀 Quick Start

### Option 1: Google Colab (Recommended for Day 1-5)
1. Open Google Colab
2. Clone this repo:
   ```python
   !git clone https://github.com/3srava0/assignment-3.git
   %cd assignment-3
   ```
3. Install dependencies:
   ```python
   !pip install -r requirements.txt
   ```
4. Upload your dataset to Colab or mount Google Drive

### Option 2: Local Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/3srava0/assignment-3.git
   cd assignment-3
   ```
2. Create virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## 📝 Commit Guidelines

Following conventional commits:
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `chore:` Maintenance

Example: `feat: add EDA notebook with 20+ visualizations`

---

## ⚠️ Limitations & Solutions

### 1. Dataset Size & GitHub Limits
**Limitation**: GitHub has 100 MB file limit
**Solution**: 
- Store full dataset on Hugging Face (private repo) or Google Drive
- Only commit small sample CSV (100 rows) to GitHub
- Add download instructions in README

### 2. Dataset Licensing
**Limitation**: GUVI dataset may not allow public redistribution
**Solution**:
- Keep dataset in private Hugging Face repo
- Or don't push dataset to GitHub at all
- Provide clear instructions on how to obtain dataset

### 3. Model File Sizes
**Limitation**: Trained models can be 100+ MB
**Solution**:
- Don't commit model binaries to GitHub
- Use reproducible training code instead
- Or use Git LFS for large files
- Or upload models to Hugging Face Hub

### 4. Reproducibility
**Limitation**: Different environments may produce different results
**Solution**:
- Pin exact library versions in `requirements.txt`
- Document Python version (3.9+)
- Set random seeds in code
- Provide Colab notebooks for exact environment

---

## 📫 Contact

Created by [@3srava0](https://github.com/3srava0)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
