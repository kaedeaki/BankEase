# 📊 Financial Insight API

This project provides a FastAPI backend to generate LLM-based financial insights and forecasts.  
It is designed to work with both a chatbot and a frontend UI for delivering insights to users in real time.

---

## 🔁 API Integration Flow

```mermaid
graph TD
  User --> Chatbot
  User --> UI
  Chatbot -->|POST /insights| Backend
  UI -->|POST /insights| Backend
  Backend --> MLModels







