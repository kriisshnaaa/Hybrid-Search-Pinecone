# 🔍 Hybrid Search using Pinecone, BM25 & HuggingFace Embeddings

A production-ready implementation of **Hybrid Search** by combining **Dense Vector Search** and **Sparse BM25 Search** using **Pinecone**.

This project demonstrates how semantic understanding from transformer embeddings can be combined with exact keyword matching to build highly accurate Retrieval-Augmented Generation (RAG) systems.

---

## 🚀 Features

- ⚡ Dense Embeddings using HuggingFace Sentence Transformers
- 🔤 Sparse Embeddings using BM25
- 🧠 Semantic + Keyword Search
- 📦 Pinecone Vector Database
- 🎯 Hybrid Retrieval
- ⚖️ Adjustable Dense/Sparse Weighting (Alpha)
- 🏗️ Production-Ready Architecture

---

# 🏗️ Architecture

```text
                            Documents
                                │
         ┌──────────────────────┴──────────────────────┐
         │                                             │
         ▼                                             ▼
 HuggingFace Embeddings                      BM25 Encoder
(Dense Semantic Representation)       (Sparse Keyword Representation)
         │                                             │
         └──────────────────────┬──────────────────────┘
                                │
                                ▼
                    Pinecone Hybrid Index
                                │
                     Hybrid Similarity Search
                                │
                                ▼
                      Most Relevant Documents
```

---

# 📚 Technologies Used

- Python
- Pinecone
- HuggingFace Embeddings
- BM25 Encoder
- LangChain
- Sentence Transformers

---

# 📂 Project Workflow

```text
Documents
    │
    ▼
Chunk Documents
    │
    ▼
Generate Dense Embeddings
    │
    ▼
Train BM25 Encoder
    │
    ▼
Generate Sparse Embeddings
    │
    ▼
Store Both Vectors in Pinecone
    │
    ▼
──────────────────────────────────────────────
                User Query
──────────────────────────────────────────────
    │
    ▼
Generate Dense Query Vector
    │
    ▼
Generate Sparse Query Vector
    │
    ▼
Hybrid Search
    │
    ▼
Retrieve Top-K Documents
```

---

# 📈 Why Hybrid Search?

Traditional vector search understands meaning.

Example

```
"What is the capital of France?"

↓

"Paris is the capital city of France."
```

---

Sparse search understands exact keywords.

Example

```
GPT-5

LangChain

Pinecone

BM25

Qdrant
```

---

Hybrid Search combines both approaches.

```text
Final Score

=

Dense Similarity

+

Sparse Similarity
```

This provides:

- Better Recall
- Better Precision
- Better Ranking
- Better Retrieval Quality
- More Accurate RAG Responses

---

# ⚙️ Hybrid Search Pipeline

```text
                    User Query
                         │
         ┌───────────────┴───────────────┐
         │                               │
         ▼                               ▼
 Dense Query Embedding          Sparse Query Encoding
         │                               │
         └───────────────┬───────────────┘
                         ▼
              Pinecone Hybrid Search
                         │
                         ▼
              Ranked Relevant Documents
```

---

# 🧠 Dense Retrieval

Dense vectors capture the semantic meaning of text using transformer embeddings.

Example

```
"How to reset password?"

≈

"Forgot my login credentials"
```

Even if the exact words don't match, semantic search retrieves relevant documents.

---

# 🔤 Sparse Retrieval

Sparse vectors capture exact keyword importance using the BM25 algorithm.

Example

```
GPT-5

Pinecone

LangChain

FAISS

RAG
```

This ensures exact terminology isn't missed.

---

# 📦 Stored Vector Format

Each document stored inside Pinecone contains:

```text
Document
│
├── Dense Vector
├── Sparse Vector
└── Metadata
```

---

# 📁 Project Structure

```text
Hybrid-Search/
│
├── notebooks/
├── data/
├── src/
│   ├── embedding.py
│   ├── bm25.py
│   ├── indexing.py
│   ├── query.py
│   └── utils.py
│
├── requirements.txt
├── README.md
└── .env
```

---

# 🎯 Applications

- Retrieval-Augmented Generation (RAG)
- AI Chatbots
- Enterprise Knowledge Bases
- Semantic Search
- Customer Support Systems
- Internal Document Search
- Question Answering Systems
- Recommendation Systems

---

# 💡 Future Improvements

- Cross-Encoder Reranking
- Metadata Filtering
- Multi-Query Retrieval
- Context Compression
- Graph RAG
- Parent Document Retrieval

---

# 📖 References

- Pinecone
- HuggingFace
- Sentence Transformers
- BM25 Ranking Algorithm
- LangChain

---

# ⭐ If you found this project useful

Please consider giving the repository a **⭐ Star**.

It helps others discover the project and motivates further development.
