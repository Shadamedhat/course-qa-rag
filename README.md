# Course Q&A RAG System

A Retrieval-Augmented Generation system that answers student questions using only course materials, with source attribution.

## Features
- 3 courses: Python, Machine Learning, Linear Algebra
- Supports PDF, DOCX, TXT and CSV files
- Text cleaning and chunking (500 characters, 50 overlap)
- Embeddings with all-MiniLM-L6-v2
- ChromaDB vector database
- LLM answers (Groq) based only on retrieved content
- Sources shown with every answer (file name + page or row)
- Gradio web interface

## How it works
Question -> Embedding -> ChromaDB search (top 3 chunks) -> Prompt -> LLM -> Answer + Sources

If the answer is not in the materials, the system says it could not find it.

## Run
1. Add your files to the data folder (see data/README.md)
2. Add GROQ_API_KEY to Colab Secrets
3. Open the notebook in Google Colab and run all cells

## Tech
Python, sentence-transformers, ChromaDB, Groq, Gradio