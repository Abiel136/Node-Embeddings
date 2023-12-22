# Node-Embeddings

I provide a Python implentation of the idea found in : https://math.ryerson.ca/~pralat/papers/2023_community+embeddings-CN2022.pdf (the code base is in Julia).

The aim is community detection using Node2Vec combined with Leiden or Louvain. Some plots analysing the effectiveness of the method are also produced. 

## How does it work:

It is very heavily based on the machinery of Word2Vec, which provides vector embeddings of words inside a text. This is then applied to nodes of a graph.

1. Create the "text" - this is done via random walks on the graph of specified length
2. Apply Word2Vec on this new "text".
3. Apply KMeans clustering on the vectors and create lots of small "communities"
4. Apply Leiden or Louivan with the found communities as the initial state.


##  Information about methods:

More info can be found at :

- Node2Vec: https://towardsdatascience.com/node2vec-explained-db86a319e9ab
- Word2Vec: https://towardsdatascience.com/word2vec-explained-49c52b4ccb71
- Leiden algorithm: https://arxiv.org/abs/1810.08473
- A note on Modularity: https://en.wikipedia.org/wiki/Modularity_(networks)




