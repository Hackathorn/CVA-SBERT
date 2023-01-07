This repository explores an analysis approach for Construct Validation Assessment (CVA) using S-BERT encodings and similarity metrics.

# What is Construct Validity Assessment (CVA)?

Within the field of sociometric survey questionaires, **Construct Validity** pertains to the degree to which the measure of a construct (questionaire item) sufficiently measures the intended concept (conceptual variable), free of measurement error. [OLeary-Kelly & Vokurka, 1998]. Assessing construct validity has been topic of much research using diverse approaches for several decades. 

This project/repo is the result of an informal discussion with Prof. Kai Larsen at the Leeds School of Business, Univ of Colo, Boulder. The CVA dataset is part of their research and should be attributed to their work. Please cite... 
- Citation -- To Be Completed

# What is S-BERT? 

For CVA, analytic techniques (such as factor analysis and latent semantic analysis) have recently been used. This work explores the use of recent Natural Language Processing (NLP) techniques based on pretrained Large Language Models (LLM) like BERT. In particular, a variation called Sentence-BERT (SBERT) has gain popularity for embedding entire sentences (or paragraphs) into a latent (or embedding) space and computing various pairwise similarity metrics (like Cosine Similarity). 

# Semantic Consistency using S-BERT

Specifically, this work approaches CVA as the _semantic consistency_ or _semantic textual similarity_ (STS) between the Definition sentence with pairwise comparisons with its Item sentences. Variations of Source-Definition-Item relationships are examined as whether they are semantically consistent. 

For example, is the definition of a conceptual variable on this survey questionaire semantically consistent to each of its survey item questions? A person should remark, "Yes, this survey question item does relate to discovering insights into this social variable", thus being judged as reasonable for most humans. The hypothesis is that, since this LLM has been pretrained on huge corpus of human-generated text, S-BERT has the potential to perform at a Human-Level Performance (HLP). 😧

# Notebook List

To understand this repository, work through the following Colab notebooks in order. The initial notebook "Setup" establishes your data environment, introduces you to the dataset, and (optionally) saves results to your Google Drive. Then, the subsequent notebooks focus on specific analyses, as described. 

| Name | Description    | Colab Link |
| -----| :-----------  | :--------: |
| Setup | Loads the CVA dataset, instantiates model, encodes Def-Item pairs, computes metrics, splits 80/20 into train/validate, and checkpoints to gDrive | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-SetUp.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| SimDist | Analyzes distribution of similarity metrics for all Definition-Item pairs. Uses only train_data. | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-SimDist.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| ROC-AUC | Analyzes ROC & AUC using similarity metrics for all Definition-Item pairs. Uses only valid_data. | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-ROC-AUC.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| DefItem | Analyzes Def-to-Items cluster similarity within each Source-Definition (TBC) | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-DefItem.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| SDIclus | Analyzes DefCluster-to-DefCluster similiarity within each Source (TBC) | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-SDIclustering.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| Latent | Analyzes 384-dim latent/embedding space using UMAP, etc (TBC) | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-Latent.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |
| YourOwn | Analyze something interesting! Provides a getting-started template. | <a href="https://colab.research.google.com/github/Hackathorn/CVA-SBERT/blob/main/notebooks/CVA-SBERT-YourOwn.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a> |

> NOTE: TBC means To-Be-Completed implying that the notebook is being developed and is likely to be incomplete and have errors. 

At the beginning of each notebook, there is the Model Parameters section, which sets key parameters to control subsequent cell processing. Normally accept the defaults, unless you want to customize the code and save the results to your Google drive. 

- SBERT_MODEL: The pre-trained LLM fine-tuned from BERT. See [the many models available](https://huggingface.co/models?pipeline_tag=sentence-similarity&sort=downloads). Default is ```all-MiniLM-L6-v2```.

- USE_GDRIVE: Flag to use gDrive if SetUp is customized. Otherwise, pre-generated repos data is used. Default is FALSE.

- CLEAN_TEXT: Default is TRUE implying that text string for Definitions and Items is changed by removing punctuation chars, eliminating whitespace, etc.

- SAVE_PLOT: Flag to save analysis plots that have been customized. USE_GDRIVE must be TRUE. Default is FALSE.

# How To Contribute 

1. Browse/explore this repo. If any comments or suggestions, please submit an Issue. We are ALL learning! 
2. Open the SetUp and DefItem notebooks in Colab. Play and break! And then, share your comments via an Issue. 
3. Contribute to the documentation. What is NOT clear? What is WRONG? Submit an Issue.
4. Contirbute to the code, especially if you have experience with S-BERT or any HuggingFace models. Real Pull-Requests will be a learning experience for us! 
5. Finally, note the Project section, which is the roadmap. We would like to discuss over a Zoom (or like) session. 

# References

- OLeary-Kelly & Vokurka, _Empirical Assessment of Construct Validity_, JOM, 1998.
- KR Larsen & R Sharma, _Theory of Construct and Instrument Development Process: Supplementing Human Judgment with Natural Language Processing Techniques_, SSRN, 2020.
  
- [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks](https://arxiv.org/abs/1908.10084) describes "Sentence-BERT (SBERT), a modification of the pretrained BERT network that use siamese and triplet network structures to derive semantically meaningful sentence embeddings that can be compared using cosine-similarity."

- Overview of the [S-BERT community](https://www.sbert.net/):

  - In S-Bert documentation, Semantic Textual Similarity example is given [here](https://www.sbert.net/docs/usage/semantic_textual_similarity.html)
  - 

- The initial notebook was derived from TDS article by Saketh Kotamraju, [_Intuitive Explaination of Sentence-BERT_](https://towardsdatascience.com/an-intuitive-explanation-of-sentence-bert-1984d144a868), 2022-01-23. Semantic consistency was defined as the cosine similiarity of two 384-dim latent vectors from S-BERT encodings. 

