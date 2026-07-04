# AI Research for Intelligent Systems

Under the mentorship of **Aryesh Sir**  
**Coding Blocks School of Technology**

---

## Overview

This project focuses on analyzing Machine Learning research papers and preparing the data for building an intelligent semantic search system using Natural Language Processing (NLP) techniques.

The current phase of the project mainly covers Exploratory Data Analysis (EDA), preprocessing, text analysis, and sentence embedding generation for understanding research paper patterns and semantic relationships.

---

## Dataset

**Dataset Used:** ML ArXiv Papers Dataset

Features used from the dataset:

- Title
- Abstract

The title and abstract are combined to create a single text representation of each research paper for further analysis.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Sentence Transformers
- Hugging Face Datasets
- WordCloud

---

## Exploratory Data Analysis (EDA)

The EDA phase is performed to understand the structure and characteristics of the dataset before building the semantic search system.

### Steps Performed

### 1. Data Loading
- Loaded the ML ArXiv Papers dataset
- Converted dataset into Pandas DataFrame

### 2. Data Preprocessing
- Selected important columns
- Removed unnecessary information
- Combined title and abstract
- Checked for missing values
- Cleaned text data

### 3. Frequent Word Analysis
- Extracted commonly occurring words from abstracts
- Identified frequently used research terms

### 4. Word Cloud Visualization
- Generated a word cloud to visualize dominant terms and concepts in research papers

### 5. Topic Extraction
- Used CountVectorizer to extract important keywords
- Identified major themes present in research papers

### 6. Sentence Embedding Generation
- Generated semantic embeddings using:

`sentence-transformers/all-MiniLM-L6-v2`

Purpose:
- Convert text into numerical vector representations
- Preserve contextual and semantic meaning

### 7. PCA Visualization
- Applied Principal Component Analysis (PCA)
- Reduced high-dimensional embeddings into 2D space for visualization

Purpose:
- Observe relationships among papers
- Identify semantic patterns

### 8. t-SNE Visualization
- Applied t-SNE for dimensionality reduction

Purpose:
- Visualize clustering behavior
- Understand local relationships between research papers

### 9. Similarity Analysis
- Applied cosine similarity to compare embeddings
- Identified semantically similar papers

---

## Output Files Generated

### cleaned_arxiv_papers.csv
Contains processed paper information

### arxiv_embeddings.npy
Contains vector embeddings generated from research papers

---

## Current Project Workflow

Dataset Loading

↓

Data Cleaning

↓

Text Analysis

↓

Word Cloud Generation

↓

Topic Extraction

↓

Embedding Generation

↓

PCA Visualization

↓

t-SNE Visualization

↓

Similarity Analysis


## Advanced Intelligent System Components Added

After completing the Exploratory Data Analysis (EDA), preprocessing, and embedding generation stages, the project was extended with multiple advanced Artificial Intelligence and Natural Language Processing components to transform the system into an intelligent research assistant.

---

## 10. Semantic Search using FAISS

To perform fast retrieval of relevant research papers, semantic search was implemented using Facebook AI Similarity Search (FAISS).

### Model Used

Sentence Transformer:

`sentence-transformers/all-MiniLM-L6-v2`

### Embedding Dimension

384

### Process

1. Convert embeddings into float32 format
2. Apply L2 normalization
3. Create FAISS index
4. Store vector embeddings
5. Search based on semantic similarity

### Purpose

- Understand contextual meaning of queries
- Retrieve relevant papers instead of exact keyword matches
- Enable fast searching in large datasets

### Search Example

Input Query:

Deep learning for medical image analysis

Output:

- Similarity score
- Paper title
- Paper abstract

Top results retrieved:

5 papers

---

## 11. Vector Database Creation

Generated and stored vector representations of research papers using FAISS.

Generated file:

`paper_faiss.index`

Purpose:

- Efficient storage of embeddings
- Faster similarity computation
- Scalable retrieval system

---

## 12. Research Paper Summarization

Automatic summarization was implemented to reduce reading effort.

### Model Used

`sshleifer/distilbart-cnn-12-6`

### Parameters Used

Maximum length:

120 tokens

Minimum length:

40 tokens

### Process

1. Retrieve relevant paper
2. Pass abstract to summarization model
3. Generate concise summary

### Output

AI-generated summary of research papers

Purpose:

