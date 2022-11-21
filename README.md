This repository explores an analysis approach for Content Validation Assessment (CVA) using S-BERT encodings and similarity metrics

# What is Content Validity Assessment?

Construct validity pertains to the degree to which the measure of a construct sufficiently measures the intended concept e.g., is free of measurement error. Ref: O


# What is S-BERT? 

TODO...

# Semantic Consistency using S-BERT

Thinking of CVA as the _semantic consistency_ or _semantic textual similarity_ (STS) between the Definition sentence with pairwise comparisons with its Item sentences.

# Notebook List

To understand this repository, work through the following Colab notebooks in order. The initial notebook "Setup" establishes your data environment and (optionally) save results to your Google Drive. These results can then be used subsequent notebooks that focus on specific analyses. 

At the beginning of each notebook, there is the Model Parameters section, which sets key parameters to control subsequent cell processing like:

- SBERT_MODEL: The pre-trained LLM fine-tuned from BERT. See [the many models available](https://huggingface.co/models?pipeline_tag=sentence-similarity&sort=downloads).

- USE_GDRIVE: Flag to use gDrive if SetUp is customized. Otherwise, pre-generated repos data is used. Default is FALSE.

- SAVE_PLOT: Flag to save analysis plots that have been customized. USE_GDRIVE must be TRUE. Default is FALSE.

| Name | Description    | Colab Link |
| -----| :-----------  | :--------: |
| Create | IGNORE - Initial notebook to be deleted | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBert-Create.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| Setup | Loads the CVS dataset, splits 80/20 into train/validate, instantiates model, encodes Def-Item pairs, computes metrics, and checkpoints to gDrive | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-Setup.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| SimDist | Analyzes distribution of similarity metrics for Def-Item pairs | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-SimDist.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| DefItem | Analyzes .... | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-DefItem.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| YourOwn | Analyzes something interesting! | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-XXX.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
# References

- OLeary-Kelly & Vokurka, _Empirical Assessment of Construct Validity_, JOM, 1998.
- KR Larsen & R Sharma, _Theory of Construct and Instrument Development Process: Supplementing Human Judgment with Natural Language Processing Techniques_, SSRN, 2020.
  
- [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084) describes "Sentence-BERT (SBERT), a modification of the pretrained BERT network that use siamese and triplet network structures to derive semantically meaningful sentence embeddings that can be compared using cosine-similarity."

- Overview of the [S-BERT community](https://www.sbert.net/):

  - In S-Bert documentation, Semantic Textual Similarity example is given [here](https://www.sbert.net/docs/usage/semantic_textual_similarity.html)
  - adsf
  - asdf

- The initial notebook was derived from TDS article by Saketh Kotamraju, [_Intuitive Explaination of Sentence-BERT_](https://towardsdatascience.com/an-intuitive-explanation-of-sentence-bert-1984d144a868), 2022-01-23. Semantic consistency was defined as the cosine similiarity of two 384-dim latent vectors from S-BERT encodings. 

