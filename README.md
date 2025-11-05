# Mini RAG System Project 🧠

This repository contains the code for a mini Retrieval-Augmented Generation (RAG) system, built from scratch in Python. This project was completed as part of the "Showcase Your AI" homework.

The core purpose of this project is to build an AI system that can answer questions based on a specific, provided knowledge base. This RAG architecture is a key technique used in modern AI to prevent model "hallucinations" and ensure answers are factual and grounded in a trusted source of information.

## How It Works

The system operates in a two-stage pipeline:

1.  **🔍 Retrieval:** When a user asks a question, the system first uses a `sentence-transformer` model (`all-MiniLM-L6-v2`) to convert the question into a numerical vector (embedding). It then compares this embedding to the pre-calculated embeddings of the knowledge base to find and retrieve the most semantically relevant document.

2.  **✍️ Generation:** The retrieved document (the context) and the original user question are then passed to a transformer-based Question-Answering model (`distilbert-base-cased-distilled-squad`). This model carefully reads the context and extracts the precise answer to the question.

## Project Highlights

In this project, I successfully:
*   Built a complete RAG pipeline using Hugging Face models for retrieval and question-answering.
*   Created a self-assessment function to rigorously test the system's accuracy on both retrieval and generation tasks.
*   **Extended the system's knowledge base** by adding a new fact about the planet Mars.
*   **Successfully tested the extended system** with a new question, demonstrating its ability to learn and answer from the newly provided information.

## Technologies Used

*   Python
*   PyTorch
*   Hugging Face `transformers`
*   Hugging Face `sentence-transformers`
*   Google Colab

