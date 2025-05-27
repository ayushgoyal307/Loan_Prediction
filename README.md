# 🏦 Loan Approval Prediction using Decision Tree

This project uses a Decision Tree Classifier to predict whether a loan will be approved based on various applicant features such as income, credit history, education, etc.

## 📁 Dataset

- File: `train.csv`
- Columns include: `Gender`, `Married`, `Dependents`, `Education`, `Self_Employed`, `ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`, `Loan_Amount_Term`, `Credit_History`, `Property_Area`, `Loan_Status`, and more.
- The target variable is **Loan_Status** (`Y` = Approved, `N` = Not Approved).

## 🧠 Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Google Colab (for uploading and running code)

## ⚙️ How it Works

1. Upload the `train.csv` file.
2. The dataset is cleaned:
   - Drops `Loan_ID`
   - Fills missing values
   - Encodes categorical variables using `LabelEncoder`
3. Splits the data into training and testing sets.
4. Trains a `DecisionTreeClassifier` with a max depth of 4.
5. Evaluates the model using accuracy, confusion matrix, and classification report.
6. Plots feature importance.
7. Allows **user input** to predict loan approval using the trained model.

## 📊 Evaluation

- **Accuracy**, **Confusion Matrix**, and **Classification Report** are displayed after training.
- A **feature importance graph** helps understand which features influence loan approval most.

## 🔮 Make Your Own Prediction

The model includes a function `predict_from_input()` where you can manually enter details like:

- Gender
- Married status
- Number of Dependents
- Education
- Employment status
- Income
- Credit history
- Property area

The model will return whether the loan will be approved or not.

## 🚀 Running the Code in Google Colab

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Copy-paste the code into a cell.
3. Run the cell to upload `train.csv` and start the process.
4. Enter input values when prompted to make a prediction.

## 📌 Sample Usage

```python
from google.colab import files
uploaded = files.upload()

# Followed by:
df = pd.read_csv(io.BytesIO(uploaded['train.csv']))
