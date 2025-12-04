# 📘 Conversational RAG with PDF Uploads  
A Streamlit-based **Conversational Retrieval-Augmented Generation (RAG)** application that lets you:

- Upload **PDF files**
- Automatically extract and index text
- Chat with the content using **Groq LLMs**
- Maintain session-based conversation history
- Retrieve context-aware answers

This project integrates **LangChain**, **ChromaDB**, **Groq**, and **Streamlit** to create a powerful AI assistant capable of understanding long documents.

---


---

## 🚀 Features

- 📄 **Upload multiple PDF files**
- 🤖 **Conversational RAG** with context-aware reformulation
- 🧠 **Chat history memory** maintained per session
- ⚡ Uses **Groq’s fast LLMs** via `langchain_groq`
- 🗂 **Chunking + Embeddings + Vector Search** powered by:
  - `RecursiveCharacterTextSplitter`
  - `OllamaEmbeddings`
  - `Chroma` vector database
- 🎯 Short, precise answers
- 🔑 Secure API key input in UI

---

## 🧩 How It Works

### 1️⃣ Upload PDF files  
Documents are extracted using **PyPDFLoader** and split into overlapping chunks.

### 2️⃣ Embedding & Indexing  
Chunks are embedded with **OllamaEmbeddings (gemma:2b)** and stored in **ChromaDB**.

### 3️⃣ Conversational Retriever  
A “history-aware retriever” reformulates queries based on the previous conversation.

### 4️⃣ RAG Workflow  
Retrieved context + user question → LLM generates a concise answer.

### 5️⃣ Session Memory  
Chat history is stored and reused using:

- `ChatMessageHistory`
- `RunnableWithMessageHistory`




