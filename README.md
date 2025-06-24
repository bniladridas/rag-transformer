
# RAG Transformer: Unifying Knowledge, Seamlessly

Craft intelligent responses across domains with a Retrieval-Augmented Generation (RAG) system that blends dense retrieval and transformer-based generation. From machine learning theory to science fiction narratives and astronomical insights, this system redefines how AI interacts with diverse knowledge.

## Why RAG Transformer?

It's not just about answering queries—it's about understanding them. By fusing external knowledge with powerful language models, RAG Transformer delivers precise, context-aware responses, whether you're exploring AI fundamentals, analyzing sci-fi themes, or interpreting cosmic data.

## Core Innovations

- Multi-Domain Mastery: Effortlessly retrieves and integrates knowledge from technical papers, narrative analyses, and scientific datasets.
- Hybrid Data Fusion: Combines structured (NASA APIs) and unstructured (TMDB) sources for richer insights.
- Coherent Generation: Produces responses that stay true to each domain's context and terminology.

## How It Works

1. Encode: Queries are transformed into semantic embeddings using `sentence-transformers/all-MiniLM-L6-v2`.
2. Retrieve: FAISS powers fast, accurate similarity searches across a unified knowledge base.
3. Generate: `google/flan-t5-base` crafts responses, augmented by retrieved context for precision.

## Get Started

### Prerequisites
- Python 3.8+
- 8GB RAM (minimum)
- CUDA-compatible GPU (optional)

### Setup
```bash
git clone https://github.com/bniladridas/rag-transformer.git
cd rag-transformer
python3 -m venv rag_env
source rag_env/bin/activate
pip install -r requirements.txt
```

### Configure APIs
Create a `.env` file:
```
TMDB_API_KEY=your_tmdb_key
NASA_API_KEY=your_nasa_key
```

### Build Knowledge Base
```bash
python sci_fi_dataset_collector.py
```

### Run the System
```bash
python rag_pipeline.py
```

## Example Queries
- Machine Learning: "Explain attention mechanisms."  
  Retrieves technical insights, delivers a clear explanation.
- Science Fiction: "How do sci-fi films portray AI consciousness?"  
  Pulls narrative analyses, generates thematic discussions.
- Astronomy: "What's the latest on exoplanet discoveries?"  
  Fetches NASA data, provides up-to-date insights.

## Performance
- Retrieval: <50ms per query (CPU)
- Generation: <2s per response
- Memory: ~4GB for full system

## What's Next?
- Short-Term: Modular code, enhanced docs, robust evaluation metrics.
- Long-Term: Hierarchical indexing, adaptive retrieval, web interface, domain-specific fine-tuning.

## Reproducibility
- Public model weights via Hugging Face Hub.
- Deterministic seeds for consistent results.
- Comprehensive logging and unit tests.

## License
MIT License © 2025 Niladri Das

## Acknowledgments
Built on the shoulders of giants: Hugging Face, FAISS, and the open-source community.

Powered by Innovation  
Badges:  
- Python 3.8+: Core language  
- Transformers: Hugging Face ecosystem  
- MIT License: Open and accessible  

