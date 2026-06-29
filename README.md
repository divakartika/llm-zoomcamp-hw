# LLM Zoomcamp Homework Solutions

This repository contains solutions for two homework assignments from the [LLM Zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp/tree/main) course by [DataTalksClub](https://datatalks.club/):

- **Homework 1: Agentic RAG** in [hw_1_agentic_rag.ipynb](hw_1_agentic_rag.ipynb)
- **Homework 2: Vector Search** in [hw_2_vector_search.ipynb](hw_2_vector_search.ipynb)

## Overview

The project explores two core retrieval and generation patterns used in modern LLM systems:

1. **Homework 1: Agentic RAG**
   - Builds a simple RAG pipeline over course lesson content.
   - Compares plain retrieval with an agentic loop that can call a search tool multiple times.
   - Uses `minsearch`, `toyaikit`, and the OpenAI API.

2. **Homework 2: Vector Search**
   - Uses embeddings to represent text chunks and compare them with cosine similarity.
   - Demonstrates vector search, text search, and hybrid search with Reciprocal Rank Fusion (RRF).
   - Uses the local ONNX embedder and search utilities from the course repository.

## Repository Structure

- [hw_1_agentic_rag.ipynb](hw_1_agentic_rag.ipynb): notebook for the agentic RAG homework.
- [hw_2_vector_search.ipynb](hw_2_vector_search.ipynb): notebook for the vector search homework.
- [embedder.py](embedder.py): wrapper around the ONNX sentence embedding model.
- [ingest.py](ingest.py): helpers for building search indexes from course documents.
- [rag_helper.py](rag_helper.py): supporting logic for the RAG experiments.
- [download.py](download.py): data download utilities.

## Setup

1. Install the project dependencies from [pyproject.toml](pyproject.toml):
   ```bash
   pip install -e .
   ```
   If you prefer, you can also install the packages manually from the same configuration file.

2. Create a `.env` file with your OpenAI API key:
   ```bash
   OPENAI_API_KEY=your-api-key
   ```

3. Launch Jupyter and open either notebook:
   ```bash
   jupyter notebook
   ```

4. Follow the official homework instructions from the [LLM Zoomcamp 2026 cohort](https://github.com/DataTalksClub/llm-zoomcamp/tree/main/cohorts/2026).

## What You Will Learn

- How a basic RAG pipeline retrieves context for an LLM.
- How an agentic loop can improve search by using tools iteratively.
- How embeddings enable semantic similarity search.
- How hybrid retrieval combines keyword and vector signals.
