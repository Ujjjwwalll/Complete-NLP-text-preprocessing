# NLP Text Preprocessing

My notes and practice code for the basic NLP text preprocessing pipeline, split module wise so it is easy to follow. Most of the cleaning is done on the IMDB movie reviews dataset.

## Modules

| Notebook | What it covers |
|---|---|
| `01_text_cleaning.ipynb` | Lowercasing, removing HTML tags, URLs, punctuation, spelling correction, stopword removal, emoji handling |
| `02_tokenization.ipynb` | Word, sentence, wordpunct, Treebank tokenizers and spaCy |
| `03_stemming_and_lemmatization.ipynb` | Porter, Regexp and Snowball stemmers, WordNet lemmatizer |
| `04_pos_tagging_and_ner.ipynb` | POS tagging and Named Entity Recognition using NLTK |
| `05_text_vectorization.ipynb` | Bag of Words and TF-IDF |
| `06_word_embeddings.ipynb` | Word2Vec (skip-gram) using gensim |

## Libraries used

`numpy`, `pandas`, `nltk`, `spacy`, `textblob`, `emoji`, `scikit-learn`, `gensim`

```bash
pip install numpy pandas nltk spacy textblob emoji scikit-learn gensim
python -m spacy download en_core_web_sm
```

NLTK data is also needed (run once):

```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')
```

## Dataset

`01_text_cleaning.ipynb` uses the [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) from Kaggle. Download `IMDB Dataset.csv` and keep it in the same folder as the notebook.

## How to run

Go in order from `01` to `06`. Every notebook runs on its own, so you can also open any one of them directly.

## Note

The NER tree in `04` opens in a pop-up window, so it may not show on cloud notebooks like Colab.
