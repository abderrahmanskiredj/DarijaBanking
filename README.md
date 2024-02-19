# DarijaBanking: A New Resource for Overcoming Language Barriers in Banking Intent Detection for Moroccan Arabic Speakers

## Abstract
This paper introduces *DarijaBanking*, a novel Arabic dataset aimed at enhancing intent detection in the banking domain. Developed through the arabization, localization, deduplication, and cleaning of three English banking datasets, DarijaBanking comprises over 7,200 queries in English, French, Modern Standard Arabic (MSA), and Moroccan Dialect (Darija). This dataset is pivotal for bridging the communication gap in the Moroccan banking sector, enabling better customer service through personalized, language-specific assistance. Our findings demonstrate the superior performance of ArabertV0.2, fine-tuned on DarijaBanking, which achieved high F1-scores of 0.98 for Darija and 0.96 for MSA, showcasing its effectiveness in the targeted application.

## Introduction
In the realm of AI-powered customer service, advanced language models like GPT-4 serve as the central intelligence, coordinating different elements for sophisticated and context-aware interactions. A key feature is the Retrieval Augmented Generation (RAG), which enhances agent responses by integrating information from a comprehensive knowledge base, thus improving interaction quality and relevance. At the heart of this system is the Intent Detection Module, a vital component of Natural Language Understanding (NLU) that deciphers the underlying meaning of user queries to generate the most fitting responses.
This study delves into the application of Natural Language Processing (NLP) in banking, emphasizing personalization and customer engagement. It presents an extensive Darija intent dataset and evaluates various intent detection techniques, including fine-tuning monolingual and multilingual models, zero-shot learning, retrieval-based methods, and leveraging large language models for prompting.

## Contributions
The main contributions of our paper are:

- Introducing the *DarijaBanking dataset*, a multilingual corpus designed for intent detection in Moroccan Arabic.
- Presenting a comparative analysis of various intent detection methods, assessing their effectiveness.
- Providing insights to enhance Moroccan Darija banking intent detection systems, indicating the advantage of specialized classifiers and the efficacy of retrieval-based approaches.

## Dataset
The DarijaBanking dataset features:

- 7,200 multilingual queries across English, French, MSA, and Darija.
- 3,600 queries specifically tailored for MSA and Darija.
- Organized into 24 intent categories.
  
The dataset is the result of a meticulous process involving arabization, localization, deduplication, cleansing, and translating existing English banking data.

## Methodology
We assess various intent detection methods including:

- Full fine-tuning of monolingual and multilingual models.
- Zero-shot learning.
- Retrieval-based approaches.
- Large Language Model prompting.

## Discussion
Our research provides several key insights:

- Cross-lingual transfer learning alone is insufficient for Moroccan Darija.
- Investing in high-quality, domain-specific data labeling improves model accuracy.
- Specialized classifiers are critical for precision in customer query understanding.
- Retrieval-based approaches are a cost-effective alternative for intent detection.

## Limitations and Future Work
The current study's limitations include:

- An intent list that is not exhaustive.
- An approach that does not fully account for the historical and multi-intent nature of conversations.

## Citation
Please cite our paper if you use the DarijaBanking dataset or any part of this work in your research:
<CITATION_TO_BE_ADDED>

## List of Bert-like fine-tuned models on DarijaBanking Dataset with their respective huggingface dataset id:


| Original Model                                 | Model                                                   | DarijaBanking Language Split Trained On |
|-----------------------------------------------|---------------------------------------------------------|-----------------------------------------|
| aubmindlab/bert-base-arabertv02-twitter       | AbderrahmanSkiredj1/banking_ar_dar_arabertv02twitter    | Arabic, Darija                          |
| UBC-NLP/MARBERTv2                             | AbderrahmanSkiredj1/banking_ar_dar_arbertv2             | Arabic, Darija                          |
| UBC-NLP/ARBERT                                | AbderrahmanSkiredj1/banking_ar_dar_arbert               | Arabic, Darija                          |
| UBC-NLP/MARBERT                               | AbderrahmanSkiredj1/banking_ar_dar_marbert              | Arabic, Darija                          |
| qarib/bert-base-qarib                         | AbderrahmanSkiredj1/banking_ar_dar_qarib                | Arabic, Darija                          |
| UBC-NLP/ARBERTv2                              | AbderrahmanSkiredj1/banking_ar_dar_marbertv2            | Arabic, Darija                          |
| CAMeL-Lab/bert-base-arabic-camelbert-da       | AbderrahmanSkiredj1/banking_ar_dar_camelbert_da         | Arabic, Darija                          |
| SI2M-Lab/DarijaBERT                           | AbderrahmanSkiredj1/banking_ar_dar_darijabert           | Arabic, Darija                          |
| CAMeL-Lab/bert-base-arabic-camelbert-mix      | AbderrahmanSkiredj1/banking_ar_dar_camelbertmix         | Arabic, Darija                          |
| alger-ia/dziribert                            | AbderrahmanSkiredj1/banking_ar_dar_dziribert            | Arabic, Darija                          |
| FacebookAI/xlm-roberta-base                   | AbderrahmanSkiredj1/banking_eng_fr_ar_dar_xlm           | English, French, Arabic, Darija         |
| FacebookAI/xlm-roberta-base                   | AbderrahmanSkiredj1/banking_eng_fr_ar_xlm               | English, French, Arabic                 |
| FacebookAI/xlm-roberta-base                   | AbderrahmanSkiredj1/banking_eng_fr_xlm                  | English, French                         |

The models listed are currently private, except for the model AbderrahmanSkiredj1/banking_ar_dar_arabertv02twitter which is public, but you can send a request if you would like to gain access to them.
