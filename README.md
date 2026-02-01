
## 🌐 RAG PIPELINE DIAGRAM

```mermaid
graph TD
    A[PDF Transformer Paper] --> B[PyPDFLoader 15 Pages]
    B --> C[Chunking 500-char 80 Chunks]
    C --> D[Embeddings 384-dim Vectors]
    D --> E[FAISS Index Ready]
    
    Q[User Query] --> F[Query Embedding]
    F --> G[Top 3 Chunks Retrieved]
    G --> H[LCEL RAG Chain]
    H --> I[Grounded Answer]
    
    style A
