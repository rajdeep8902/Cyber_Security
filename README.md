
# 🔐 Malicious File Severity Prediction using Machine Learning

This project aims to predict the **severity** of malicious files using structured data extracted from JSON files. The data was initially processed and analyzed with the help of ChatGPT, and further used to train various machine learning models. This work combines concepts of **cybersecurity**, **data preprocessing**, and **machine learning classification**.

## 📁 Dataset

The dataset (`output.csv`) was derived from JSON reports containing metadata about files. It includes features like:
- `md5`, `sha1`, `sha256`: File hashes
- `file_type`, `file_size`
- `tags`, `tlp`, `score`, `severity`
- Various AV (Antivirus) and behavioral signatures

> The target variable is `severity` — a label indicating the threat level of the file.

## 🧠 ML Models Used

The following supervised learning models were trained and evaluated:
- ✅ **Support Vector Machines (SVM)**
- ✅ **Random Forest**
- ✅ **XGBoost Classifier**
- ✅ **Decision Tree**
- ✅ **K-Nearest Neighbors (KNN)**
- ✅ **Logistic Regression**

Each model was evaluated using:
- Accuracy
- Precision, Recall, F1-Score
- Confusion Matrix
- Feature Importance (for interpretability)

## 🔄 Workflow

1. **Data Cleaning & Preprocessing**
   - Removed irrelevant or duplicate columns
   - Encoded categorical variables
   - Handled missing values
   - Feature selection

2. **Model Training**
   - Split dataset into training and testing sets (e.g., 80-20)
   - Applied standardization where required
   - Trained and tuned multiple classifiers

3. **Evaluation**
   - Plotted confusion matrices
   - Compared performance metrics across models
   - Selected best-performing model based on accuracy and generalization

## 📊 Results

- Best accuracy achieved: **`86%`** using **`Bagging Ensemble with SVM`**
- Key features affecting severity prediction were: `score`, `tags`, `file_type`, and AV detections.

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/malicious-file-severity-ml.git
   cd malicious-file-severity-ml
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

## 🛠 Tech Stack

- Python 3
- Jupyter Notebook
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn

## 📌 Key Takeaways

- Severity of malicious files can be predicted effectively using metadata-based features.
- XGBoost and Random Forest generally offer the best performance for such classification tasks.
- Feature engineering and data cleaning significantly influence model performance.

