# nlp-core

A hands-on learning journal for **Natural Language Processing (NLP)** — teaching computers to read and understand human language.

Each notebook explains every step in plain English (a note above each code cell), so it's easy to review later even without an NLP background.

## 📚 Contents

### 01 — NLP Foundation

| # | Notebook | What you'll learn |
|---|---|---|
| 1 | [Tokenization with NLTK](01_nlp-foundation/1.tokenization_nltk.ipynb) | Chopping text into sentences and words using `sent_tokenize`, `word_tokenize`, `wordpunct_tokenize` and `TreebankWordTokenizer` |
| 2 | [Stemming with NLTK](01_nlp-foundation/2.stemming.ipynb) | Reducing words to their root form with `PorterStemmer`, `RegexpStemmer` and `SnowballStemmer`, and where stemming falls short |
| 3 | [Lemmatization with NLTK](01_nlp-foundation/3.lemmatization.ipynb) | Turning words into real dictionary roots with `WordNetLemmatizer`, using part-of-speech (`pos`) tags, and how it compares to stemming |
| 4 | [Stopwords with NLTK](01_nlp-foundation/4.stopwords.ipynb) | Removing common low-meaning words with `stopwords`, then building a full cleaning pipeline (tokenize ➜ remove stopwords ➜ stem / lemmatize) on a real speech |
| 5 | [Parts of Speech Tagging](01_nlp-foundation/5.parts_of_speech.ipynb) | Labelling each word as noun, verb, adjective, … with `nltk.pos_tag`, reading Penn Treebank tags, and why stopwords should stay in while tagging |
| 6 | [Named Entity Recognition](01_nlp-foundation/6.named_entity_recognition.ipynb) | Finding people, places and organizations in text with `nltk.ne_chunk`, and the limits of NLTK's NER |

## 🛠️ Setup

Requires **Python 3.14+** and [uv](https://docs.astral.sh/uv/).

```bash
# 1. Install dependencies (creates .venv)
uv sync

# 2. Activate the virtual environment
source .venv/bin/activate

# 3. Download the NLTK data used by the notebooks
python -c "import nltk; nltk.download('punkt_tab'); nltk.download('wordnet'); nltk.download('stopwords'); nltk.download('averaged_perceptron_tagger_eng'); nltk.download('maxent_ne_chunker_tab'); nltk.download('words')"
```

Then open any notebook in VS Code / Jupyter and pick the **`.venv`** kernel.

## 📦 Dependencies

- [`nltk`](https://www.nltk.org/) — Natural Language Toolkit
- [`numpy`](https://numpy.org/) — needed by NLTK's named entity recognizer
- `ipykernel` — runs the notebooks inside the project's virtual environment

## 🗂️ Project structure

```
nlp-core/
├── 01_nlp-foundation/        # Basics: tokenization, stemming, lemmatization, stopwords, POS tagging, NER
│   ├── 1.tokenization_nltk.ipynb
│   ├── 2.stemming.ipynb
│   ├── 3.lemmatization.ipynb
│   ├── 4.stopwords.ipynb
│   ├── 5.parts_of_speech.ipynb
│   └── 6.named_entity_recognition.ipynb
├── main.py                   # Placeholder entry point
├── pyproject.toml            # Project config & dependencies
└── uv.lock                   # Locked dependency versions
```
