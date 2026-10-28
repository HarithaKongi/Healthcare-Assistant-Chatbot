# 🩺 Healthcare Assistant Chatbot

A Streamlit-based health-information chatbot powered by the Groq API. It is designed to answer general health and wellness questions in clear language and to direct users to professional or emergency care when appropriate.

> **Medical disclaimer:** This project is for educational and informational purposes only. It does not diagnose conditions, replace a clinician, or provide individualized treatment. For urgent or potentially life-threatening symptoms, contact local emergency services immediately.

## Features

- 💬 Chat-style interface with temporary session history
- 🩺 Health-focused system instructions
- 🛡️ API key loaded from a local `.env` file or Streamlit Cloud Secrets
- 🔒 Secret files and local virtual environments excluded through `.gitignore`
- 🧹 Clear-chat control
- ⚠️ User-friendly handling of AI service errors

## Tech stack

- Python
- [Streamlit](https://streamlit.io/)
- [Groq API](https://console.groq.com/)
- `python-dotenv`

## Run locally

### 1. Clone the repository

```bash
git clone https://github.com/HarithaKongi/Healthcare-Assistant-Chatbot.git
cd Healthcare-Assistant-Chatbot
```

### 2. Create and activate a virtual environment

Windows:

```powershell
py -m venv .venv
.venv\Scripts\activate
```

macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure your API key

Create a local file named `.env` in the project root. You can copy `.env.example` and replace the placeholder with your own key from the [Groq Console](https://console.groq.com/).

```env
GROQ_API_KEY=your_actual_groq_api_key
```

**Never commit `.env` or share your API key.** The real key must stay in your local environment or deployment secrets.

### 5. Start the app

```bash
streamlit run app.py
```

Streamlit will print a local URL, usually `http://localhost:8501`.

## Deploy on Streamlit Community Cloud

1. Sign in at [Streamlit Community Cloud](https://share.streamlit.io/).
2. Choose **Create app** and select this GitHub repository.
3. Set the branch to `main` and the main file path to `app.py`.
4. Open the app's **Settings → Secrets** and add:

   ```toml
   GROQ_API_KEY = "your_actual_groq_api_key"
   ```

5. Save and wait for the deployment to finish. The public app URL will be provided by Streamlit after a successful deployment.

## Privacy and safety notes

- Do not enter identifying information or sensitive medical records into the chatbot.
- Conversation history is kept in Streamlit session state and is not a medical-record system.
- AI responses can be incomplete or inaccurate. Verify important information with a qualified healthcare professional.
- The app requires a valid Groq API key and network access to the Groq service.

## Project structure

```text
Healthcare-Assistant-Chatbot/
├── app.py
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

## Author

**Haritha Kongi**  
GitHub: [@HarithaKongi](https://github.com/HarithaKongi)

---

Built as an educational AI application.
