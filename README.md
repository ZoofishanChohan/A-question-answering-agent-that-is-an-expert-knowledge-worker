#  Insurellm Expert Chatbot

A high-accuracy, low-cost knowledge assistant designed for employees of **Insurellm**, an Insurance Tech company. This chatbot leverages **Retrieval Augmented Generation (RAG)** to provide reliable answers by referencing internal documentation and knowledge sources.

##  Project Overview

This project implements a **brute-force RAG architecture** to build a smart, domain-specific chatbot capable of answering complex insurance-related queries with high precision. It’s designed as a first-step prototype for internal deployment across Insurellm teams.

---

##  Features

- **Expert-Level Responses** – Trained on internal insurance documentation and FAQs.
- **Retrieval-Augmented Generation (RAG)** – Fetches relevant documents from a knowledge base to ground the answers.
- **Brute-Force Retriever** – Initial implementation uses a simple vector search for document retrieval.
- **Low-Cost Deployment** – Prioritizes efficiency and budget-conscious infrastructure.

---

##  Tech Stack

- **Language Model**: OpenAI GPT / Local LLMs (configurable)
- **Embedding Model**: e.g., `all-MiniLM-L6-v2` (via SentenceTransformers)
- **Vector Store**: FAISS (Flat Index)
- **Backend**: Python (FastAPI or Streamlit for demo UI)
- **Data Sources**: Internal insurance documents, PDFs, Markdown, FAQs

---

##  How It Works

1. **Ingestion**: Documents are embedded using a sentence transformer and stored in a FAISS index.
2. **Retrieval**: User query is embedded and matched against the vector store to fetch top-k relevant chunks.
3. **Generation**: Retrieved context is appended to the user’s query and sent to the LLM for answer generation.

---

##  Use Cases

- Answering internal employee questions about policies, claims, and procedures.
- Surfacing insights from manuals, handbooks, and training materials.
- Supporting new employee onboarding with instant knowledge access.

---
