## API Integration Flow

```mermaid
graph TD
  User --> Chatbot
  User --> UI
  Chatbot -->|POST /insights| Backend
  UI -->|POST /insights| Backend
  Backend --> MLModels




["API Endpoint Specifications"]

| Endpoint          | Method | Description                            | Request Body                | Response                        |
|------------------|--------|----------------------------------------|-----------------------------|---------------------------------|
| `/insights`       | POST   | Generate LLM-based financial insight   | `{query, user_id}`          | `{insight: "...text..."}`       |
| `/health`         | GET    | Status check for backend service       | N/A                         | `{"status": "ok"}`             |
