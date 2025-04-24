# 📧 Email Classification & PII Masking API

A deep learning-based project that classifies IT service emails (e.g., **Incident**, **Request**, **Change**) while protecting user privacy by masking and restoring sensitive **Personally Identifiable Information (PII)**. Built with **TensorFlow**, **FastAPI**, and **spaCy**.

---

## 🔍 Features

- ✅ Classifies emails into Incident, Request, or Change
- 🔐 Detects and masks PII (Email, Phone, Aadhar, etc.) using regex + NLP
- 🔁 Restores original PII after classification
- 🧠 LSTM-based model with tokenizer and label encoder
- ⚡ FastAPI for real-time prediction API

---

## 🧠 Model Overview

| Attribute     | Details                          |
|---------------|----------------------------------|
| **Model Type**| Bidirectional LSTM (Keras)       |
| **Input**     | Combined email subject & body    |
| **Output**    | Email Type (incident/request/...)|
| **Accuracy**  | ~70% (tunable to 85%+)           |
| **Dataset**   | 24,000 labeled support emails    |

---

## 🗂 Project Structure

# 📧 Email Classification & PII Masking API

A deep learning-based project that classifies IT service emails (e.g., **Incident**, **Request**, **Change**) while protecting user privacy by masking and restoring sensitive **Personally Identifiable Information (PII)**. Built with **TensorFlow**, **FastAPI**, and **spaCy**.

---

## 🔍 Features

- ✅ Classifies emails into Incident, Request, or Change
- 🔐 Detects and masks PII (Email, Phone, Aadhar, etc.) using regex + NLP
- 🔁 Restores original PII after classification
- 🧠 LSTM-based model with tokenizer and label encoder
- ⚡ FastAPI for real-time prediction API

---

## 🧠 Model Overview

| Attribute     | Details                          |
|---------------|----------------------------------|
| **Model Type**| Bidirectional LSTM (Keras)       |
| **Input**     | Combined email subject & body    |
| **Output**    | Email Type (incident/request/...)|
| **Accuracy**  | ~70% (tunable to 85%+)           |
| **Dataset**   | 24,000 labeled support emails    |

---

## 🗂 Project Structure
- app.py (or equivalent main script)
- Requirements file (requirements.txt or environment.yml)
- README with setup and usage instructions
- models.py containing the model training and utility functions
- utils.py containing the utility function and code
- api.py to support the development of APIs.



---

## ⚙️ Setup Instructions

# 1. Clone the repo
git clone https://github.com/yourusername/email-classifier-pii-api.git
cd email-classifier-pii-api

# 2. Create and activate virtual environment
conda create -n email_env python=3.10
conda activate email_env

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the API
uvicorn main:app --reload


# Sample API Request & Response
 
✅ Request
json

{
  "email": "Subject: Reset access\nPlease reset my credentials. Email: john.doe@example.com, Phone: 9876543210"
}
✅ Response
json

{
  "masked_email": "Subject: Reset access\nPlease reset my credentials. Email: [EMAIL_1], Phone: [PHONE_1]",
  "classification": "incident",
  "original_entities": {
    "EMAIL_1": "john.doe@example.com",
    "PHONE_1": "9876543210"
  }
}
# Model Training
To train or retrain the model:
python models.py

Trains the LSTM classifier and saves the model to model/email_classifier_model.h5.

# 🛠 Tech Stack
Python 3.10

TensorFlow / Keras

FastAPI

spaCy (NLP for PII detection)

Regex for pattern-based masking

scikit-learn (LabelEncoder)


