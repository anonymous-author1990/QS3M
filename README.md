# QS3M
We propose a Query-Specific Siamese Similarity Metric (QS3M) for query-specific clustering of text documents. Our approach uses fine-tuned BERT embeddings to train a non-linear projection into a query-specific similarity space. We build on the idea of Siamese networks, but include a third component, a representation of the query. QS3M is able to model the fine-grained similarity between text passages about the same broad topic and also generalizes to new unseen queries during evaluation. When used to obtain query-relevant clusters, QS3M achieves a 12% performance improvement on two TREC datasets over a recently published BERT-based reference method, as well as many baselines such as TF-IDF and topic models. Similar improvement is observed for another dataset derived from arXiv dataset suggesting the general applicability of QS3M to different domains.

## Download dataset
Download the dataset used for this project from this google drive link: https://drive.google.com/drive/folders/1jTOYL-QnE2B8de42ESithlRN970K_Wfo?usp=sharing

Dataset will be added upon acceptance in JCDL 2022.

## Quickstart

1. Clone this repository, move to the directory and add the current directory to the python classpath
```
git clone https://github.com/anonymous-author1990/QS3M.git
cd QS3M
export PYTHONPATH=.
```

2. Train the QS3M model
```
python3 model/models.py -dd path/to/downloaded/data/ --save
```
This trains the QS3M model with the default parameters and saves the trained model in the "saved_models" directory inside the current directory.

3. Evaluate the trained model
```
python3 eval/eval_model.py -dd path/to/downloaded/data/ -mp saved_models/name-of-the-trained-model.model
```
This evaluates the trained model on two test datasets (TRECCAR benchmark Y1 train and test). Specify the model name saved in "saved_models" directory trained in the previous step.

To train and evaluate other variations of CATS, please make necessary changes to parameters. A detailed description of various parameters can be found by using the --help switch of models.py.
