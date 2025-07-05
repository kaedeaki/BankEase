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
```



```markdown
## API Endpoint Specifications

| Endpoint          | Method | Purpose                  |
|------------------|--------|--------------------------|
| `/insights`       | POST   | LLM-based insight        |


## Interactive API Docs

You can test the endpoints and review schemas at:

git:
uvicorn insights:app --reload

- **Swagger UI** (interactive and user-friendly): [`/docs`](http://127.0.0.1:8000/docs)  
  ↳ [Example Requests (Markdown)](docs/api_example_requests.md)

- **ReDoc** (well-structured, human-readable): [`/redoc`](http://127.0.0.1:8000/redoc)  
  ↳ [Supplemental Notes](docs/redoc_notes.md)

- **OpenAPI Schema** (machine-readable JSON): [`/openapi.json`](http://127.0.0.1:8000/openapi.json)  
  ↳ ![OpenAPI Diagram](docs/openapi_diagram.png)






```






