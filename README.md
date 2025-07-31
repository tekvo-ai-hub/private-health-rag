# Private Patient Query System

**Industry:** Healthcare

**Repository:** [tekvo-ai-hub/private-health-rag](https://github.com/tekvo-ai-hub/private-health-rag)

## Description
A secure, on-prem RAG system for querying sensitive patient data.

## Requirements
### Functional
- Ingest patient records in PDF format.
- Allow doctors to ask natural language questions.
- Retrieve relevant data without exposing PHI externally.
### Non-Functional
- 100% on-prem deployment.
- Low-latency inference.
- HIPAA-compliant data handling.
## Solution Design
**LLM:** Mistral 7B (local)
**Vector DB:** ChromaDB (on-prem)

### Components
- Document Ingestion Pipeline
- Embedding using BGE-small
- RAG Retrieval Engine
- Local LLM Prompt Engine
### Data Flow
$ PDF → Chunker → Embedder → VectorDB → Retriever → Prompt → LLM → Answer

### Tech Stack
- **Frontend:** Streamlit
- **Backend:** FastAPI
- **Storage:** Local Disk
- **Deployment:** Docker Compose
