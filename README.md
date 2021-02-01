# archeo-bertje
A Dutch BERT model for the Archaeology domain

This model is based on the Dutch BERTje model by wietsedv (https://github.com/wietsedv/bertje)

We finetuned BERTje with a corpus of ~650 million Dutch excavation reports from the DANS data archive.

The archeo-bertje folder contains the finetuned ArcheoBERTje model. The archeo-bertje-NER folder contains the same model but trained for archaeological NER, targeting the following entities:

- Time periods
- Places
- Artefacts
- Contexts
- Materials
- Species
