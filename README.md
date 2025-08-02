
# 💼 Customer Churn Prediction App (ANN + Streamlit)

This project is a **Streamlit-based web application** that predicts the probability of a bank customer churning using an **Artificial Neural Network (ANN)** model. The model is trained on historical customer data and deployed for real-time prediction via a user-friendly interface.

---

## 📊 Features

- Predicts customer churn probability with a trained ANN model.
- Accepts input features like geography, gender, age, balance, credit score, etc.
- Performs data preprocessing using `LabelEncoder`, `OneHotEncoder`, and `StandardScaler`.
- Real-time probability output with business logic insights:
  - Shows likelihood of churn.
  - Actionable insight for customer retention.

---

## 🧠 Model Details

- Built using **TensorFlow**.
- Pre-trained ANN model stored as `model.h5`.
- Encoders and scaler saved using `pickle`:
  - `label_encoder_gender.pkl`
  - `onhot_encoder_geo.pkl`
  - `scaler.pkl`

---

## 🛠 Tech Stack

| Layer           | Tools / Libraries                            |
|----------------|-----------------------------------------------|
| Frontend        | Streamlit                                     |
| Model           | TensorFlow (ANN)                              |
| Preprocessing   | scikit-learn (`LabelEncoder`, `OneHotEncoder`, `StandardScaler`) |
| Backend         | Python, Pandas, NumPy                         |

---

## 📥 Inputs

The user can adjust the following inputs via the web UI:

- **Geography** (Dropdown: e.g., France, Germany, Spain)
- **Gender** (Male/Female)
- **Age** (18–92)
- **Credit Score**
- **Balance**
- **Estimated Salary**
- **Tenure** (Years with bank)
- **Number of Products**
- **Has Credit Card** (0 or 1)
- **Is Active Member** (0 or 1)

---

## 📤 Output

- **Churn Probability** (0.00–1.00)
- **Churn Likelihood Status**:
  - `> 0.5` → “The Customer is likely to churn”
  - `<= 0.5` → “Customer is not likely to churn”

---

## 🧑‍💻 How to Run Locally

1. **Clone this repository**

   ```bash
   git clone https://github.com/yourusername/churn-prediction-ann.git
   cd churn-prediction-ann
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Streamlit app**

   ```bash
   streamlit run app.py
   ```

---

## 📂 File Structure

```
.
├── app.py                       # Streamlit application
├── model.h5                     # Trained ANN model
├── scaler.pkl                   # StandardScaler object
├── label_encoder_gender.pkl     # LabelEncoder for Gender
├── onhot_encoder_geo.pkl        # OneHotEncoder for Geography
├── README.md                    # Project documentation
└── requirements.txt             # Python dependencies
```

---

## ✅ Sample Use Case

This app can be used by customer retention teams in banks or fintech companies to:

- Proactively identify high-risk customers.
- Trigger personalized retention strategies.
- Monitor churn metrics over time.

---

## 📌 Future Improvements

- Upload CSV for batch predictions.
- Visualize feature importance.
- Deploy on cloud (e.g., Streamlit Cloud, AWS).

---

## 🙌 Acknowledgments

Inspired by industry use cases in customer churn prediction. Model design and deployment influenced by real-world telecom/banking datasets.
