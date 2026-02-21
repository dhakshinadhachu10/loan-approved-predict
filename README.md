📌 Loan Approved Prediction
📖 Project Overview
Loan Approved Prediction is a Machine Learning project that predicts whether a loan application will be approved or not based on applicant details.
The model uses Logistic Regression to classify loan applications into two categories:
✅ Loan Approved
❌ Loan Not Approved

This project demonstrates the complete ML workflow including:

Data preprocessing

Encoding categorical variables

Train-test splitting

Model training

Model evaluation

🛠️ Technologies Used

Python

Pandas

Scikit-learn

Google Colab (for development)

📂 Dataset

The dataset used in this project (loanapproval.csv) contains applicant information such as:

Gender

Marital Status

Employment Status

Other financial details

Loan Approval Status (Target Variable)

Target Column:

loan_approved
⚙️ Project Workflow
1️⃣ Import Libraries

The following libraries are used:

pandas

sklearn.preprocessing

sklearn.model_selection

sklearn.linear_model

sklearn.metrics

2️⃣ Load Dataset

The dataset is loaded using:

df = pd.read_csv("/content/loanapproval.csv")
3️⃣ Data Preprocessing

✔ Checked for missing values

df.isnull().sum()

✔ Encoded categorical variables using LabelEncoder:

employment_status

gender

marital_status

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
4️⃣ Feature & Target Separation
x = df.drop("loan_approved", axis=1)
y = df["loan_approved"]
5️⃣ Train-Test Split

The dataset is split into:

80% Training Data

20% Testing Data

train_test_split(x, y, test_size=0.2)
6️⃣ Model Training

The model used:

🔍 Logistic Regression
from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(max_iter=500)
lr.fit(x_train, y_train)
7️⃣ Model Prediction
y_pred = lr.predict(x_test)
8️⃣ Model Evaluation

The model performance is evaluated using:

from sklearn.metrics import classification_report
classification_report(y_test, y_pred)

Evaluation Metrics:

Precision

Recall

F1-Score

Accuracy

📊 Output

The model predicts whether a loan will be approved or not based on applicant features.

Example Output:

[1 0 1 1 0 ...]

Where:

1 → Loan Approved

0 → Loan Not Approved

🚀 How to Run the Project

Install required libraries:

pip install pandas scikit-learn

Place loanapproval.csv in your working directory.

Run:

python loan approved prediction.py
🎯 Future Improvements

Add data visualization

Try other ML models (Decision Tree, Random Forest, SVM)

Hyperparameter tuning

Add model accuracy comparison
