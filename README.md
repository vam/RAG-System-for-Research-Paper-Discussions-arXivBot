# RAG-System-for-Research-Paper-Discussions — arXivBot

---

## 🧠 Overview

arXivBot is a **Retrieval-Augmented Generation (RAG)** system that enables users to interact with research papers using natural language queries.

Instead of relying on keyword search or standalone LLM responses, the system retrieves relevant academic content and generates answers **grounded directly in research papers**, improving factual accuracy and reducing hallucinations.

---

## 🎯 Motivation

During literature reviews, we observed:

- **Searching across multiple papers is time-consuming**
- **Keyword search lacks semantic understanding**
- **LLMs may hallucinate without document grounding**

This project aims to provide **accurate, context-aware research assistance**.

---

## 🏗️ System Architecture

### 🔎 Retrieval Module
- Papers split into **semantic chunks**
- Embedded using **HuggingFace embedding models**
- Indexed via **LlamaIndex** for vector search

### 🤖 Generation Module
- Fine-tuned **Falcon-7B** using **LoRA + 4-bit quantization**
- Generates responses using retrieved context
- Improves **factual consistency**

---

## ⚙️ Technical Approach

- Processed **500 research papers**
- Built vector database for semantic retrieval
- Integrated retriever + generator pipeline
- Implemented custom LLM wrapper
- Optimized training under limited GPU resources

---

## 📊 Evaluation

Grounding quality evaluated using **RAGAS**.

| Metric | Score |
|--------|-------|
| Faithfulness | **0.82** |

---

## ⚡ Challenges

- Limited GPU resources
- Designing RAG pipeline from scratch
- Context window constraints
- Retrieval vs latency trade-off

---

## 🧠 Key Learnings

Built an **end-to-end AI system** demonstrating how retrieval, memory, and generation work together in practical LLM applications.

---

## 🔮 Future Work

- Multilingual support
- Interactive web interface
- Multi-agent workflows
- Extended RAGAS metrics

---

## 🛠️ Tech Stack

**Python • LlamaIndex • HuggingFace Transformers • Falcon-7B • LoRA (PEFT) • RAGAS**
