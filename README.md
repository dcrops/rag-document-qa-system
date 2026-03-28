# 📄 RAG Document QA System

A Retrieval-Augmented Generation (RAG) application that allows users to upload documents and ask natural language questions, receiving context-aware answers grounded in the source material.

---

## 🚀 Overview

This project demonstrates how to build an end-to-end RAG pipeline combining:

- Document ingestion
- Text chunking & embedding
- Vector similarity search
- LLM-based answer generation

The system retrieves relevant document context and uses it to generate accurate, explainable responses.

---

## 🧠 Key Features

- Upload and process documents (PDF / text)
- Chunking and embedding using modern embedding models
- Vector search for relevant context retrieval
- LLM-powered question answering
- Context-grounded responses (reduces hallucination)
- Modular pipeline design for easy extension

---

## 🏗️ Architecture

The system follows a standard RAG pipeline:

1. **Ingestion**
   - Load documents
   - Clean and preprocess text

2. **Chunking**
   - Split documents into manageable segments

3. **Embedding**
   - Convert chunks into vector representations

4. **Storage**
   - Store embeddings in a vector database

5. **Retrieval**
   - Perform similarity search based on user query

6. **Generation**
   - Pass retrieved context to an LLM to generate answers

---

## 🧪 Example Workflow

1. Upload a document
2. Ask a question like:
   > "What are the key risks mentioned in this report?"

3. System:
   - Finds relevant chunks
   - Sends them to the LLM
   - Returns a grounded answer

---

## 🛠️ Tech Stack

- **Python**
- **LangChain** (or custom orchestration)
- **OpenAI / LLM API**
- **Vector DB** (Chroma / Pinecone / FAISS)
- **Streamlit / FastAPI** (depending on your implementation)


## 📁 Project Structure

rag-document-qa-system/
│
├── app/ # Application entrypoints (API / UI)
├── src/
│ ├── ingestion/ # Document loading & preprocessing
│ ├── chunking/ # Text splitting logic
│ ├── embeddings/ # Embedding generation
│ ├── retrieval/ # Vector search logic
│ ├── generation/ # LLM interaction
│ └── utils/ # Helper functions
│
├── data/ # Sample documents
├── vectorstore/ # Stored embeddings
├── notebooks/ # Experiments / exploration
├── requirements.txt
└── README.md

---

## ⚙️ Setup

### 1. Clone the repository


git clone https://github.com/your-username/rag-document-qa-system.git
cd rag-document-qa-system

### 2. Install dependencies

pip install -r requirements.txt

### 2. Set environment variables

export OPENAI_API_KEY=your_api_key

## ▶️ Running the Application

### Option 1 — Streamlit UI


streamlit run app/app.py

### Option 2 — FastAPI

uvicorn app.main:app --reload

## 🔍 Example Use Cases
  - Internal document search
  - Knowledge base assistants
  - Compliance and policy lookup
  - Research summarisation
  - Customer support tooling

## ⚠️ Limitations
  - Performance depends on chunking strategy and embedding quality
  - Requires API access to LLM provider
  - Large documents may require optimisation

## 🔮 Future Improvements
  - Hybrid search (keyword + vector)
  - Metadata filtering
  - Source citation highlighting
  - Conversation memory
  - Deployment (Docker / cloud)

## 📌 Why This Project
This project demonstrates practical AI engineering skills:

  - Designing end-to-end LLM systems
  - Working with embeddings and vector databases
  - Managing context for reliable LLM outputs
  - Building modular, production-style pipelines

## 📄 License

This project is for educational and portfolio purposes.
