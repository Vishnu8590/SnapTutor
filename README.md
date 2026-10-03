# SnapTutor 📚 - AI Visual Study Assistant

> **Your AI study tutor, one snap away.** Snap a photo of a textbook, handwritten note, math problem, diagram, or code snippet, and get instant, step-by-step explanations.

---

## ✨ Features

- 📸 **Multimodal Image Analysis**: Upload images of textbook pages, handwritten notes, math equations, coding bugs, diagrams, or MCQs.
- 🧠 **Step-by-Step AI Tutoring**: Powered by Google Gemini (`google-genai`) to provide intuitive, beginner-friendly explanations without just giving away answers.
- 💬 **Interactive Study Chat**: Ask follow-up questions, request practice questions, or drill down on confusing concepts in real-time.
- 📤 **WhatsApp Study Summaries**: Generates a quick revision summary of your study session and delivers it directly to your WhatsApp via Twilio.
- 🔒 **Secure Secrets Management**: Keeps sensitive API keys protected with Streamlit secrets.

---

## 🛠️ Tech Stack

- **Frontend / UI**: [Streamlit](https://streamlit.io/)
- **AI / LLM**: [Google GenAI SDK](https://github.com/googleapis/python-genai) (Gemini)
- **Messaging API**: [Twilio REST API](https://www.twilio.com/docs/whatsapp) (WhatsApp Messaging)
- **Language**: Python 3.10+

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Vishnu8590/SnapTutor.git
cd SnapTutor
```

### 2. Create and Activate a Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## ⚙️ Configuration

Create a `.streamlit/secrets.toml` file in the root directory and add your API credentials:

```toml
GEMINI_API_KEY = "your_google_gemini_api_key"
TWILIO_ACCOUNT_SID = "your_twilio_account_sid"
TWILIO_AUTH_TOKEN = "your_twilio_auth_token"
TWILIO_WHATSAPP_FROM = "+14155238886"  # Twilio WhatsApp sandbox number
TWILIO_CONTENT_SID = "your_twilio_content_sid"
```

> **Note**: Never commit `.streamlit/secrets.toml` or `.env` to Git. They are ignored by default in `.gitignore`.

---

## 💻 Running the App

Start the Streamlit application:

```bash
streamlit run app.py
```

Open `http://localhost:8501` in your browser, enter your name and WhatsApp number, and start studying!

---

## 📁 Project Structure

```text
SnapTutor/
├── .streamlit/
│   └── secrets.toml        # Local API credentials (ignored in git)
├── .gitignore              # Git ignore rules
├── app.py                  # Main Streamlit application and Twilio integration
├── prompts.py              # System prompt and conversational templates
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