- Reduce manual reading effort
- Quickly understand paper content

---

## 13. Search and Summarization Pipeline

A complete search pipeline was developed combining semantic retrieval and summarization.

### Workflow

User Query

↓

Generate Query Embedding

↓

Retrieve Similar Papers

↓

Display Similarity Score

↓

Generate AI Summary

↓

Present Final Results

Purpose:

Provide an intelligent search experience with summarized results.

---

## 14. Keyword Extraction using KeyBERT

Important keywords and phrases were extracted automatically.

### Library Used

KeyBERT

### Configuration

`keyphrase_ngram_range=(1,3)`

### Extracted Information

- Single keywords
- Multi-word phrases
- Important research concepts

Example:

- Deep Learning
- Medical Image Analysis
- Segmentation

Purpose:

- Understand major concepts
- Improve paper analysis
- Support recommendation system

---

## 15. Named Entity Recognition (NER)

Named Entity Recognition was implemented using SpaCy.

### Model Used

`en_core_web_sm`

### Extracted Entities

- Organizations
- Dates
- Locations
- Technologies
- Person names

Example Output

```

("Google","ORG")
("MIT","ORG")
("2025","DATE")

```

Purpose:

- Extract meaningful entities
- Understand important research concepts
- Support knowledge graph generation

---

## 16. Hybrid Search System

A hybrid retrieval system was developed by combining:

1. BM25 Search
2. Semantic Search

### Formula Used

Final Score:

Final Score =

0.5 × BM25 Score

+

0.5 × Semantic Similarity Score

### Purpose

- Improve retrieval quality
- Combine keyword matching with semantic understanding
- Increase search accuracy

Advantages:

- Better ranking
- Context-aware retrieval
- Reduced irrelevant results

---

## 17. Retrieval Augmented Generation (RAG)

RAG architecture was implemented to generate intelligent responses using retrieved research papers.

### Model Used

GPT-2

### Process

1. Retrieve top papers
2. Extract paper abstracts
3. Create context
4. Generate response

Prompt Structure:

Context:

Retrieved research information

Question:

User query

Answer:

Generated response

Purpose:

- Generate contextual answers
- Improve response quality
- Reduce hallucination

---

## 18. Knowledge Graph Generation

Knowledge graphs were generated to visualize relationships among extracted entities.

### Libraries Used

- NetworkX
- Matplotlib

### Process

1. Extract entities
2. Create graph nodes
3. Create edges between related entities
4. Visualize relationships

Purpose:

- Understand connections among concepts
- Discover relationships in research data
- Visualize information structure

---

## 19. Research Paper Recommendation System

A recommendation system was implemented using embedding similarity.

### Process

1. Select paper
2. Obtain embedding vector
3. Search nearest embeddings
4. Recommend related papers

Output:

Top 5 recommended papers

Purpose:

- Discover similar research work
- Assist literature review
- Improve research exploration

---

## Files Generated

### cleaned_arxiv_papers.csv

Contains:

- Title
- Abstract
- Author information

### arxiv_embeddings.npy

Contains:

- Research paper embeddings

Shape:

(500,384)

### paper_faiss.index

Contains:

- FAISS vector index

---

## Final Intelligent System Workflow

Dataset Loading

↓

Data Cleaning

↓

Text Analysis

↓

Word Cloud Generation

↓

Topic Extraction

↓

Embedding Generation

↓

PCA Visualization

↓

t-SNE Visualization

↓

Similarity Analysis

↓

Semantic Search using FAISS

↓

Vector Database Creation

↓

Research Paper Summarization

↓

Keyword Extraction

↓

Named Entity Recognition

↓

Hybrid Search

↓

Retrieval Augmented Generation

↓

Knowledge Graph Generation

↓

Research Paper Recommendation System

↓

Final Intelligent Research Assistant Output

---

## Current Project Capabilities

✓ Research paper collection

✓ Data preprocessing

✓ Exploratory data analysis

✓ Text analysis

✓ Topic extraction

✓ Semantic embedding generation

✓ Similarity analysis

✓ Semantic search

✓ Vector database implementation

✓ Automatic summarization

✓ Keyword extraction

✓ Named Entity Recognition

✓ Hybrid retrieval system

✓ Retrieval Augmented Generation

✓ Knowledge graph visualization

✓ Research paper recommendation system

✓ Intelligent research assistance

