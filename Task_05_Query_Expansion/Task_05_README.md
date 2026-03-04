# Task 05: Semantic Query Expansion using Word2Vec

## Overview
This task demonstrates **Semantic Query Expansion**, a technique used to improve retrieval recall. By using a **Word2Vec** model trained on a specific domain (UFC/MMA), the system can "understand" that words like *knockout* might be related to *finish* or *power*, and automatically adds these related terms to the user's search query.



## Pipeline
1.  **Corpus Selection:** A specialized dataset of 20 documents related to Mixed Martial Arts (MMA) and the UFC.
2.  **Advanced Pre-processing:** Includes tokenization, lowercasing, stop-word removal, and **Porter Stemming** for term normalization.
3.  **Word2Vec Training:** Implements a **Skip-gram (sg=1)** model to learn semantic relationships between terms in the corpus.
4.  **Query Expansion Logic:**
    * Takes an original query (e.g., "title fight").
    * Uses the Word2Vec model to find the top $N$ most similar stems.
    * Appends these stems to the original query.
5.  **Vector Space Retrieval:** Uses **TF-IDF** and **Cosine Similarity** to rank documents for both the original and the expanded versions of the query.

## Visualization & Analysis
The project generates:
* **Comparison Tables:** Side-by-side rankings showing how document relevance scores change after expansion.
* **Bar Charts:** Visualizing the increase/decrease in cosine similarity across different query types.
* **Summary Metrics:** Average similarity scores for the top-5 results to evaluate the impact of the expansion.

## Technical Stack
* **Gensim:** For the Word2Vec embedding implementation.
* **NLTK:** For text processing and stemming.
* **Scikit-learn:** For TF-IDF vectorization and similarity calculations.
* **Matplotlib:** For performance visualization.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
