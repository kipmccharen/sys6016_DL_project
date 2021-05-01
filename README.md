# sys6016_DL_project

Originally from https://github.com/speechbrain/speechbrain/tree/develop/recipes/TIMIT/ASR/seq2seq

## TIMIT ASR with seq2seq models.
This folder contains the scripts to train a seq2seq RNNN-based system using TIMIT.
TIMIT is a speech dataset available from LDC: https://catalog.ldc.upenn.edu/LDC93S1

## How to run
python train.py train/train.yaml

## Results

| Release | hyperparams file | Val. PER | Test PER | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:| :-----------:|
| 21-04-08 | train_with_wav2vec2.yaml |  7.11 | 8.04 | https://drive.google.com/drive/folders/1-IbO7hldwrRh4rwz9xAYzKeeMe57YIiq?usp=sharing | 1xV100 32GB |
