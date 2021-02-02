# ArcheoBERTje
A Dutch BERT model for the Archaeology domain

This model is based on the Dutch BERTje model by wietsedv (https://github.com/wietsedv/bertje).

We finetuned BERTje with a corpus of ~60k Dutch excavation reports (~650 million tokens) from the DANS data archive (https://easy.dans.knaw.nl/ui/home).

The archeo-bertje folder contains the finetuned ArcheoBERTje model. The archeo-bertje-NER folder contains the same model but trained for archaeological NER, targeting the following entities:

- Time periods
- Places
- Artefacts
- Contexts
- Materials
- Species

The training-data folder contains the training data for NER, split up into 5 folds, with sentences shortened to max 90 tokens. For each fold, 1 document group is the test set, 1 document group is the dev set, and the remaining 3 document groups is the train set. The archeo-bertje-NER model is trained on fold 2.

You can find the fold split below:

| Fold  | DANS IDs | No. Docs | Tokens | Entities|
| ------------- | ------------- | ------------- | ------------- | ------------- |
| 1  | 48036, 33649, 33513  | 3  | 91k  | 5,385   |
| 2  | 29580, 38589, 33620  | 3  | 91k  | 7,042   |
| 3  | 53631, 46229  | 2  | 80k  | 5,902   |
| 4  | 38589, 49541, 56943  | 3  | 86k   | 6,499  |
| 5  | 55391, 33527, 59132, 33460  | 4  | 92k  | 6,393   |
| TOTAL | | 15 | 440k | 31,221