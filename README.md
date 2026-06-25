# Healthcare-Agentic-AI-System

🚀 Overview

An AI-powered multi-agent healthcare assistant system designed to support clinical decision-making in resource-constrained environments using:
⚙️ Tech Stack
. LangGraph (multi-agent orchestration)
. Groq API (Llama 3.3 70B)
. FAISS (vector database)
. FastAPI (backend)
. PyPDF + RAG pipeline
. Sentence Transformers (embeddings)

The system simulates a clinical workflow assistant, not a chatbot.

Patient Input
    ↓
Supervisor Agent (LangGraph Router)
    ↓
┌──────────────┬──────────────┬──────────────┐
│ Triage Agent │ Medical RAG │ Tool Agent   │
└──────────────┴──────────────┴──────────────┘
    ↓
Reflection / Safety Agent
    ↓
Structured Medical Response (JSON)

🧠 Key Features
🧠 Multi-agent decision system
📚 Retrieval-Augmented Generation (RAG)
🏥 Healthcare triage classification
🔁 Reflection / hallucination checking loop
🧰 Tool calling (calculator + symptom tools)
🌍 Deployable REST API
📊 Structured JSON medical outputs

. Uses agent routing logic (LangGraph)
. Grounds responses in medical knowledge (FAISS)
. Includes self-evaluation loop (reflection agent)
. Produces structured clinical outputs
. Designed for real-world healthcare environments

Input:
"I have chest pain and difficulty breathing"

Output:
{
  "risk_level": "EMERGENCY",
  "recommendation": "Seek immediate medical attention",
  "possible_conditions": ["Cardiac issue", "Respiratory distress"],
  "confidence": "high"
}

| Endpoint | Description             |
| -------- | ----------------------- |
| /chat    | Main AI agent interface |
| /triage  | Risk classification     |
| /health  | System status           |
| /webhook | WhatsApp integration    |


🧠 What Makes This Different

Unlike traditional chatbots, this system:

Future Enhancements
WhatsApp integration
Persistent patient memory
Azure deployment
Multi-language support
Clinical guideline expansion
Disclaimer

This project is intended for educational and research purposes only and does not provide medical advice.

