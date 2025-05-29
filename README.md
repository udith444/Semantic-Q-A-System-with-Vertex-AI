# Semantic Q&A System with Vertex AI

A question-answering system that uses **semantic search** and **LLMs** to find and generate answers from a Stack Overflow dataset.

!![Alt Text](work_flow.png) 

## Features
- 🔍 **Semantic Search**: Finds relevant answers using embeddings (Google's `textembedding-gecko`).
- 💬 **LLM-Powered Answers**: Generates natural responses using Vertex AI's `text-bison`.
- ⚡ **Optimized Search**: Uses **ScaNN** for fast approximate nearest-neighbor lookup.
- 🛠️ **Handles Unknown Queries**: Gracefully responds when no match is found.

## Tech Stack
- **Google Vertex AI** (Embeddings & Text Generation)
- **Python** (Pandas, NumPy, Scikit-learn)
- **ScaNN** (Scalable Nearest Neighbors)
- **Jupyter Notebook** (Prototyping)

## Dataset

- **Pre-processed Stack Overflow Q&A pairs**: [`so_database_app.csv`](so_database_app.csv)  
  Contains cleaned question-answer pairs from Stack Overflow.

- **Pre-computed embeddings**: [`question_embeddings_app.pkl`](question_embeddings_app.pkl)  
  Generated using Google Vertex AI's `textembedding-gecko@001` model.

---

## Future Improvements

### Short-Term
🚀 **Deploy as a web app**  
   - FastAPI backend + Streamlit/Gradio frontend  
   - Dockerize for easy deployment  

🔍 **Hybrid search**  
   - Combine semantic search (embeddings) with keyword matching (BM25/Elasticsearch)  

### Long-Term
📂 **Expand dataset**  
   - Domain-specific docs (medical, legal, technical)  
   - Dynamic data loading (e.g., live Stack Overflow API)  

🤖 **Fine-tune LLM responses**  
   - Use user feedback to improve answer quality  
   - Add citation to original sources  
