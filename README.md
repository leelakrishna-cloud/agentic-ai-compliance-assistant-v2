# Agentic AI Compliance Assistant v2

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-UI-red)
![LangChain](https://img.shields.io/badge/LangChain-Framework-green)
![OpenAI](https://img.shields.io/badge/OpenAI-LLM-black)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20DB-orange)
![PyPDF](https://img.shields.io/badge/PyPDF-Document%20Loader-lightgrey)
![TextBlob](https://img.shields.io/badge/TextBlob-NLP-yellow)

---

## Overview

An enterprise-grade **Agentic AI Compliance Solution** designed to deliver **trusted, explainable, and governed regulatory intelligence for compliance and risk environments**.

This solution enhances traditional RAG by introducing a validation and decision layer, ensuring responses are reliable, traceable, and aligned with compliance requirements.

Designed for compliance use cases where accuracy, traceability, and controlled AI behavior are critical.

---

## Key Concept

**Traditional RAG:**  
Retrieve → Generate → Return

**Agentic AI Flow:**  
Retrieve → Generate → Validate → Decide → Govern → Respond

---

## Key Features

- Retrieval-Augmented Generation (RAG) over regulatory and compliance documents  
- Strict document-grounded responses  
- Validation layer for response support classification:
  - `SUPPORTED`
  - `PARTIAL`
  - `UNSUPPORTED`
- Confidence scoring  
- Controlled AI-assisted fallback for unsupported queries  
- Explainable responses with source traceability  

---

## Architecture

High-level flow of the Agentic AI decision pipeline:

User Query
   ↓
Safe Query Handling
   ↓
Document Retrieval (FAISS Vector Search + Embeddings)
   ↓
Strict Answer Generation
   ↓
Validation Layer (Response Support Classification)
   ├── SUPPORTED   → Document-Based Response
   ├── PARTIAL     → Blend Document + AI Explanation
   └── UNSUPPORTED → AI-Assisted Fallback
   ↓
Confidence Scoring + Source Traceability

Designed for compliance use cases where accuracy, traceability, and controlled AI behavior are essential.

---

## Architecture Diagram

```mermaid
flowchart TD

A[User Query] --> B[Safe Query Handling]
B --> C[Retrieval Layer<br/>FAISS + Embeddings]
C --> D[Document-Grounded Response Generator]
D --> E{Validation<br/>Support Classification}

E -->|SUPPORTED| F[Document-Based Response]
E -->|PARTIAL| G[Blended Response<br/>Document + AI]
E -->|UNSUPPORTED| H[AI-Assisted Response]

F --> I[Confidence Score + Source Traceability]
G --> I
H --> I
```

---

## Why this is Agentic AI

This solution is called **Agentic AI** because it does not simply retrieve and answer.

Instead, it follows a sequence of controlled steps:

- Retrieves relevant document evidence
- Generates a strict document-grounded answer
- Validates whether the answer is supported
- Decides the appropriate response strategy
- Returns the response with confidence and traceability

This introduces **decision-making, control, and governance**, which are critical in compliance environments.

---

## Business Value

**Problem**  
Fragmented regulatory documents and low trust in AI outputs  

**Solution**  
Agentic AI system with validation and controlled decision logic  

**Impact**
- Trusted decision-making  
- Explainable and auditable AI outputs  
- Audit-ready traceability  
- Reduced hallucination risk  

---

## Tech Stack

- Python (Core programming)
- Streamlit (UI / Application layer)
- LangChain (LLM orchestration)
- OpenAI (LLM / Generation)
- FAISS (Vector search / Retrieval)
- PyPDF (Document ingestion)
- TextBlob (Text processing / validation support)

---

## How to Run

1. Install dependencies

       pip install -r requirements.txt

2. Set API key

       export OPENAI_API_KEY="your_api_key"

3. Add PDFs to

       /content/data

4. Run app

       streamlit run app.py

---

## Demo Examples

These examples demonstrate how the system differentiates between supported and unsupported queries and applies controlled response strategies.

**Example 1 — Document-Based Response (SUPPORTED)**  
Query: What is Customer Due Diligence?  
→ Response generated strictly from document evidence  

**Example 2 — AI-Assisted Insight (UNSUPPORTED)**  
Query: What is Model Context Protocol?  
→ Response generated using controlled AI-assisted fallback  

---

## Demo Screenshots

Below screenshots illustrate system behavior across different validation outcomes:

### Scenario 1 — Document-Based Response (SUPPORTED)
![Document-Based Response](Scenario1-Document%20Based.jpg)

### Scenario 2 — AI-Assisted Insight (UNSUPPORTED)
![AI-Assisted Insight](Scenario2-AI-Assisted%20Insight.jpg)


---

## Author

**Leela Krishna.T**  
Director | Data & AI/ML | Agentic AI | Compliance Systems  

Focused on building reliable, explainable, and enterprise-grade AI solutions.
