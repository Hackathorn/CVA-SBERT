This repository explores an analysis approach for Content Validation Assessment (CVA) using S-BERT encodings and similarity metrics

# What is Content Validity Assessment?

TODO....

# What is S-BERT? 

TODO...

# Semantic Consistency using S-BERT

Thinking of CVA as the _semantic consistency_ or _semantic textual similarity_ (STS) between the Definition sentence with pairwise comparisons with its Item sentences.

## References

- TODO ref to CVS
  
- [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084) describes "Sentence-BERT (SBERT), a modification of the pretrained BERT network that use siamese and triplet network structures to derive semantically meaningful sentence embeddings that can be compared using cosine-similarity."

- Overview of the [S-BERT community](https://www.sbert.net/):

  - In S-Bert documentation, Semantic Textual Similarity example is given [here](https://www.sbert.net/docs/usage/semantic_textual_similarity.html)
  - adsf
  - asdf

- The initial notebook was derived from TDS article by Saketh Kotamraju, [_Intuitive Explaination of Sentence-BERT_](https://towardsdatascience.com/an-intuitive-explanation-of-sentence-bert-1984d144a868), 2022-01-23. Semantic consistency was defined as the cosine similiarity of two 384-dim latent vectors from S-BERT encodings. 

  


# Notebook List

To use this repository, work through the following Colab notebooks. The initial notebook "Prep" clones the repos and then uses your Google Drive to save results. These results are then used subsequent notebooks, which focus on various analyses (as described below).

| Name | Description    | Colab Link |
| -----| :-----------  | :--------: |
| Create | Reads in the dataset, splits 80/20 into train/validate, checkpoints to gDrive, encodes Definition/Item pairs, and computes similarity metrics | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBert-overview.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| SimDist | asdfadf | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBert-overview.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| DefItem | asdfa asdf asdf asdf asdf asdf | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBert-overview.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
|

