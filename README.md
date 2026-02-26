# Simple RAG Learning Project (LlamaIndex)

This project implements a **minimal Retrieval-Augmented Generation (RAG)** system using **LlamaIndex**, open-source embeddings, and a local HuggingFace LLM.

The goal of this project is to understand the core RAG pipeline end-to-end before moving to more advanced architectures.

---

## 🚀 What this project does

- Loads local documents
- Splits them into semantic chunks
- Generates embeddings for each chunk
- Stores embeddings in an in-memory vector index
- Retrieves relevant context for user queries
- Uses an LLM to generate grounded answers

---

## 🧠 RAG Architecture

The system follows this pipeline:

---

## ⚙️ Tech Stack

- **Framework**: LlamaIndex
- **Embeddings**: HuggingFace (BAAI/bge-small-en-v1.5)
- **LLM**: TinyLlama (local HuggingFace model)
- **Runtime**: Google Colab (GPU)
- **Storage**: In-memory vector store

---

## 📂 Project Structure

---

## ▶️ How to run

1. Open the notebook in Google Colab
2. Enable GPU runtime
3. Upload a text document to the `data/` folder
4. Run cells sequentially
5. Ask questions about your document

---

## 🎯 Key Learnings

- RAG quality depends heavily on document ingestion
- Chunking strategy impacts retrieval performance
- Retrieval selects knowledge, LLM synthesizes answers
- Hardware acceleration greatly improves latency
- LlamaIndex uses global configuration (`Settings`) to connect components

---

## 🔜 Next Steps

- Implement the same pipeline using LangChain
- Add website ingestion
- Experiment with chunk sizes and retrieval depth
- Introduce evaluation metrics
- Explore agentic workflows

---

## 📌 Purpose

This repository is part of a learning journey to understand modern AI application architecture and build intuition around RAG systems.
                +----------------+
                |   Documents    |
                +----------------+
                        |
                        v
                +----------------+
                |    Chunking    |
                +----------------+
                        |
                        v
                +----------------+
                |   Embeddings   |
                +----------------+
                        |
                        v
                +----------------+
                | Vector Index   |
                +----------------+
                        |
         User Query --->|<--- Similarity Search
                        |
                        v
                +----------------+
                |  Retrieved     |
                |    Context     |
                +----------------+
                        |
                        v
                +----------------+
                |      LLM       |
                +----------------+
                        |
                        v
                +----------------+
                |     Answer     |
                +----------------+
