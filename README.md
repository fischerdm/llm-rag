# RAG Chatbot (Proof-of-Concept)

A simple proof-of-concept RAG (Retrieval-Augmented Generation) chatbot built as part of a continuous software engineering education project. The conceptual use case was a trade fair assistant for the Swiss Federal Railways (SBB) to improve information flow among employees at **InnoTrans** — the world's largest trade fair for the rail industry, held in Berlin. One employee spotting an interesting supplier or innovation could instantly share that knowledge with colleagues across the fair, who could then draw on it in their own conversations and negotiations — making the entire visit far more valuable for the team. This is the reason for sample texts — here translated to English — like:

> Supplier X distributes coupling B.

The prototype demonstrates that RAG works: a local LLM answers questions grounded in a custom document set, rather than relying purely on its training data.

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

Open `src/RAG_prototype.ipynb` and run all cells.

## Project Structure

```
data/       # Source documents ingested into the vector store
docs/       # Reference material and notes
src/        # Notebook with the RAG implementation
chroma_db/  # Persisted vector store (not committed to git)
```
