# 🩺 HealthCare AI Assistant

A healthcare chatbot rebuilt from a Class 12 AI project that looked cool in a demo and broke the moment you asked it a real question.

> ⚠️ **Informational only.** Not a medical device. Always consult a real doctor.

## What it does

- **💬 Chat** — multi-turn conversation, regenerate, voice input
- **🔍 Disease Prediction** — describe symptoms, get possible conditions + an urgency flag (Low / Medium / "see a doctor now")
- **📋 Treatment Plan** — enter a condition (optionally with height/weight for BMI-aware advice), download the plan as a PDF
- **🌐 Tanglish input** — understands Tamil typed in English, always replies in clear English
- **💡 Built-in glossary** — complex medical terms come with hover tooltips instead of a Google search

## Tech stack

- **[Gradio](https://gradio.app)** — UI
- **[Groq](https://groq.com)** — inference via `openai/gpt-oss-120b`
- **[Groq Whisper](https://console.groq.com/docs/speech-to-text)** (`whisper-large-v3-turbo`) — voice-to-text
- **[fpdf2](https://pypi.org/project/fpdf2/)** — PDF export

## Running it yourself

```bash
pip install gradio groq fpdf2
export GROQ_API_KEY="your-key-here"   # get one at console.groq.com/keys
python app.py
```

## 🔗 Live demo

**[Try it here](https://healthcare-ai-assistant-4lf3.onrender.com/)** — deployed on Render. *(swap the `#` for your actual Render URL)*

## Why this exists

A rebuild of a school project, done properly: a real API instead of a shaky local model, real bug fixes, and Tanglish support built around how people here actually type.
