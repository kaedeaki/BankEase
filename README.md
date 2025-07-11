# 📊 Financial Insight API

This project provides a FastAPI backend to generate LLM-based financial insights and forecasts.  
It is designed to work with both a chatbot and a frontend UI for delivering insights to users in real time.

---

## 🔁 API Integration Flow

```mermaid
graph TD
  User --> Chatbot/UI
  Chatbot/UI -->|POST /insights| Backend
  Backend --> Forecasting
  Forecasting --> LLM
  LLM -->|Summarized Output| Chatbot/UI
```




## API Endpoint Specifications

| Endpoint    | Method | Description                               | Request                                                                    | Response                                             |            
|-------------|--------|-------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------|      
| `/insights` | POST   | Generate forecast and LLM-based insights  |{ "user_id": "string", "account_id": "string", - "transaction_data":[+ {...}]} | { "title": "Spending Insights", "snippet": "..."  }  |      


## Technology Stack  

* **Framework**: FastAPI  

* **Language**: Python 3.10+

* **Libraries**: fastapi, Pydantic, Uvicorn, Facebook Prophet, Groq SDK/API

* **Docs**: Auto-generated with Swagger UI and ReDoc


## 📁 Project Structure

bankease_agentic_app/  
├── backend_api/  
│ ├── insights.py # Entry point of the FastAPI app (defines /insights endpoint)  
│ └── chatbot_logs.jsonl # Output file for chat logs and system actions (generated locally)    
├── logic/    
│ ├── insights_agent2.py # Logic for insight generation using Prophet + LLM  
│ └── prompts.py # Prompt templates for LLM  
└── utils/    
    └── logger.py # JSONL logger for saving insight events  
   


> 💡 Note: `chatbot_logs.jsonl` is not included in the repository. It will be generated when you run the application locally.

## 🔐 Environment Configuration

You must create a `.env` file in the root directory before running the app. This file should contain the following:

```env
GROQ_API_KEY=your_groq_api_key_here
```

## 🔐 Environment Setup    
1. Clone the repository    
2. Create a `.env` file with your API key    
3. cd backend_api
4. Install dependencies



## Interactive API Docs

To run the FastAPI server locally:

```bash
uvicorn insights:app --reload
```


- **Swagger UI** (interactive and user-friendly): [`/docs`](http://127.0.0.1:8000/docs)  
  ↳ ![Example](docs/Swagger_UI_backendAPI.jpg)

- **ReDoc** (well-structured, human-readable): [`/redoc`](http://127.0.0.1:8000/redoc)  
  ↳ ![Supplemental Notes](docs/ReDoc_backendAPI.jpg)

- **OpenAPI Schema** (machine-readable JSON): [`/openapi.json`](http://127.0.0.1:8000/openapi.json)  
  ↳ [JSON Schema File](docs/openapi.json)













