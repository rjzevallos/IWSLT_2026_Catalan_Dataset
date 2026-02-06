# IWSLT2026-Low-resource Speech Translation Track: Catalan-English Parallel Corpus

Catalan (català) is a Western Romance language which has approximately 4.1 million L1 speakers and more than 10 million people who can speak the language across its territories. It is spoken primarily in Catalonia, the Valencian Community, the Balearic Islands, and parts of Aragon in Spain, as well as in Andorra, where it is the sole official language. Catalan is also spoken in parts of southern France (Northern Catalonia) and in the city of Alghero in Sardinia, Italy.

In Catalonia, the Valencian Community, and the Balearic Islands, Catalan is co-official with Spanish and is widely used in education, media, and public administration. It is recognized as a regional or minority language in several European regions and has the ISO 639-1 code ca.

This repository provides a synthetic Catalan–English parallel corpus created for the [IWSLT 2026](https://iwslt.org/2026/) Catalan-English translation task. This dataset is created from the first ~15h of Catalan speech data (11.87h for train and 5.15h for validation) from Mozilla Common Voice [1] and synthetically translated into English to create aligned text pairs using [Helsinki-NLP/opus-mt-ca-en](https://huggingface.co/Helsinki-NLP/opus-mt-ca-en) [2].


## Download dataset

```python
BASE = "/path/to/ca_en_synthetic_translation"
data_files = {
    "train": f"{BASE}/train/data-00000-of-00001.arrow",
    "validation": f"{BASE}/val/data-00000-of-00001.arrow",
}

dataset = load_dataset("arrow", data_files=data_files)
``` 

## Authors

* Rodolfo Zevallos (Barcelona Supercomputing Center)
* Marc Casals i Salvador (Barcelona Supercomputing Center)
* Guillermo Cámbara Ruiz (Universitat Pompeu Fabra)
* John Ortega (Northeastern University)
* Fabrício Carraro (Barcelona Supercomputing Center)

## Evaluation
You can evaluate your model using two widely adopted translation metrics: BLEU and ChrF++.


## License
This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivs 3.0 Unported License](https://creativecommons.org/licenses/by-nc-nd/3.0/).

## References
[1] Ardila, R., Branson, M., Davis, K., Henretty, M., Kohler, M., Meyer, J., Morais, R., Saunders, L., Tyers, F. M., & Weber, G. (2019, December 13). Common Voice: A Massively-Multilingual Speech Corpus. arXiv.Org. https://arxiv.org/abs/1912.06670v2

[2] Gibert, O. de, Attieh, J., Vahtola, T., Aulamo, M., Li, Z., Vázquez, R., Hu, T., & Tiedemann, J. (2025). Scaling Low-Resource MT via Synthetic Data Generation with LLMs (arXiv:2505.14423). arXiv. https://doi.org/10.48550/arXiv.2505.14423

