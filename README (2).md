
# 📰 Fake News Detection Chatbot Using Transformer

This project provides an intelligent chatbot that classifies news as **"fake"** or **"true"** using a transformer-based model.

---

## 📌 Project Objective

To build and deploy an AI-driven conversational system that can classify news articles in real-time.

---

## ⚙️ How the Code Works

The machine learning pipeline is designed to accurately distinguish between fake and true news articles through the following stages:

### 1. 📂 Data Loading and Preprocessing

- Load `true.csv` and `fake.csv` datasets.
- Preprocess the text: remove special characters, lowercase, and tokenize.
- Convert the cleaned tokens into numerical format suitable for transformer models.

### 2. 🤖 Model Training

- Utilize a transformer model such as BERT or DistilBERT.
- Train the model on labeled data (`True` or `Fake`) to detect patterns and context.
- Save the trained model and tokenizer for later inference.

### 3. 🚀 Model Deployment via Streamlit

- A Streamlit app (`app.py`) provides a chatbot-style interface.
- User inputs are processed and classified using the trained model.
- Output: Classification result — "Fake" or "True" — is shown instantly.

---

## 🗃️ Data

The following datasets are used for training:

- `true.csv` – Contains genuine news articles.
- `fake.csv` – Contains fake/misinformation news articles.

---

## 🧰 Setup and Installation

### 🔧 Prerequisites

- Python 3.8 or higher
- pip package manager

### 📦 Installation (Recommended in Virtual Environment)

Install dependencies with:

```bash
pip install pandas scikit-learn transformers torch streamlit pyngrok wordcloud matplotlib
```

> 📌 Ensure `true.csv` and `fake.csv` are in the root project directory if not using Colab.

---

## ▶️ Running the Project

### 🧪 Step 1: Data Preparation & Model Training

1. Place `true.csv` and `fake.csv` in your project folder.
2. Open `FAKE_NEWS_DETECTION_USING_TRANSFORMERS.ipynb` (Jupyter Notebook).
3. Execute all notebook cells to:
   - Preprocess data
   - Train transformer model
   - Save the model and tokenizer (e.g., `saved_model/`, `tokenizer/`)

---

### 💬 Step 2: Running the Chatbot via Streamlit

#### ✅ Locally (On Your PC)

1. Ensure `app.py` exists and is configured to load the saved model and tokenizer.
2. From the terminal, run:

```bash
streamlit run app.py
```

3. The chatbot will open in your browser at:  
   `http://localhost:8501`

---

#### 🌐 In Google Colab (with Public Shareable Link)

1. Add your [ngrok authtoken](https://dashboard.ngrok.com/get-started/setup) to the Colab notebook:

```python
!ngrok authtoken YOUR_AUTHTOKEN_HERE
```

2. Run the cell that launches the Streamlit app via pyngrok:

```python
!streamlit run app.py & npx localtunnel --port 8501
```

3. You'll receive a public URL like `https://xyz.loca.lt` — you can share this link with others.

---

## 🧠 Usage

- Open the app and input a news paragraph or sentence.
- Click **Submit**.
- The chatbot will respond with a prediction:  
  🔹 **True** – likely real news  
  🔹 **Fake** – likely misinformation

---

## 📎 Notes

- Built using HuggingFace Transformers and Streamlit.
- Easily extendable to other languages or news domains.
- Ideal for learning NLP classification, fine-tuning transformers, and rapid prototyping with Streamlit.

---

## 📁 Project Structure (Sample)

```
├── app.py
├── true.csv
├── fake.csv
├── saved_model/
├── tokenizer/
├── FAKE_NEWS_DETECTION_USING_TRANSFORMERS.ipynb
└── README.md
```

---

## 📫 Contact

For questions, feedback, or collaboration ideas, feel free to open an issue or reach out. Contact me at sayanmondalhs1433@gmail.com

