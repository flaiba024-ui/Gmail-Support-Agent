# Gmail Support Agent

> An AI-powered customer support automation built with **n8n** that reads incoming Gmail messages, retrieves relevant information from a recipe knowledge base, and automatically generates a helpful email response.

![Workflow Preview](workflow-preview.png)

---

## 📌 Overview

The **Gmail Support Agent** automates repetitive support questions by combining Gmail, an AI Agent, and a vector-based knowledge base.

Instead of manually reading every support email and searching for an answer, the workflow allows an AI Agent to retrieve relevant information from the knowledge base and respond automatically.

This project demonstrates a practical **AI-powered support automation** using **RAG (Retrieval-Augmented Generation)** principles.

---

## ⚙️ How It Works

```text
                    ┌─────────────────────┐
                    │     Gmail Trigger   │
                    │  Incoming Question  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      AI Agent       │
                    │ Understands Request │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Pinecone Vector DB  │
                    │  Knowledge Retrieval│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   OpenAI Chat Model │
                    │  Generate Response  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Gmail Reply      │
                    │ Automated Response  │
                    └─────────────────────┘
