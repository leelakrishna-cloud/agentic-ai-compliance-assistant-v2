# Agentic AI Compliance Assistant v2

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Streamlit](https://img.shields.io/badge/UI-Streamlit-red)
![LangChain](https://img.shields.io/badge/Framework-LangChain-green)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-orange)
![OpenAI](https://img.shields.io/badge/LLM-OpenAI-black)
![RAG](https://img.shields.io/badge/Architecture-RAG-purple)
![Agentic AI](https://img.shields.io/badge/Pattern-Agentic%20AI-indigo)
![Governance](https://img.shields.io/badge/Focus-Explainability%20%26%20Governance-teal)

---

## Overview

An enterprise-focused **Agentic AI Compliance Solution** designed to deliver **trusted, explainable, and governed regulatory intelligence**.

This solution goes beyond traditional RAG by introducing a **validation and decision layer** that determines whether a response is fully supported by documents, partially supported, or unsupported before deciding how to respond.

---

## Key Concept

Traditional RAG:  
Retrieve → Generate → Return  

This Solution:  
Retrieve → Generate → Validate → Decide → Respond  

---

## Key Features

- **Retrieval-Augmented Generation (RAG)** over regulatory/compliance PDFs
- **Strict document-grounded answering**
- **Validation layer** to classify responses as:
  - `SUPPORTED`
  - `PARTIAL`
  - `UNSUPPORTED`
- **Confidence scoring** based on retrieval quality
- **Controlled AI fallback** for unsupported or partially supported queries
- **Explainable outputs** with source references and optional retrieved context

---

## Why this is Agentic AI

This is called an **Agentic AI solution** because the system does not simply retrieve and answer.

It performs a sequence of autonomous steps:

1. **Retrieves** relevant document evidence
2. **Generates** a strict document-grounded answer
3. **Validates** whether the answer is actually supported
4. **Decides** whether to:
   - return a document-based answer
   - blend with AI explanation
   - fall back to AI-assisted insight
5. **Responds** with confidence and traceability

This introduces **decision-making, control, and governed behavior**, which are essential in compliance environments.

---

## Architecture Overview

```text
User Query
   ↓
Safe Query Handling
   ↓
Document Retrieval (FAISS + Embeddings)
   ↓
Strict Answer Generation
   ↓
Validation Layer
   ├── SUPPORTED   → Document-Based Response
   ├── PARTIAL     → Blend Document + AI Explanation
   └── UNSUPPORTED → AI-Assisted Fallback
   ↓
Confidence Score + Source Traceability

---

## **Architecture Diagra**

```mermaid
flowchart TD
    A[User Query] --> B[Safe Query Handling]
    B --> C[Retriever Layer<br/>FAISS + Embeddings]
    C --> D[Strict Answer Generator<br/>Document-Grounded]
    D --> E[Validation Layer]

    E -->|SUPPORTED| F[Document-Based Response]
    E -->|PARTIAL| G[Blend Document + AI Explanation]
    E -->|UNSUPPORTED| H[AI-Assisted Fallback]

    F --> I[Confidence Score + Sources]
    G --> I
    H --> I
```

---

Solution Flow

Retrieve → Generate → Validate → Decide → Respond

This is the core design principle of the solution.

---

Business Value
Problem

Regulatory and compliance teams often work with fragmented document repositories and require reliable, traceable answers.

Solution

An Agentic AI assistant that combines RAG, validation, and controlled fallback logic.

Impact

Enables:

---

## Tech Stack

Tech Stack
Python
Streamlit
LangChain
OpenAI
FAISS
PyPDF
TextBlob

---

## How to Run

1. Install dependencies:
   pip install -r requirements.txt

2. Set API key:
   export OPENAI_API_KEY="your_api_key"

3. Add PDF files to:
   /content/data

4. Run application:
   streamlit run app.py

---

## Demo Examples

Example 1:
Query: What is Customer Due Diligence?
Result: Document-based answer (SUPPORTED)

Example 2:
Query: What is Model Context Protocol?
Result: AI-assisted fallback (UNSUPPORTED)

Scenario2-AI-Assisted Insight
![Document-Based Response](Scenario1-Document Based.png)

![AI-Assisted Insight](Scenario2-AI-Assisted Insight.png)

---

## Author

Leela Krishna.T
Director | Data & AI/ML | Agentic AI | Compliance Systems
