# CodeQA: Advanced Programming Question-Answering using LLM Agent and RAG

## Overview

**CodeQA** is a system designed to enhance programming-related question-answering using a combination of **Large Language Models (LLMs)** and **Retrieval-Augmented Generation (RAG)**. This project addresses the challenges of hallucinations, adaptability, and context sensitivity in traditional transformer-based systems by integrating advanced retrieval techniques and domain-specific LLM fine-tuning.

With the exponential growth of programming languages and their ecosystems, CodeQA serves as a robust mechanism to help developers navigate complex documentation and technical queries efficiently.

## Features

- **Dynamic Retrieval**: Utilizes vector databases for fast and accurate retrieval of programming-related documents.
- **Context-Aware Responses**: Combines in-depth pre-training with RAG techniques to improve accuracy and reduce hallucinations.
- **Zero-Shot Learning**: Achieves high performance on unseen programming queries.
- **Comparative Modeling**: Benchmarks between transformer-based models (Flan-T5) and large-scale LLMs (Deepseek).

## System Architecture

The workflow consists of:
1. **Question Classification**: Determines if the query is programming-related.
2. **Document Retrieval**: Uses cosine similarity to retrieve top 3 relevant documents from a local vector database.
3. **Context-Based Answering**: Generates answers using either the retrieved documents or external web search results.
4. **LLM Integration**: Employs deep pre-trained models for improved context understanding and response generation.

![Workflow Diagram](https://github.com/user-attachments/assets/4569efcd-5761-433f-9713-8fdd67f83df3)

## Results

### Evaluation Metrics
CodeQA has been tested on the **CoNaLa dataset**, with 50 programming questions. The results demonstrate the superior performance of LLM-based models:

| Model                   | Average Score (out of 5) |
|-------------------------|-------------------------|
| Flan-T5-Base           | 2.54                   |
| Deepseek-Coder-1.3b    | 3.32                   |

### Key Findings
- LLMs significantly outperform smaller transformer models in understanding and responding to complex queries.
- Retrieval techniques ensure more accurate and context-relevant answers.
- Flan-T5 is faster, but Deepseek-Coder provides higher-quality answers.

## Technologies Used

- **Programming Language**: Python
- **Core Libraries**:
  - **BeautifulSoup**: For web scraping.
  - **NLTK**: Text preprocessing and chunking.
  - **Multilingual-E5 Base**: Embedding model for document representation.
  - **ChromaDB**: Vector database for efficient retrieval.
- **Models**:
  - **Flan-T5-Base**: A lightweight transformer model.
  - **Deepseek-Coder-1.3b**: A domain-specific large language model.

## Future Work

- **Semantic Chunking**: Enhance document preprocessing for more accurate retrieval.
- **Question-Driven Similarity**: Generate multiple questions per document chunk to improve matching precision.
- **Fine-Tuning**: Train transformer models specifically on programming datasets.
- **Improved Search Tool**: Enhance web-based context retrieval for rare or complex queries.

## References

For a full list of references, see the [paper](https://ieeexplore.ieee.org/abstract/document/10753267).
Our data files: [Main Data](https://drive.google.com/drive/folders/1OeW5SyKsLnIXYEaElsddgM6DdZam_F2R?usp=sharing)
