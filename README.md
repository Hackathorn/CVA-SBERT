This repository explores an analysis approach for Content Validation Assessment (CVA) using S-BERT encodings and similarity metrics

# What is Content Validity Assessment (CVA)?

With the field of sociometric measurements, **Construct Validity** pertains to the degree to which the measure of a construct (questionaire item) sufficiently measures the intended concept (conceptual variable), free of measurement error. [OLeary-Kelly & Vokurka, 1998]. Assessing this Construct Validity in specific studies has been topic of much research for several decades. 


# What is S-BERT? 

More analytic techniques (such as factor analysis and latent semantic analysis) have recently been used for CVA. This work explores the use of recent Natural Language Processing (NLP) techniques based on pretrained Large Language Models (LLM) like BERT. In particular, a variation called S-BERT or Sentence-BERT has gain popularity for embedding entire sentences (or paragraphs) into a latent (or embedding) space and computing various pairwise similarity metrics (like Cosine Similarity). 

# Semantic Consistency using S-BERT

Specifically, this work approaches CVA as the _semantic consistency_ or _semantic textual similarity_ (STS) between the Definition sentence with pairwise comparisons with its Item sentences.

# Notebook List

To understand this repository, work through the following Colab notebooks in order. The initial notebook "Setup" establishes your data environment and (optionally) save results to your Google Drive. These results can then be used subsequent notebooks that focus on specific analyses. 

| Name | Description    | Colab Link |
| -----| :-----------  | :--------: |
| Setup | Loads the CVS dataset, splits 80/20 into train/validate, instantiates model, encodes Def-Item pairs, computes metrics, and checkpoints to gDrive | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-Setup.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| SimDist | Analyzes distribution of similarity metrics for Def-Item pairs | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-SimDist.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| DefItem | Analyzes .... | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-DefItem.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| Latent | Analyzes .... | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-Latent.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| YourOwn | Analyzes something interesting! | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-using-SBERT-YourOwn.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |

At the beginning of each notebook, there is the Model Parameters section, which sets key parameters to control subsequent cell processing like:

- SBERT_MODEL: The pre-trained LLM fine-tuned from BERT. See [the many models available](https://huggingface.co/models?pipeline_tag=sentence-similarity&sort=downloads).

- USE_GDRIVE: Flag to use gDrive if SetUp is customized. Otherwise, pre-generated repos data is used. Default is FALSE.

- SAVE_PLOT: Flag to save analysis plots that have been customized. USE_GDRIVE must be TRUE. Default is FALSE.

# References

- OLeary-Kelly & Vokurka, _Empirical Assessment of Construct Validity_, JOM, 1998.
- KR Larsen & R Sharma, _Theory of Construct and Instrument Development Process: Supplementing Human Judgment with Natural Language Processing Techniques_, SSRN, 2020.
  
- [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084) describes "Sentence-BERT (SBERT), a modification of the pretrained BERT network that use siamese and triplet network structures to derive semantically meaningful sentence embeddings that can be compared using cosine-similarity."

- Overview of the [S-BERT community](https://www.sbert.net/):

  - In S-Bert documentation, Semantic Textual Similarity example is given [here](https://www.sbert.net/docs/usage/semantic_textual_similarity.html)
  - adsf
  - asdf

- The initial notebook was derived from TDS article by Saketh Kotamraju, [_Intuitive Explaination of Sentence-BERT_](https://towardsdatascience.com/an-intuitive-explanation-of-sentence-bert-1984d144a868), 2022-01-23. Semantic consistency was defined as the cosine similiarity of two 384-dim latent vectors from S-BERT encodings. 

