# RAG_Pipeline

# 📄 End-to-End RAG Pipeline using Google Gemini & LangChain

## 🚀 Overview

This project demonstrates an **end-to-end Retrieval-Augmented Generation (RAG) pipeline** built in Python.
It converts unstructured documents (PDFs) into an intelligent chatbot by combining **semantic search** with **Google Gemini LLMs**.

The solution showcases practical skills in:

* Retrieval-Augmented Generation (RAG)
* Google Gemini embeddings & LLMs
* LangChain framework
* FAISS vector database
* Secure API key management

---

## 🧠 What is RAG?

**Retrieval-Augmented Generation (RAG)** enhances LLM responses by:

1. Retrieving relevant context from external documents
2. Injecting that context into the LLM prompt
3. Generating accurate, grounded answers

This avoids hallucinations and enables **document-aware chatbots**.

---

## 🏗️ Architecture (High Level Flow)

### Phase 1: Document Processing & Indexing

1. **Load & Combine Documents**

   * Upload PDF files
   * Extract and merge text

2. **Split into Chunks**

   * Break text into small, overlapping chunks
   * Optimized for embedding and retrieval

3. **Create Vector Store (FAISS)**

   * Generate embeddings using **Google Gemini**
   * Store vectors in FAISS for fast similarity search

### Phase 2: Retrieval & Generation

4. **Retrieve Relevant Context**

   * Convert user query into an embedding
   * Perform similarity search in FAISS

5. **Prompt the LLM**

   * Inject retrieved chunks into the prompt
   * Call **Gemini LLM** for response generation

6. **Build the Chatbot**

   * Simple conversational interface powered by RAG

---

## 🛠️ Tech Stack

| Component     | Technology             |
| ------------- | ---------------------- |
| LLM           | Google Gemini          |
| Embeddings    | `gemini-embedding-001` |
| Framework     | LangChain              |
| Vector Store  | FAISS                  |
| Language      | Python                 |
| Document Type | PDF                    |

---

## 🔑 Secure API Key Management

API keys are **never hard-coded**.

```bash
export GOOGLE_API_KEY="your_api_key_here"
```

```python
import os
gemini_key = os.getenv("GOOGLE_API_KEY")
```

✔ Follows security best practices
✔ Production-ready approach

---

## 🧩 Key LangChain Concepts Used

* `Document` objects for chunk management
* `TextSplitter` for controlled chunking
* `GoogleGenerativeAIEmbeddings` for vector generation
* `FAISS.from_documents()` for vector indexing
* Retriever-based similarity search
* Prompt chaining for context-aware responses

---

## 📌 Sample Embedding Logic

```python
texts = [doc.page_content for doc in chunks]
embeddings = embedding_model.embed_documents(texts)
```

* Generates embeddings for **all document chunks**
* Used both for FAISS indexing and debugging

---

## 🎯 Use Cases

* Document Q&A systems
* Internal knowledge assistants
* Policy / SOP chatbots
* Research & learning assistants
* Enterprise search applications

---

## 📈 Skills Demonstrated

* ✅ Retrieval-Augmented Generation (RAG)
* ✅ Google Gemini LLM & Embeddings
* ✅ LangChain orchestration
* ✅ Vector databases (FAISS)
* ✅ Secure secret management
* ✅ End-to-end ML application design

---

## 🙌 Future Enhancements

* Streaming responses
* Metadata-based filtering
* Hybrid search (keyword + vector)
* Deployment using FastAPI or Streamlit
* Multi-document conversational memory

---



