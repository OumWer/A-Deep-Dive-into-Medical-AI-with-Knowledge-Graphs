# 🧬 EPTanit — Knowledge Graph-Augmented Medical AI for Clinical Reasoning in Reproductive Medicine

[![Python](https://img.shields.io/badge/Python-blue.svg)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-red.svg)](https://streamlit.io)
[![Neo4j](https://img.shields.io/badge/Neo4j-green.svg)](https://neo4j.com)
[![Groq](https://img.shields.io/badge/LLM-Groq_LLaMA--4-purple.svg)](https://groq.com)

> **Advanced Medical AI System** combining Knowledge Graphs with Retrieval-Augmented Generation (KG-RAG) for clinical fertility reasoning and biomedical insight generation.

---

## 🎯 Overview

**EPTanit** is a domain-specialized Medical AI system designed for **fertility and reproductive medicine**.  
It implements a **Knowledge Graph–augmented Retrieval-Augmented Generation (KG-RAG)** architecture, integrating structured biomedical knowledge with large language model reasoning.

Unlike traditional RAG pipelines, EPTanit leverages a **Neo4j biomedical knowledge graph** to enable structured reasoning, relationship traversal, and clinically grounded responses.

---

## ✨ Key Innovations

- **🔗 Hybrid KG-RAG Architecture**  
  Combines symbolic knowledge graphs with neural LLM reasoning.

- **🏥 Domain-Specialized Intelligence**  
  Tailored specifically for fertility and reproductive medicine.

- **🧠 Multi-Stage Clinical Reasoning**  
  Chain-of-thought style inference with evidence grounding.

- **📊 Property-Aware Entity Mapping**  
  Semantic matching using biomedical node properties and relationships.

- **🔍 Graph-Driven Context Retrieval**  
  Knowledge graph traversal instead of plain vector similarity.

- **📑 Evidence Attribution Layer**  
  Responses grounded in graph entities and discovered paths.

---

## 🏗️ System Architecture

```mermaid
graph TB
    A[User Query] --> B[Biomedical Entity Recognition]
    B --> C[KG Entity Mapping]
    C --> D[Graph Path Discovery]
    D --> E[Context Retrieval]
    E --> F[LLM Chain-of-Thought]
    F --> G[Clinical Answer Generation]
    G --> H[Evidence Attribution]
    
    subgraph "Knowledge Graph Layer"
        I[Neo4j Database]
        J[Disease Nodes]
        K[Drug Nodes]
        L[Relationship Edges]
    end
    
    subgraph "LLM Layer"
        M[Groq LLaMA-4]
        N[Clinical Reasoning]
        O[Answer Synthesis]
    end
    
    C --> I
    D --> I
    E --> I
    F --> M
