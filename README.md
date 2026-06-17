# CapstoneProject

CapstoneProject is an AI assessment platform that turns uploaded study PDFs into context-aware exams. It uses a Retrieval-Augmented Generation architecture to ingest documents, chunk content, generate embeddings, store vectors in Supabase/Postgres with pgvector, and support assessment generation workflows.

Live app reference: https://capstone-project-teal-delta.vercel.app/

## Features

- PDF upload and text extraction pipeline.
- SHA-256 based file deduplication for uploaded documents.
- Chunking and embedding workflow for document content.
- Supabase/Postgres vector storage using pgvector/vecs.
- FastAPI backend with document, user, health, and development routes.
- React/Vite frontend for the application layer.
- Architecture designed around user-owned document access and future API expansion.

## Tech Stack

- React, TypeScript, Vite, Tailwind CSS
- FastAPI and Python
- Supabase and PostgreSQL pgvector
- Ollama for local LLM/embedding workflows
- Docker Compose

## Project Structure

- backend/app/main.py - FastAPI app setup and service initialization
- backend/app/api - API routers for documents, users, health, and dev routes
- backend/app/services - upload, embedding, and vector database services
- backend/app/utils/pdf_processor.py - PDF processing utilities
- src - React frontend
- docker-compose.yml - containerized backend setup

## Getting Started

Install frontend dependencies:

~~~bash
npm install
npm run dev
~~~

Set up backend environment variables:

~~~bash
DATABASE_URL=your_postgres_connection_string
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_KEY=your_supabase_service_role_key
OLLAMA_BASE_URL=http://localhost:11434
~~~

Run the backend with Docker Compose or from the backend directory with Uvicorn after installing backend/requirements.txt.

## Roadmap

- Complete the RAG ingest, chunk, embed, and store pipeline.
- Generate multiple-choice and short-answer assessments from uploaded documents.
- Add role-specific teacher/student workflows.
- Expand toward a public API for educational datasets.

## Status

Capstone project in active development. The repo already contains the frontend, FastAPI service layer, vector database integration, upload service, and PDF processing foundations.
