# Abstractive Text Summarization

## The Algorithm
<http://arxiv.org/abs/1509.00685>

Our implementation differs in that we fix the context and summary token of the
embedding matrix. 

-Both embedding matrices are initialised from GloVe

Helptext:

```bash
python3 main.py -h
```

The training datasets are under `data/`. Each JSON file contains three fields `title`, `full_text`, `summary`. They're downloaded with scripts in `download_data/`.

GloVe data needs to be downloaded and unzipped under `glove/`. The code uses the first 10k most frequent tokens by default. To generate the embeddings for them, 

```bash
cd glove
head -n 10000 glove.6B.300d.txt >glove.10k.300d.txt
```
