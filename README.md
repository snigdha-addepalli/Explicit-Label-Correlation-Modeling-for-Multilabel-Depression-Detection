# CS6140 Final Project – Team 23
## Depression Emotion Classification with Explicit Label Attention

This repository contains implementations of three models for multilabel
depression emotion classification on Reddit data.

## Repository Structure
- `Model A`: SVM + Classifier Chain
- `Model B`: BERT + Label Attention Network 
- `Model C`: BiLSTM + Label Attention Network (LSTM-LAN)

## Setup
pip install -r requirements.txt

## Run Model A (SVM)
open and run:
src/Model_A/Model_A_SVM.ipynb

## Run Model B (BERT-LAN)
python src/Model_B/bert_lan.py

## Run Model c (LSTM-LAN)

This project uses GloVe 6B 300d embeddings.

Download from GitHub Releases:
- https://github.com/itskhushee/CS6140_TEAM23_DEPRESSION_EMOTION_CLASSIFICATION/releases/download/artifact/glove.6B.300d.txt

After downloading, place the file at: src/Model_C/glove/glove.6B.300d.txt
Place the .txt file inside the glove folder.
### To train the explicit label-correlation LSTM model (Model C), run:

```bash
python src/Model_C/train_explicit.py
```

For testing, evaluation, and visualization of results , open and run:

```bash
src/Model_C/test_explicit.ipynb
```

### For comparison the baseline implicit LSTM model code is available.
To train implicit model

```bash
python src/Model_C/train_implicit.py
```
For testing:
```bash
src/Model_C/test_implicit.ipynb
```