# 🤖 ParmaTIS AI Assistant

ParmaTIS AI Assistant is a modular, memory-aware chatbot system designed to showcase how modern AI architectures can simulate intelligent internal assistants for organizations. It combines LangChain's Retrieval-Augmented Generation (RAG) capabilities with OpenAI's function-calling Agent SDK, wrapped in a clean Gradio-based UI.

---
## 🧠 What It Does

- ✅ **Convert data** from a knowledge base to vector data store
- ✅ **Retrieves facts** about ParmaTIS from a vector data store
- 🧭 **Decides intelligently** when to use retrieval or general reasoning
- 💬 **Chat UI** built with Gradio for a clean and responsive experience
- ⚙️ Supports **multiple LLMs** including GPT, LLaMA (localhost), Claude, DeepSeek

---

## 🧠 Project Overview

This assistant operates on a fictional dataset describing **Parma Tecno Intelligent Services (ParmaTIS)**, an innovative AI company based in Parma, Italy. The assistant answers questions about the company, including:

* Leadership and employees
* Projects and services
* Departments and history
* General knowledge questions

---

## 🏗️ Architecture Summary

* **RAG Agent (LangChain)**: Uses `ConversationalRetrievalChain`, HuggingFace embeddings, and Chroma vector store for searching ParmaTIS documents.
* **Orchestrator Agent (OpenAI SDK)**: Determines whether to call the RAG agent or respond using general knowledge.
* **Memory Layers**: Provides 3 memory layers.
* **Gradio UI**: Interactive frontend that supports real-time communication with history context.

### Memory Layers

* `RAG_memory`: Internal LangChain memory for RAG responses.
* `chat_memory`: Conversation memory for the orchestrator agent combines also RAG_memory.
* `history_display`: Maintains full chat history for UI display.

---

## 🚀 Features

* Hybrid architecture (RAG + OpenAI Agents )
* Multi-agent orchestration with tool calling
* Company-specific context retrieval
* Clean, async-friendly Gradio interface
* Supports multiple models (GPT, Claude, LLaMA, DeepSeek, etc.)

---

## 🔧 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/bahathabet/rag-openai-agent.git
cd rag-openai-agent
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up environment variables

Create a `.env` file with the following:

```env
OPENAI_API_KEY=your_key_here
ANTHROPIC_API_KEY=...
DEEPSEEK_API_KEY=...
...
```

---

## 💬 Example Prompts

* "Who is the CEO of ParmaTIS?"
* "What projects are currently ongoing?"
* "Tell me about the AI department."
* "What is the capital of France?" *(general knowledge)*

---

## 📦 Built With

* [LangChain](https://www.langchain.com/)
* [OpenAI Agent SDK](https://platform.openai.com/)
* [Gradio](https://www.gradio.app/)
* [ChromaDB](https://www.trychroma.com/)
* [HuggingFace Embeddings](https://huggingface.co/)

---

## 📌 Notes

* This is a **demo project** using **synthetic data** for ParmaTIS.
* Extendable with additional tools: calendar, Gmail, PDF parsing, and more.
* Easily adaptable to real enterprise use cases.

---

## 📜 License

MIT License.
