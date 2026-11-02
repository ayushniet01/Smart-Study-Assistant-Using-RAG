
# Smart Study Assistant using RAG

An AI-powered academic assistant that helps students organize study materials, search documents, and get context-aware answers using Retrieval-Augmented Generation (RAG).

## Overview

Smart Study Assistant is a document-based learning platform that allows users to upload academic materials and interact with them through an AI-powered question-answering system.

It uses semantic search and Large Language Models (LLMs) to retrieve relevant information from uploaded documents and generate meaningful answers with source references.

## Key Features

- Upload academic documents, PDFs, notes, and slides.
- Organize study materials by classes and subjects.
- Semantic search for relevant document content.
- AI-powered question answering using RAG.
- Context-aware responses with source citations.
- Background document processing and embedding generation.
- User authentication and document management.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite, Tailwind CSS |
| Backend | Python, FastAPI |
| AI/LLM | OpenAI API, RAG |
| Embeddings | Text Embeddings |
| Vector Database | Pinecone |
| Database | PostgreSQL |
| Background Tasks | Celery, Redis |
| Storage | AWS S3 |
| Deployment | Docker, Docker Compose |

## RAG Workflow

1. Upload academic documents.
2. Extract and process document text.
3. Split text into smaller chunks.
4. Generate vector embeddings.
5. Store embeddings in Pinecone.
6. Retrieve relevant content through semantic search.
7. Pass retrieved context to the LLM.
8. Generate answers with relevant source references.

## Project Structure

```text
smart-study-assistant/
│
├── frontend/
├── ingestion-service/
├── embedding-worker/
├── query-service/
├── shared/
├── database/
├── docker-compose.yml
└── README.md
```

## Installation and Setup

### Prerequisites

- Python 3.9+
- Node.js 18+
- Docker and Docker Compose
- Required API credentials

### 1. Clone Repository

```bash
git clone https://github.com/YOUR-USERNAME/smart-study-assistant.git
cd smart-study-assistant
```

### 2. Configure Environment

Create a `.env` file in the project root and configure the required credentials:

```env
OPENAI_API_KEY=your-api-key
REDIS_URL=your-redis-url
CELERY_REDIS_URL=your-celery-redis-url
DATABASE_URL=your-database-url
PINECONE_API_KEY=your-pinecone-api-key
PINECONE_INDEX_NAME=your-index-name
JWT_SECRET_KEY=your-secret-key
```

Configure additional variables required by your services.

### 3. Start Backend Services

```bash
docker-compose up -d
```

### 4. Start Frontend

```bash
cd frontend
npm install
npm run dev
```

### 5. Access Application

```text
Frontend: http://localhost:5173
Query Service: http://localhost:8000
Ingestion Service: http://localhost:8001
Auth Service: http://localhost:8002
```

## Application Usage

1. Register or log in.
2. Create a class or subject.
3. Upload academic documents.
4. Wait for document processing.
5. Ask questions through the AI chat interface.
6. Get answers based on uploaded study materials.

## Future Enhancements

- Multilingual support.
- Automatic quiz generation.
- AI-generated summaries.
- Voice-based interaction.
- Personalized learning recommendations.
- Improved document retrieval accuracy.

## Conclusion

Smart Study Assistant combines Artificial Intelligence, semantic search, and Retrieval-Augmented Generation to simplify academic learning.

It transforms traditional study materials into an interactive knowledge base, helping students find information and understand their subjects more efficiently.

---

**Technologies:** Python | React | FastAPI | OpenAI | Pinecone | PostgreSQL | Redis | Docker
