# Simple RAG Assistant

A clean, beginner-friendly implementation of a **Retrieval-Augmented Generation (RAG)** system.

This project demonstrates how modern AI systems can **retrieve relevant information from documents** and use a **Large Language Model (LLM)** to generate accurate, grounded answers — instead of guessing.

It is designed for **learning, experimentation, and portfolios**, not heavy production use.

---

## 🎯 What Is This Project For?

This project is built to show **how RAG works in practice**.

It is useful if you want to:
- Learn **RAG fundamentals**
- Understand **document-based question answering**
- Build a **portfolio project** for jobs or internships
- Experiment with **LLMs safely**
- Create a **Kaggle or Colab notebook demo**

The system answers questions **only from your documents**, reducing hallucinations and improving reliability.

---

## 🧠 What Can This Project Do?

- Load documents in common formats:
  - `.txt`
  - `.pdf`
  - `.docx`
- Split documents into meaningful chunks
- Convert text into **vector embeddings**
- Store embeddings in a vector database
- Retrieve the most relevant content for a query
- Generate answers using an LLM **grounded in retrieved context**
- Switch between LLM providers **without changing core logic**

---

## ✨ Key Features

- 📄 Document ingestion
- 🔍 Semantic search using embeddings
- 🤖 Retrieval-Augmented Generation
- 🌍 Multiple LLM providers:
- 🔒 Secure by design (no hardcoded keys)
- 🧪 Ideal for experimentation and learning
- 📦 Works smoothly in Google Colab & Kaggle

---

## 🔧 Supported LLM Providers

The system is designed to work with different LLM APIs:

- **OpenAI**
- **Groq**
- **Google Gemini**

The provider can be selected at runtime **without modifying the RAG pipeline**.

> ⚠️ Model availability depends on API support and provider lifecycle.
> The retrieval and grounding logic remains the same across providers.

---

## 🧠 How It Works (High Level)

1. Documents are loaded from a folder
2. Text is split into overlapping chunks
3. Embeddings are created for each chunk
4. Embeddings are stored in a vector database
5. A user question retrieves the most relevant chunks
6. The LLM generates an answer **only from retrieved content**

This ensures:
- Reduced hallucinations
- Transparent reasoning
- Document-grounded answers

---

## ▶️ Running on Google Colab

This project runs smoothly on **Google Colab** with minimal setup.

### Step 1: Open Colab
- Visit https://colab.research.google.com
- Create a **New Notebook**

### Step 2: Install Dependencies
Run once:

```python
!pip install -q langchain chromadb sentence-transformers \
               langchain-community langchain-openai \
               langchain-groq langchain-google-genai \
               pypdf docx2txt
````

### Step 3: Upload Documents

* Create a folder named `data/`
* Upload your `.txt`, `.pdf`, or `.docx` files into it using the file panel

### Step 4: Choose an LLM Provider

You can select:

* OpenAI
* Groq
* Google Gemini

API keys should be provided securely (never hardcoded).

### Step 5: Ask Questions

Once documents are loaded and indexed, ask questions like:

* “What is NLP?”
* “Explain embeddings from the documents”
* “Summarize the uploaded files”

The assistant will respond **only using your documents**.

---

## ⚠️ Limitations

* Not optimized for large-scale production
* Requires valid API keys
* Model availability may change
* Focused on educational use

---

## 📜 License

This project is shared for educational and personal use.

---
