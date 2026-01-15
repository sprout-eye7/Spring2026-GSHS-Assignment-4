# MLP for XOR

In this assignment, you will implement a text search system using the TF-IDF (Term Frequency–Inverse Document Frequency) representation to identify the most relevant document for a given query.

## Assignment Instructions

### Objective
Implement the `compute_tf`, `compute_idf`, and `compute_tf_idf` functions in tf_idf_search.py to compute TF-IDF vectors for a collection of documents and return the single best-matching document for a given query.

1. The `compute_tf` function should:
    - Given a single document, compute the Term Frequency (TF) of each word in the document.   
    - The starter code for tokenizing the document is already provided.
    - **Input:** A single document.
    - **Output:** A dictionary mapping each word to its term frequency in the document.

```
For a given document d,
TF(w) = (Number of times word w appears in document d) / (Total number of words in document d)
```

2. The `compute_idf` function should:
    - Given a list of input documents, compute the Inverse Document Frequency (IDF) for each word across the entire corpus. 
    - The starter code for tokenizing the documents is already provided.
    - **Input:** A list of documents.
    - **Output:** A dictionary mapping each word to its inverse document frequency value.

```
IDF(w) = log( Total number of documents / Number of documents containing word w )
```

3. The `compute_tf_idf` function should:
   - Given a document and the precomputed IDF values, compute the TF-IDF vector for that document.
   - **Input:** A single document and the IDF dictionary.
   - **Output:** A dictionary representing the TF-IDF vector of the document.

```
For a given document d,
TF-IDF(w) = TF(w) × IDF(w)
```

4. The `cosine_similarity` function should:
    - Given two TF-IDF vectors, compute and return their cosine similarity.
    - **Note:** The complete implementation is already provided.

```
cosine_similarity(A, B) = (A · B) / (||A|| × ||B||)
```

5. The `tf_idf_search` function should:
    - For each document in the input, compute its cosine similarity with the query using their TF-IDF vectors and identify the most relevant document.
    - **Note:** The complete implementation is already provided.
