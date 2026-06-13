# XBioRE-RAG-LLM

🚀 **Explainable Biomedical Relation Extraction using BioBERT, Retrieval-Augmented Generation (RAG), and Large Language Models (LLMs) for evidence-grounded drug–disease discovery.**

---

## Overview

XBioRE-RAG-LLM is an advanced Biomedical Natural Language Processing (BioNLP) framework designed to automatically identify and explain drug–disease relationships from scientific literature.

The framework combines:

* BioBERT-based Named Entity Recognition (NER)
* Drug–Disease Relation Extraction
* Retrieval-Augmented Generation (RAG)
* Large Language Models (LLMs)
* Explainable AI (XAI)

to generate accurate, interpretable, and evidence-backed biomedical insights.

The project evaluates both **Pipeline** and **Joint Learning** architectures and demonstrates how semantic retrieval and LLM reasoning can improve explainability and trustworthiness in biomedical AI systems.

---

## Key Features

### Biomedical Named Entity Recognition (NER)

* BioBERT-based chemical and disease entity extraction
* BIO tagging scheme
* Context-aware biomedical language understanding
* Biomedical entity boundary detection

### Drug–Disease Relation Extraction

* Chemical-Induced Disease (CID) relation prediction
* Pipeline-based architecture
* Joint multi-task learning architecture
* Context-aware BioBERT embeddings

### Retrieval-Augmented Generation (RAG)

* ChromaDB vector database
* Semantic evidence retrieval
* SentenceTransformer embeddings
* Evidence-grounded predictions

### LLM Integration

* Clinical explanation generation
* NER verification
* Biomedical question answering
* Multiple LLM backend support

Supported LLMs:

* GPT-4
* Claude
* Gemini
* Llama-3

### Explainable AI (XAI)

* SHAP explanations
* LIME explanations
* Attention visualization
* Evidence-backed reasoning

### Interactive Web Interface

* Gradio-based application
* Real-time biomedical text analysis
* Interactive explainability dashboard

---

## System Architecture

```text
Biomedical Text
       │
       ▼
 BioBERT NER
       │
       ▼
Relation Extraction
(Pipeline / Joint)
       │
       ▼
 ChromaDB RAG
 Evidence Retrieval
       │
       ▼
     LLM Layer
(Explanation + QA)
       │
       ▼
 SHAP / LIME /
 Attention Maps
       │
       ▼
 Explainable Prediction
```

---

## Dataset

### BC5CDR Dataset

The project uses the BC5CDR benchmark dataset containing:

* PubMed abstracts
* Chemical entity annotations
* Disease entity annotations
* Chemical–Disease relation labels

The dataset supports both:

* Named Entity Recognition (NER)
* Relation Extraction (RE)

tasks in biomedical NLP.

---

## Models Used

### Core Models

* BioBERT (`dmis-lab/biobert-base-cased-v1.2`)
* all-MiniLM-L6-v2 SentenceTransformer

### Supported LLMs

* OpenAI GPT-4
* Anthropic Claude
* Google Gemini
* Meta Llama-3

---

## Tech Stack

### Machine Learning & NLP

* Python
* PyTorch
* Hugging Face Transformers
* Sentence Transformers
* Scikit-learn

### Explainable AI

* SHAP
* LIME

### Retrieval & Storage

* ChromaDB

### Deployment

* Gradio

---

## Experimental Results

### Named Entity Recognition

| Entity Type | Precision | Recall | F1-Score |
| ----------- | --------- | ------ | -------- |
| Chemical    | 0.91      | 0.89   | 0.90     |
| Disease     | 0.88      | 0.86   | 0.87     |
| Overall     | 0.89      | 0.88   | 0.88     |

---

### Relation Extraction

| Model                | Accuracy | Precision | Recall | F1-Score |
| -------------------- | -------- | --------- | ------ | -------- |
| Pipeline Model       | 0.82     | 0.82      | 0.80   | 0.81     |
| Joint Learning Model | 0.88     | 0.86      | 0.85   | 0.85     |

---

### Effect of Class Weighting

| Configuration           | Relation F1 |
| ----------------------- | ----------- |
| Without Class Weighting | 0.78        |
| With Class Weighting    | 0.85        |

---

## Example Workflow

1. Input biomedical abstract
2. Detect chemical and disease entities using BioBERT
3. Predict Chemical-Induced Disease (CID) relationships
4. Retrieve supporting biomedical evidence using ChromaDB
5. Generate clinical explanations using an LLM
6. Visualize model reasoning using SHAP, LIME, and attention maps

---

## Quick Start

### Clone Repository

```bash
git clone https://github.com/<your-username>/xbiore-rag-llm.git
cd xbiore-rag-llm
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Notebook

Open:

```text
notebooks/finalNLPNotebook.ipynb
```

and execute the cells sequentially.

---

## Project Structure

```text
xbiore-rag-llm/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── finalNLPNotebook.ipynb
│
├── docs/
│   └── NLP_Report.pdf
│
└── assets/
    ├── architecture.png
    ├── methodology.png
    ├── attentionVisualization.png
    └── demoOutput.png
```

---

## Future Work

* PubMedBERT integration
* BioMegatron-based biomedical modeling
* CRF-enhanced NER module
* Knowledge Graph integration
* Cross-encoder RAG reranking
* REST API deployment
* Multi-modal biomedical learning
* Clinical decision support systems

---

## Authors

### Harinandana K A

Department of Computer Science Engineering (AI)

### Haripriya A R

Department of Computer Science Engineering (AI)

**Amrita School of Computing, Amritapuri Campus, India**

---

## Citation

If you use this work, please cite:

> LLM-Enhanced Explainable Biomedical Relation Extraction: Pipeline vs Joint Models with RAG-Based Evidence Retrieval

---

## License

This project is intended for academic and research purposes.

---

## Acknowledgements

* BC5CDR Dataset
* BioBERT
* Hugging Face Transformers
* ChromaDB
* Sentence Transformers
* SHAP
* LIME
* Gradio
