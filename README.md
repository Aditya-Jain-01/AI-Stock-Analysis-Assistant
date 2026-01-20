# AI Stock Analysis Assistant 📈

An AI-powered stock analysis platform that enables natural language interaction with real-time and historical market data. The system leverages LangChain agents with GPT-5 to fetch, analyze, and explain stock information using live data from Yahoo Finance.

---

## ✨ Key Features

- **Real-time Stock Prices**  
  Retrieve current market prices for any publicly traded ticker.

- **Historical Market Analysis**  
  Analyze stock performance over custom date ranges.

- **Financial News Retrieval**  
  Fetch and summarize the latest news related to a company.

- **Balance Sheet Insights**  
  Access and interpret financial statements for deeper analysis.

- **Streaming AI Chat Interface**  
  Conversational interface with token-by-token streamed responses.

---

## 🏗️ Architecture Overview

- **Frontend**: React-based UI for interactive chat experience  
- **Backend**: FastAPI server hosting a LangChain-powered AI agent  
- **AI Layer**: GPT-5 via Thesys API with tool-based reasoning  
- **Data Layer**: Live financial data from Yahoo Finance (yFinance)

---

## 🧰 Tech Stack

### Backend
- **FastAPI** – High-performance Python API framework  
- **LangChain** – Tool-augmented AI agent orchestration  
- **LangGraph** – Stateful agent memory and conversation tracking  
- **yFinance** – Yahoo Finance market data access  
- **Thesys API** – GPT-5 language model integration  

### Frontend
- **React 19** – Component-based UI framework  
- **Vite** – Fast development and build tooling  
- **TypeScript** – Type-safe frontend development  
- **@thesysai/genui-sdk** – AI chat interface components  

---

## 📁 Project Structure

```
AI_Stock_Analysis_Assistant/
├── backend/
│   ├── main.py           # FastAPI server and LangChain agent
│   ├── requirements.txt  # Python dependencies
│   ├── .env              # Environment variables (excluded from VCS)
│   └── venv/             # Python virtual environment
├── frontend/
│   ├── src/
│   │   ├── App.tsx       # Main React application
│   │   └── main.tsx      # Application entry point
│   ├── package.json      # Node.js dependencies
│   └── vite.config.ts    # Vite configuration
└── README.md
```

---

## ⚙️ Setup Instructions

### Prerequisites
- Python 3.10 or higher  
- Node.js 18 or higher  
- npm or yarn  

---

### Backend Setup

```bash
cd backend

python -m venv venv

# Windows
.\venv\Scripts\activate

# macOS / Linux
source venv/bin/activate

pip install -r requirements.txt
```

### Environment Variables

Create a `.env` file in the `backend` directory:

```
OPENAI_API_KEY=your_api_key_here
LLM_MODEL=c1/openai/gpt-5/v-20250930
LLM_BASE_URL=https://api.thesys.dev/v1
```

> Environment variables are managed securely using `.env` files and are excluded from version control.

---

### Frontend Setup

```bash
cd frontend
npm install
```

---

## ▶️ Running the Application

### Start Backend (Terminal 1)

```bash
cd backend
python main.py
```

Backend: **http://localhost:8888**

---

### Start Frontend (Terminal 2)

```bash
cd frontend
npm run dev
```

Frontend: **http://localhost:3000**

---

## 🔌 API Endpoint

| Endpoint     | Method | Description                                      |
|-------------|--------|--------------------------------------------------|
| `/api/chat` | POST   | Send a prompt and receive a streaming AI response |

---

## 🧠 AI Agent Capabilities

| Tool Name                     | Description                                      |
|------------------------------|--------------------------------------------------|
| `get_stock_price`             | Fetches the current price of a stock             |
| `get_historical_stock_price`  | Retrieves historical price data for a date range |
| `get_balance_sheet`           | Returns company balance sheet data               |
| `get_stock_news`              | Fetches recent news articles for a stock         |

---

## 💬 Example Queries

- What is the current price of AAPL?
- Show TSLA stock performance from Jan 2024 to Dec 2024
- Get the latest news on NVDA
- Show Microsoft’s balance sheet

---

## 🔐 Security & Best Practices

- API keys are stored using environment variables  
- `.env` files are excluded from Git version control  
- No secrets are committed to the repository  

---

## 📄 License

MIT License
