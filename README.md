# QS3M
We propose a Query-Specific Siamese Similarity Metric (QS3M) for query-specific clustering of text documents. Our approach uses fine-tuned BERT embeddings to train a non-linear projection into a query-specific similarity space. We build on the idea of Siamese networks, but include a third component, a representation of the query. QS3M is able to model the fine-grained similarity between text passages about the same broad topic and also generalizes to new unseen queries during evaluation. When used to obtain query-relevant clusters, QS3M achieves a 12% performance improvement on two TREC datasets over a recently published BERT-based reference method, as well as many baselines such as TF-IDF and topic models. Similar improvement is observed for another dataset derived from arXiv dataset suggesting the general applicability of QS3M to different domains.

## Download dataset
Download the dataset used for this project from this google drive link: https://drive.google.com/drive/folders/1jTOYL-QnE2B8de42ESithlRN970K_Wfo?usp=sharing
*Dataset will be added upon acceptance in JCDL 2022
