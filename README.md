# Healthcare-Agentic-AI-System

🚀 Overview

An AI-powered multi-agent healthcare assistant system designed to support clinical decision-making in resource-constrained environments using:

LangGraph (agent orchestration)
Groq LLM (Llama 3.3 70B)
FAISS (medical knowledge retrieval)
FastAPI (production API layer)

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

⚙️ Tech Stack
. LangGraph (multi-agent orchestration)
. Groq API (Llama 3.3 70B)
. FAISS (vector database)
. FastAPI (backend)
. PyPDF + RAG pipeline
. Sentence Transformers (embeddings)

🧠 Key Features
🧠 Multi-agent decision system
📚 Retrieval-Augmented Generation (RAG)
🏥 Healthcare triage classification
🔁 Reflection / hallucination checking loop
🧰 Tool calling (calculator + symptom tools)
🌍 Deployable REST API
📊 Structured JSON medical outputs

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

. Uses agent routing logic (LangGraph)
. Grounds responses in medical knowledge (FAISS)
. Includes self-evaluation loop (reflection agent)
. Produces structured clinical outputs
. Designed for real-world healthcare environments
