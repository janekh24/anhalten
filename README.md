# ANHALTEN: Cross-Lingual Transfer for German Token-Level Reference-Free Hallucination Detection

Authors: Janek Herrlein, Chia-Chien Hung, Goran Glavaš 

ACL 2024. SRW: https://arxiv.org/pdf/2407.13702

## Introduction

Research on token-level reference-free hallucination detection has predominantly focused on English, primarily due to the scarcity of robust datasets in other languages. This has hindered systematic investigations into the effectiveness of cross-lingual transfer for this important NLP application. To address this gap, we introduce **ANHALTEN**, a new evaluation dataset that extends the English hallucination detection dataset to German. To the best of our knowledge, this is the first work that explores cross-lingual transfer for token-level reference-free hallucination detection. ANHALTEN contains gold annotations in German that are parallel (i.e., directly comparable to the original English instances). We benchmark several prominent cross-lingual transfer approaches, demonstrating that larger context length leads to better hallucination detection in German, even without succeeding context. Importantly, we show that the sample-efficient few-shot transfer is the most effective approach in most setups. This highlights the practical benefits of minimal annotation effort in the target language for reference-free hallucination detection.


## Citation
If you use any source codes, or datasets included in this repo in your work, please cite the following paper:
<pre>
@article{herrlein2024anhalten,
  title={ANHALTEN: Cross-Lingual Transfer for German Token-Level Reference-Free Hallucination Detection},
  author={Herrlein, Janek and Hung, Chia-Chien and Glava{\v{s}}, Goran},
  journal={arXiv preprint arXiv:2407.13702},
  year={2024}
}
</pre>


## Pretrained Models
The pre-trained models can be easily loaded using huggingface [Transformers](https://github.com/huggingface/transformers) or Adapter-Hub [adapter-transformers](https://github.com/Adapter-Hub/adapter-transformers) library. Following pre-trained versions are supported:
* `bert-base-multilingual-cased`: mBERT 
* `xlm-roberta-base`: XLM-R
* `en/wiki@ukp`: Adapter trained on English Wiki
* `de/wiki@ukp`: Adapter trained on German Wiki

The scripts for downstream tasks are mainly modified from [here](https://github.com/microsoft/HaDes), where there might be slight version differences of the packages, which are noted down in the `requirements.txt` file.


## Structure
This repository is currently under the following structure:
```
.
└── Code
└── Data
└── README.md
```