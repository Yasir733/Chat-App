# 🚀 Real-Time Chat + AI Assistant

A full-stack, scalable real-time chat application integrated with an AI assistant powered by RAG (Retrieval-Augmented Generation). This project demonstrates modern backend architecture, real-time communication, and AI integration.

---

## 📌 Features

### 💬 Real-Time Chat

* WebSocket-based messaging
* Typing indicators & online presence
* Scalable with Redis Pub/Sub
* Message persistence

### 🔐 Authentication

* JWT-based authentication
* Secure login & registration
* Protected routes

### 🤖 AI Assistant

* AI chatbot integrated into chat UI
* Context-aware responses
* Supports conversation memory

### 🧠 RAG (Retrieval-Augmented Generation)

* Document-based Q&A
* Embeddings + Vector Search
* Contextual AI responses using external knowledge

---

## 🏗️ Architecture

```
Client (React)
   ↓
Node.js Backend (API + WebSockets)
   ↓
AI Service (RAG + LLM)
   ↓
Data Layer:
  - Database (MongoDB/Postgres)
  - Redis (Pub/Sub, Cache)
  - Vector DB (FAISS/Pinecone)
```

---

## 📁 Project Structure

```
real-time-chat-ai/
│
├── client/          # React frontend
├── server/          # Node.js backend
├── ai-service/      # AI microservice (Python/Node)
├── docker/          # Docker configs
├── docs/            # Documentation
├── .env
├── docker-compose.yml
└── README.md
```

---

## ⚙️ Tech Stack

### Frontend

* React.js
* WebSockets (Socket.io / native)
* Axios

### Backend

* Node.js
* Express.js
* JWT Authentication
* Redis

### AI / ML

* LangChain / Custom RAG pipeline
* Vector DB (FAISS / Pinecone)
* LLM APIs (OpenAI / local models)

### DevOps

* Docker & Docker Compose
* Nginx (optional)

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/real-time-chat-ai.git
cd real-time-chat-ai
```

---

### 2️⃣ Setup Environment Variables

Create `.env` files in `server/` and `ai-service/`:

#### Server `.env`

```
PORT=5000
JWT_SECRET=your_secret
DB_URI=your_database_url
REDIS_URL=redis://localhost:6379
AI_SERVICE_URL=http://localhost:8000
```

#### AI Service `.env`

```
OPENAI_API_KEY=your_key
VECTOR_DB_PATH=./vector-db
```

---

### 3️⃣ Run with Docker (Recommended)

```bash
docker-compose up --build
```

---

### 4️⃣ Run Manually

#### Start Backend

```bash
cd server
npm install
npm run dev
```

#### Start Frontend

```bash
cd client
npm install
npm run dev
```

#### Start AI Service

```bash
cd ai-service
pip install -r requirements.txt
python main.py
```

---

## 🔌 API Endpoints

### Auth

* `POST /api/auth/register`
* `POST /api/auth/login`

### Chat

* `GET /api/chat/history`
* `POST /api/chat/message`

### AI

* `POST /api/ai/chat`
* `POST /api/ai/rag`

---

## 🔗 WebSocket Events

| Event        | Description           |
| ------------ | --------------------- |
| `connect`    | User connects         |
| `message`    | Send/receive messages |
| `typing`     | Typing indicator      |
| `disconnect` | User disconnects      |

---

## 🧠 RAG Flow

```
User Query
   ↓
Embedding Generation
   ↓
Vector DB Search
   ↓
Relevant Context Retrieval
   ↓
LLM Response Generation
   ↓
Response to User
```

---

## 🧪 Future Enhancements

* Group chats
* File sharing
* Voice messages
* AI agents (multi-step reasoning)
* Chat summarization
* Role-based access control

---

## 📸 Screenshots (Optional)

*Add screenshots of UI here*

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## 📜 License

MIT License

---

## 👨‍💻 Author

**Yasir Hussain**

* Full Stack Developer (React + Node.js)
* AI/ML Enthusiast

---

## ⭐ Show Your Support

If you like this project, give it a ⭐ on GitHub!
