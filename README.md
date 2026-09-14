# 🩺 HealthCare AI Assistant

A healthcare chatbot that actually finishes its sentences. Started life as a Class 12 AI project that looked cool in a demo and broke the moment you asked it a real question — rebuilt from the ground up to actually work.

> ⚠️ **Informational only.** This is a learning project, not a medical device. Always consult a real doctor.

## What it does

- **💬 Chat** — a multi-turn conversation with regenerate and voice input, so you can talk instead of type
- **🔍 Disease Prediction** — describe your symptoms, get possible conditions explained in plain language, plus a Low / Medium / "see a doctor now" urgency flag
- **📋 Treatment Plan** — enter a condition (optionally with height/weight for BMI-aware advice) and get a treatment overview you can download as a PDF
- **🌐 Understands Tanglish** — type in Tanglish (Tamil written in English letters) and it understands you, replying back in clear English
- **💡 Built-in glossary** — complex medical terms are wrapped in hover tooltips instead of leaving you to Google them mid-conversation
- **🌗 Dark/light mode**, because nobody wants a retina-searing chatbot at 1am

## Tech stack

- **[Gradio](https://gradio.app)** — the UI
- **[Groq](https://groq.com)** — fast inference via `openai/gpt-oss-120b`
- **Groq Whisper** (`whisper-large-v3-turbo`) — voice-to-text
- **[fpdf2](https://pypi.org/project/fpdf2/)** — PDF export for treatment plans

## Running it yourself

```bash
pip install gradio groq fpdf2
```

Set your Groq API key as an environment variable (grab a free one at [console.groq.com/keys](https://console.groq.com/keys)):

```bash
export GROQ_API_KEY="your-key-here"
```

Then run:

```bash
python app.py
```

## 🔗 Live demo

**[Try it here](#)** — deployed on Render. *(swap the `#` for your actual Render URL)*

## Why this exists

Not trying to reinvent medical AI here — this is a rebuild of a school project, done properly this time: real bug fixes, a real API instead of a shaky local model, and a couple of features (Tanglish support especially) built around how people around here actually type, not just generic textbook English.

## Disclaimer

This tool does not provide medical diagnoses. It's an educational project. If you're feeling unwell, please see an actual doctor.
