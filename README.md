[README_NLP_Practice.md](https://github.com/user-attachments/files/30472682/README_NLP_Practice.md)
# NLP Practice

A collection of hands-on **Natural Language Processing (NLP)** exercises covering text preprocessing, linguistic analysis, text representation, multiclass classification, and retrieval-augmented multi-hop question answering.

The repository progresses from fundamental NLP operations on individual documents to machine-learning classification on benchmark datasets and, finally, knowledge-intensive question answering with **Qwen**, **RAG**, and **FLARE-style active retrieval**.

## Repository Overview

The exercises are organized into three main parts:

| Exercise | Main topic | Data / corpus |
|---|---|---|
| Exercise 1 | Text preprocessing and linguistic analysis | `Sample3` and a Steve Jobs text |
| Exercise 2 | TF-IDF-based multiclass text classification | 20 Newsgroups and AG News |
| Exercise 3 | Multi-hop question answering and retrieval-augmented generation | 2WikiMultihopQA |

## Exercise 1 — Text Preprocessing and Linguistic Analysis

The first exercise applies fundamental NLP operations to the `Sample3` and Steve Jobs text files.

The implemented or demonstrated tasks include:

- Text cleaning and normalization
- Sentence and word tokenization
- Stopword removal
- Stemming
- Lemmatization
- Part-of-speech tagging
- Chunking
- Syntactic parsing
- Basic semantic-relation analysis

This exercise demonstrates how raw text is transformed into structured linguistic information that can be used by later NLP systems.

## Exercise 2 — Multiclass Text Classification

The second exercise focuses on supervised multiclass text classification using two widely used datasets:

- **20 Newsgroups**
- **AG News**

The general workflow includes:

1. Loading the text and category labels
2. Cleaning and preprocessing the documents
3. Converting text into numerical features with **TF-IDF**
4. Splitting the data into training and testing sets
5. Training multiple machine-learning classifiers
6. Comparing model performance using standard classification metrics

Typical evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-score

This exercise shows how text documents can be represented numerically and assigned to predefined topic categories.

## Exercise 3 — Multi-Hop Question Answering with RAG and FLARE

The third exercise explores knowledge-intensive, multi-step question answering using the **2WikiMultihopQA** dataset.

The exercise compares approaches such as:

- Direct question answering with a Qwen language model
- Standard Retrieval-Augmented Generation
- Active retrieval
- FLARE-style retrieval during generation
- Hugging Face API-based model access

Unlike single-hop question answering, multi-hop questions require combining information from multiple pieces of evidence before producing the final answer.

### Main Idea

A standard RAG pipeline retrieves relevant context once before generation. In an active-retrieval or FLARE-style pipeline, retrieval may be triggered again while the answer is being generated when additional information is needed.

The exercise is intended to compare how retrieval strategy affects the quality of answers to multi-step questions.

## Core NLP Concepts Covered

This repository includes practical examples of:

- Natural language preprocessing
- Tokenization
- Stopwords
- Stemming and lemmatization
- POS tagging
- Chunking and parsing
- Bag-of-Words concepts
- TF-IDF vectorization
- N-grams
- Text classification
- Classification metrics
- Information retrieval
- Retrieval-Augmented Generation
- Active retrieval
- Multi-hop question answering
- Large language model inference

## Technologies

The notebooks are written in Python and are intended to run in Jupyter Notebook or Google Colab.

Main technologies used across the exercises include:

- Python
- Jupyter Notebook / Google Colab
- NLTK
- pandas
- NumPy
- scikit-learn
- Hugging Face Datasets
- Hugging Face Transformers / Inference API
- Qwen language models
- Retrieval-Augmented Generation
- FLARE-style active retrieval

Some notebooks may use additional packages depending on the selected retrieval and model-access configuration.

## Installation

Clone the repository:

```bash
git clone https://github.com/Hamedlk80/NLP-practice.git
cd NLP-practice
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Activate it on Linux or macOS:

```bash
source .venv/bin/activate
```

Install the main dependencies:

```bash
pip install jupyter nltk pandas numpy scikit-learn datasets transformers huggingface-hub
```

For notebooks that use dense retrieval or a local vector index, the following packages may also be required:

```bash
pip install sentence-transformers faiss-cpu
```

## Running the Notebooks

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the required notebook and run its cells in order.

The notebooks can also be uploaded to Google Colab. When using Colab, install any missing dependency in the first cell:

```python
!pip install nltk pandas numpy scikit-learn datasets transformers huggingface-hub
```

## Hugging Face API Configuration

Some question-answering experiments use a model through the Hugging Face API.

Store the token as an environment variable instead of writing it directly in the notebook:

```python
import os

HF_TOKEN = os.getenv("HF_TOKEN")
```

On Linux or macOS:

```bash
export HF_TOKEN="your_token_here"
```

On Windows PowerShell:

```powershell
$env:HF_TOKEN="your_token_here"
```

Do not commit API tokens, passwords, or private credentials to GitHub.

## Dataset Notes

### Sample3 and Steve Jobs Text

These files are used for basic preprocessing and linguistic-analysis operations.

### 20 Newsgroups

A benchmark dataset containing documents from multiple discussion-group categories. It is commonly used for topic classification and text-mining experiments.

### AG News

A multiclass news-classification dataset containing articles from several news categories.

### 2WikiMultihopQA

A multi-hop question-answering dataset in which answering a question can require combining evidence from more than one document or fact.

## Suggested Repository Structure

```text
NLP-practice/
├── exercise-1-preprocessing/
│   ├── notebook.ipynb
│   └── text-files/
├── exercise-2-text-classification/
│   └── notebook.ipynb
├── exercise-3-multihop-qa/
│   └── notebook.ipynb
├── requirements.txt
└── README.md
```

The current filenames may be kept unchanged. The structure above is only a recommended organization for making the repository easier to navigate.

## Learning Objectives

After completing these exercises, the learner should be able to:

- Prepare raw text for NLP analysis
- Explain the differences between stemming and lemmatization
- Apply tokenization, POS tagging, chunking, and parsing
- Convert documents into TF-IDF feature vectors
- Train and evaluate multiclass text classifiers
- Work with benchmark NLP datasets
- Explain the role of retrieval in knowledge-intensive NLP
- Distinguish standard RAG from active-retrieval approaches
- Build and compare multi-hop question-answering pipelines

## Limitations

- Some notebooks may require an internet connection to download datasets or access hosted models.
- API-based experiments depend on provider availability, rate limits, and account quotas.
- Generated answers may vary across model versions and inference providers.
- Large datasets and retrieval indexes may require significant memory and storage.
- The repository is educational and is not intended as a production NLP system.

## Future Improvements

Possible improvements include:

- Adding a shared `requirements.txt`
- Replacing notebook-specific installation cells with one reproducible environment
- Adding model-comparison tables to the README
- Saving confusion matrices and classification reports
- Adding retrieval-quality metrics
- Evaluating more embedding and retrieval models
- Comparing local and API-based language models
- Adding automated tests for preprocessing functions
- Organizing notebooks into clearly named exercise folders

## Academic Context

This repository contains practical assignments developed for a Natural Language Processing course. The exercises move from foundational text-processing concepts to machine-learning classification and retrieval-augmented language-model applications.

## License

No license is currently specified for this repository. Add an appropriate license before allowing reuse, modification, or redistribution.
