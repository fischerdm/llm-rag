# RAG Chatbot — InnoTrans Prototype

A simple proof-of-concept RAG (Retrieval-Augmented Generation) chatbot built as part of a continuous software engineering education project. The original use case was a trade fair assistant for **InnoTrans**, where visitors could ask questions about the latest innovations on display.

This prototype demonstrates that RAG works: a local LLM answers questions grounded in a custom document set, rather than relying purely on its training data.

## Stack

- [Ollama](https://ollama.com/download) — runs the LLM locally
- Llama 3 8B Instruct — the language model
- LangChain — orchestration (document loading, splitting, retrieval chain)
- Chroma — local vector store

## Setup

**1. Install Ollama and pull the model**
```bash
ollama pull llama3
```

**2. Create the conda environment**
```bash
conda env create -f environment.yml
conda activate chatbot
```

**3. Start Ollama**
```bash
ollama serve
```

**4. Run the notebook**

Open `src/my_first_chat_bot_mit_RAG.ipynb` and run all cells.

## Project Structure

```
data/       # Source documents ingested into the vector store
docs/       # Reference material and notes
src/        # Notebook with the RAG implementation
chroma_db/  # Persisted vector store (not committed to git)
```
