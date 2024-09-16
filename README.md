# Identify-clusters-using-Node2Vec-Embedding-Spectral-and-GCN-embeddings
This project identifies clusters in a transaction dataset using three node embedding techniques: Node2Vec, Spectral Embedding, and Graph Convolutional Networks (GCN). The dataset consists of sender-receiver payment transactions, with the transaction amount as the edge weight in the graph.

Link for Dataset: https://drive.google.com/file/d/1fvg_uOfLAJKfZwBiH-ofzejJLcLRHA45/view?usp=sharing

## Methodology:
### Data Processing:
* The transaction data was transformed into a graph where each node represents a sender or receiver, and edges are weighted by the transaction amounts.

### Embeddings:
* Node2Vec: Performed random walks on the graph and used skip-gram to generate 8-dimensional embeddings, later reduced to 3 dimensions via PCA.
* Spectral Embedding: Created an adjacency matrix, followed by a Laplacian matrix. The largest three eigenvectors were used to form the embeddings.
* GCN Embedding: Built a graph convolutional network to capture structural information in the graph.

### Clustering:
* Used K-Means clustering to detect patterns of fraudulent and non-fraudulent transactions, with the number of clusters set to 2.
