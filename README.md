# Healthcare RAG System Lab

## Overview
This project implements a simple Retrieval-Augmented Generation (RAG) pipeline in a healthcare education setting. The goal is to answer common patient questions by retrieving relevant information from a small medical knowledge base and generating a response grounded in that retrieved context.

## What I built
- **Knowledge base**: A small set of medical topic snippets (diabetes, hypertension, wellness, vaccination) with metadata.
- **Retrieval**: Sentence-transformer embeddings + cosine similarity to return the most relevant documents for a user query.
- **Generation**: A causal language model (GPT-2) generates responses using the retrieved documents as context.
- **Evaluation**: Basic heuristic metrics (response length, grounding overlap with retrieved docs, medical term usage).

## Key takeaway
Retrieval worked well, but generation was not always grounded in the retrieved context (hallucinations can still occur). This highlights why stronger models, better prompts/constraints, and more rigorous evaluation are important for healthcare use cases.

## Tech stack
- Python
- transformers
- sentence-transformers
- scikit-learn (cosine similarity)
- Jupyter Notebook

## Files
- `rag_generation_lab.ipynb` — main notebook with implementation and results
