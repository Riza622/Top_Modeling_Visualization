# Topic Modeling Analysis

This document outlines the topic modeling workflow and interactive visualization for the corporate disclosures dataset.

## Overview

* **Method**: Latent Dirichlet Allocation (LDA)
* **Topics**: 10
* **Tool**: `pyLDAvis`

## Workflow

1. **Data Preparation**

   * Clean text data: remove stopwords, punctuation, and non-alphabetic characters.
   * Tokenize and lemmatize terms.
   * Create a document-term matrix.

2. **Model Fitting**

   * Use the `topicmodels` or `lda` R package (or Python’s `gensim`) to fit an LDA model with 10 topics.
   * Set hyperparameters: alpha = 0.1, beta = 0.01, iterations = 1000.

3. **Visualization**

   * Export model to JSON via `LDAvis` compatibility functions.
   * Use `pyLDAvis` to create an interactive HTML widget.
   * Save as `LDA_Vis.html` for standalone viewing.

## Viewing the Visualization

Open `LDA_Vis.html` in your web browser to explore:

* **Inter-topic distances**: plotted via multidimensional scaling on principal components.
* **Term relevance**: tune the relevance metric λ to inspect top terms per topic.
* **Frequency & Saliency**: view term frequency and lift across topics.

---

*Riza Saireke — May 2025*
