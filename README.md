# DarijaBanking: A New Resource for Overcoming Language Barriers in Banking Intent Detection for Moroccan Arabic Speakers

## Abstract
Navigating the complexities of language diversity is a central challenge in developing robust natural language processing systems, especially in specialized domains like banking. The Moroccan Dialect (Darija) serves as the common language that blends cultural complexities, historical impacts, and regional differences. The complexities of Darija present a special set of challenges for language models, as it differs from Modern Standard Arabic with strong influence from French, Spanish, and Tamazight, it requires a specific approach for effective communication. To tackle these challenges, this paper introduces **DarijaBanking**, a novel Darija dataset aimed at enhancing intent classification in the banking domain, addressing the critical need for automatic banking systems (e.g., chatbots) that communicate in the native language of Moroccan clients. DarijaBanking comprises over 1,800 parallel high-quality queries in Darija, Modern Standard Arabic (MSA), English, and French, organized into 24 intent classes. We experimented with various intent classification methods, including full fine-tuning of monolingual and multilingual models, zero-shot learning, retrieval-based approaches, and Large Language Model prompting. One of the main contributions of this work is BERTouch, our BERT-based language model for intent classification in Darija. BERTouch achieved F1-scores of 0.98 for Darija and 0.96 for MSA on DarijaBanking, outperforming the state-of-the-art alternatives including GPT-4 showcasing its effectiveness in the targeted application.

## Introduction
The field of Natural Language Processing (NLP), particularly with the rise of Large Language Models (LLMs), is revolutionizing industries where customer engagement is crucial. In retail banking, Financial NLP and LLMs are transforming client interactions, enhancing personalization, responsiveness, and customer satisfaction. Within generative AI-enhanced customer service, LLMs like GPT-4 orchestrate various components to deliver contextually relevant interactions. Retrieval Augmented Generation (RAG) enriches these interactions with information from a dense knowledge base. A key element in this setup is the Intent Classification Module, crucial for deciphering user inputs and initiating appropriate chatbot actions. Intent classification, a challenging task due to the terse nature of user utterances and the vast variety of potential intents, requires a large dataset for accurate detection.

## Contributions
The main contributions of our paper are:

- The **DarijaBanking dataset** is introduced, serving as a novel resource for banking intent detection in Darija, featuring over 7,200 multilingual queries across English, French, MSA, and Darija across 24 intent categories. This dataset results from arabizing, localizing, deduplicating, cleansing, and translating existing English banking data.
- A **comparative analysis** of intent classification methodologies is presented, evaluating monolingual and multilingual model fine-tuning, zero-shot learning, retrieval strategies, and LLM prompting, to assess their effectiveness across the dataset.
- **BERTouch** our Darija specific BERT-based language model, that is tailored for the intent classification task. BERTouch proved to be competitive with state-of-the-art solution including large language models such as GPT-4. As a contribution to open science, we made BERTouch publicly available in the HuggingFace platform.
- **Insights for enhancing Moroccan Darija banking intent detection systems** are detailed, highlighting the balance between using generalist LLMs, cross-lingual transfer learning, and the importance of domain-specific data annotation. Our findings indicate the advantage of specialized classifiers with sufficient data labeling and the efficacy of retrieval-based approaches as a budget-friendly option, guiding the development of precise and economical systems.
  
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
| aubmindlab/bert-base-arabertv02-twitter       | AbderrahmanSkiredj1/BERTouch                            | Arabic, Darija                          |
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

The models listed are currently private, except for the model AbderrahmanSkiredj1/BERTouch which is public, but you can send a request if you would like to gain access to them. The dataset is openly available at https://huggingface.co/datasets/AbderrahmanSkiredj1/DarijaBanking
