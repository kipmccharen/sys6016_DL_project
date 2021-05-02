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

## Bash Commands to run in Google Colab

!pip install speechbrain
!pip install transformers
!git clone https://github.com/kipmccharen/sys6016_DL_project

%cd ..
!gdown --id '1EIfBmwiT0RF3-U81-Qu5K4J27N31BdB5'  ## speechbrain_s2s_wav2vec_ckpt.zip
!unzip speechbrain_s2s_wav2vec_ckpt.zip
!rm speechbrain_s2s_wav2vec_ckpt.zip

%cd /content/data/trainwav2vec/save/

!python sys6016_DL_project/train_with_wav2vec2.py sys6016_DL_project/hparams/train_with_wav2vec2.yaml --data_folder /content/data/ --output_folder /content/data/trainwav2vec/ --new_json /content/data/new_train.json