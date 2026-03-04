# Task 03: Rocchio Algorithm for Relevance Feedback

## Overview
This project implements the **Rocchio Algorithm**, a method used to improve query results based on user feedback. By representing documents as vectors in a high-dimensional space (Vector Space Model), the algorithm calculates an "optimal" query vector that maximizes the similarity to known relevant documents while minimizing similarity to non-relevant ones.



## Features
* **TF-IDF Vector Space:** Simulates a corpus of 50 documents and 10 vocabulary terms with randomly generated TF-IDF values.
* **Ground Truth Labels:** Assigns relevance labels to a subset of documents to simulate user feedback.
* **Centroid Calculation:** Computes the average vector (centroid) for both the relevant ($\mu_R$) and non-relevant ($\mu_{NR}$) document sets.
* **Query Optimization:** Implements the Rocchio formula:
  $$q_{opt} = \alpha \cdot q_0 + \beta \cdot \mu_R - \gamma \cdot \mu_{NR}$$
  *(In this specific task, simplified parameters were used: $q_{opt} = 2\mu_R - \mu_{NR}$)*.
* **Similarity Ranking:** Uses **Cosine Similarity** to find the documents that most closely match the newly optimized query vector.

## Technical Tools
* **NumPy:** For high-performance vector operations and matrix manipulations.
* **Pandas:** Used to organize document metadata and display ranked results.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
