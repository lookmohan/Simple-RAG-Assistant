# Simple RAG Assistant

A clean, beginner-friendly implementation of a **Retrieval-Augmented Generation (RAG)** system for document-based question answering.

This project demonstrates how modern AI systems retrieve relevant information from documents and use a Large Language Model (LLM) to generate **accurate, grounded answers** instead of guessing. It is designed for learning, experimentation, and portfolio use.

---

## 📘 Ready Tensor Publication

This project is officially published on Ready Tensor:

🔗 https://app.readytensor.ai/publications/simple-rag-assistant-document-grounded-ai-for-question-answering-FAos5pUpSSAI

---

## 🎯 What Is This Project For?

This project helps you understand how RAG works in practice. It is useful if you want to:

- Learn Retrieval-Augmented Generation (RAG)
- Understand document-based question answering
- Build a portfolio project for jobs or internships
- Experiment with LLMs safely
- Create a Google Colab or Kaggle demo

The assistant answers questions **only from uploaded documents**, reducing hallucinations and improving reliability.

---

## 🧠 What Can This Project Do?

- Load documents in common formats:
  - `.txt`
  - `.pdf`
  - `.docx`
- Split documents into meaningful chunks
- Convert text into vector embeddings
- Store embeddings in a vector database
- Retrieve the most relevant content for a query
- Generate answers grounded in retrieved context
- Switch between LLM providers without changing core logic

---

## ✨ Key Features

- 📄 Document ingestion
- 🔍 Semantic search using embeddings
- 🤖 Retrieval-Augmented Generation
- 🌍 Multiple LLM providers
- 🔒 Secure by design (no hardcoded API keys)
- 🧪 Ideal for experimentation and learning
- 📦 Works smoothly in Google Colab and Kaggle

---

## 🔧 Supported LLM Providers

The system supports multiple LLM APIs:

- OpenAI
- Groq
- Google Gemini

The provider can be selected at runtime without modifying the RAG pipeline.

⚠️ Model availability depends on API support and provider lifecycle. The retrieval and grounding logic remains the same across providers.

---

## 🧠 How It Works (High Level)

1. Documents are loaded from a `data/` folder  
2. Text is split into overlapping chunks  
3. Embeddings are created for each chunk  
4. Embeddings are stored in a vector database (ChromaDB)  
5. A user question retrieves the most relevant chunks  
6. The LLM generates an answer **only from retrieved content**

This ensures:
- Reduced hallucinations  
- Transparent reasoning  
- Document-grounded answers  

---

## ▶️ Run on Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/lookmohan/Simple-RAG-Assistant/blob/main/RAG_Implementation_v2.ipynb
)

---

## 🛠️ Setup Instructions

### Step 1: Open Google Colab
Visit https://colab.research.google.com  
Open the provided notebook or upload `RAG_Implementation_v2.ipynb`.

---

### Step 2: Install Dependencies

All required dependencies are listed in `requirements.txt`.

Run once:
```bash
!pip install -q -r requirements.txt
````

---

### Step 3: Upload Documents

1. Create a folder named `data/`
2. Upload your `.txt`, `.pdf`, or `.docx` files using the file panel

---

### Step 4: Choose an LLM Provider

Supported providers:

* OpenAI
* Groq
* Google Gemini

Provide API keys securely using environment variables (never hardcode keys).

---

### Step 5: Ask Questions

After documents are indexed, ask questions like:

* “What is NLP?”
* “Explain embeddings from the documents”
* “Summarize the uploaded files”

The assistant responds **only using your documents**.

---

## ⚠️ Limitations

* Not optimized for large-scale production
* Requires valid API keys
* Model availability may change
* Designed mainly for educational and portfolio use

---

## 📜 License

This project is shared for educational and personal use.

---
img src="https://t.bkit.co/w_69553c5bebadc.gif" />

## 🙌 Acknowledgements

This project uses open-source tools such as **LangChain**, **ChromaDB**, and **sentence-transformers** to demonstrate Retrieval-Augmented Generation in a simple and understandable way.
