# Indonesian NER using BiLSTM+CRF+IndoBERT
This model is used to predict named entities in Indonesian text utilizing BiLSTM and CRF architecture, and IndoBERT. The model is built by modifying an existing NER: https://github.com/PeijiYang/BERT-BiLSTM-CRF-NER-pytorch.
  
## Datasets
The model uses datasets provided by IndoNLU: https://github.com/indobenchmark/indonlu

## Training Dataset Format
Training dataset is in BIO format. These are some examples:
```
Produser	O
David	B-PERSON
Heyman	I-PERSON
dan	O
sutradara	O
Mark	B-PERSON
Herman	I-PERSON
sedang	O
mencari	O
seseorang	O
yang	O
mampu	O
memerankan	O
tokoh	O
utama	O
yang	O
lugu	O
,	O
sehingga	O
mereka	O
meminta	O
setiap	O
anak	O
apa	O
yang	O
mereka	O
tahu	O
tentang	O
Holocaust	O
.	O
```
## How to run
Training and test processes can be performed at the same time using this syntax:
```
python ner.py --do_train True     --do_eval True     --do_test True     --max_seq_length 25  --train_batch_size 8     --eval_batch_size 8     --num_train_epochs 10     --do_lower_case     --logging_steps 200     --need_birnn True     --rnn_dim 256     --clean True
```
