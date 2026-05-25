# RAG Evaluation with RAGAS

A complete end-to-end Retrieval-Augmented Generation (RAG) evaluation pipeline using:

* [RAGAS](https://github.com/explodinggradients/ragas?utm_source=chatgpt.com)
* [LangChain](https://www.langchain.com/?utm_source=chatgpt.com)
* [ChromaDB](https://www.trychroma.com/?utm_source=chatgpt.com)
* [Groq API](https://groq.com/?utm_source=chatgpt.com)
* [Hugging Face Sentence Transformers](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2?utm_source=chatgpt.com)

This project demonstrates how to:

* Build a RAG pipeline
* Retrieve relevant context using vector search
* Generate answers using an LLM
* Evaluate the quality of the RAG system using RAGAS metrics

---

# Features

✅ Document chunking and vector storage using ChromaDB
✅ Semantic retrieval using sentence-transformer embeddings
✅ LLM-based answer generation using Groq Llama models
✅ Automatic RAG evaluation using RAGAS
✅ Metrics:

* Faithfulness
* Answer Relevancy
* Context Precision
* Context Recall

✅ JSON export of:

* Generated answers
* Evaluation scores

---

# Architecture

```text
Documents
   ↓
Text Chunking
   ↓
Embeddings (MiniLM)
   ↓
ChromaDB Vector Store
   ↓
Retriever
   ↓
LLM (Groq Llama)
   ↓
Generated Answer
   ↓
RAGAS Evaluation
```

---

# Project Structure

```bash
.
├── main.ipynb
├── rag_outputs.json
├── ragas_scores.json
├── requirements.txt
└── README.md
```

---

# Technologies Used

| Component       | Technology         |
| --------------- | ------------------ |
| Vector Database | ChromaDB           |
| Embeddings      | all-MiniLM-L6-v2   |
| Framework       | LangChain          |
| LLM             | Groq Llama 3.3 70B |
| Evaluation      | RAGAS              |
| Language        | Python             |

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/rag-evaluation-ragas.git
cd rag-evaluation-ragas
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Environment Variables

Set your Groq API key:

```python
import os
os.environ["GROQ_API_KEY"] = "your_api_key"
```

You can get an API key from:

[Groq Console](https://console.groq.com/keys?utm_source=chatgpt.com)

---

# Running the Project

Run the notebook or script:

```bash
python main.py
```

or open:

```bash
main.ipynb
```

---

# 📊 RAGAS Metrics Explained

## 1. Faithfulness

Checks whether the generated answer is supported by the retrieved context.

* High score → grounded answers
* Low score → hallucinations

---

## 2. Answer Relevancy

Measures whether the answer actually addresses the question.

* High score → on-topic answers
* Low score → vague or unrelated answers

---

## 3. Context Precision

Measures whether retrieved chunks are useful.

* High score → relevant retrieval
* Low score → noisy retrieval

---

## 4. Context Recall

Measures whether the retriever found all necessary information.

* High score → complete retrieval
* Low score → missing context

---

# Example Output

```text
Faithfulness         1.000
Answer Relevancy     0.828
Context Precision    1.000
Context Recall       0.933

Overall Score        0.940
```

---

# Example Questions

* What is RAG?
* What does Faithfulness measure?
* How does ChromaDB work?
* What is Context Precision?

---

# Key Learning Outcomes

This project demonstrates:

* Retrieval-Augmented Generation (RAG)
* Vector databases
* Embedding models
* Semantic search
* LLM prompting
* RAG evaluation pipelines
* Hallucination detection
* End-to-end AI system evaluation


# Future Improvements

* Add hybrid retrieval
* Add reranking
* Support PDF ingestion
* Add conversational memory
* Add dashboard visualization
* Deploy as a web app

---

# Contributing

Pull requests are welcome.

For major changes, please open an issue first to discuss what you would like to change.

---



# If you found this useful

Give the repository a star on GitHub ⭐
