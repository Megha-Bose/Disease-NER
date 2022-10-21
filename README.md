# Disease-NER
Given a medical diagnosis, identifying medical conditions within the text and mapping them to standardized medical encodings.

## Data
The data directory contains:
- The disease mentions from the text files stored in entities.tsv.
- Text files containing the medical textual data in the text directory.

The data is taken from the English version of multilingual resources of the DisTEMIST 2022 task: https://zenodo.org/record/6532684  

## Pre-processing
The pre-processing stage involves:
- Splitting medical text in each file into sentences.
- Tokenizing the sentences into words/tokens.
- Calculating IOB tags for the tokens for named entity recognition (NER) task.

## NER Task
Two Types of Models are built:
- The entire clinical case is given as input
- Sentence based Tokenization

The basic models used are : 
- https://huggingface.co/d4data/biomedical-ner-all
- https://huggingface.co/pucpr/clinicalnerpt-medical

Disease mentions identification is built as a Token classification problem