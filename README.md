# cs5542-lab03
Daniel Evans repo for CS5542 

## Dataset
Documents from [govinfo.gov](https://www.google.com/url?q=https%3A%2F%2Fwww.govinfo.gov%2Fapp%2Fcollection%2Fcfr%2F2024%2Ftitle49) - the Code of Federal Regulations. Specifically, we select documents pertaining to highway transportation and commercial motor vehicles. PDFs contain a large amount of text, as well as many images. When automating rerouting, we want to make sure our suggested routes comply with federal regulations.



## Findings & Discussion

### Chunking Strategy
- Page-based chunking seemed to perform better than fixed-length chunking. I suspect this is due to fixed-length chunks being too fragmented.

### Retrieval Methods
- Sparse (TF-IDF) performance: brought better context to the model
- Dense embeddings performance: had trouble getting good context
- Hybrid fusion: certainly helped with page-based chunking, but didn't really help with fixed-length chunking
- Reranking: neither hurt nor helped results, so might not be worth doing

### Multimodal Evidence
- Query 3 returned the exact image required, showing an example of how drivers should record their duty status.

### Query Failure
- Query 1 seemed to miss the point of the question, even after toying with the question to get a better answer. It generates some tangentially relevant information, but claims it can't find an answer to the question. However, the relevant documents directly answer the question.
