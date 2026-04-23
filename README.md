# UncCy: A SpaCy Parser for Uncial Manuscripts
<img src="https://github.com/SphRbtHyk/unccy/blob/main/assets/unccy.jpeg" alt="logo" width="200"/>


Uncial manuscripts have several distinctive features that render current parsers unusable for working on manuscript transcriptions: **(1)** they do not use diacritics; **(2)** they contain spelling variations linked to the evolution of Greek during the first centuries AD. `UncCy` is a parsing library for **lemmatization**, **part of speech classification** and **morphological analysis** that supports both Greek without diacritics and is resilient to the spelling variations observed in New Testament uncials copied between the 4th and 6th centuries.

## Usage

`UncCy` is fully compatible with the `spaCy` API. The model itself is hosted on *HuggingFace*.

You need first to run the installation of `spacy`, as well as of the corresponding wheel:
```bash
pip install spacy spacy-transformers
pip install https://huggingface.co/SphRbtHyk/grc_unccy/resolve/main/grc_unccy-1.0.0-py3-none-any.whl
```

You can then use `uncCy` using the standard `spaCy` API.

```python
import spacy
nlp = spacy.load("grc_unccy")

doc = nlp("εν αρχη ην ο λογος")
for token in doc:
    print(token.text, token.pos_, token.lemma_)
```

## Training data
This parser was trained on three of the oldest manuscripts of the four Gospels (Matthew, Mark, Luke and John) and 4 Pauline Epistles (Galatians, 1 and 2 Corinthians, Romans):
- Manuscript Vaticanus (IVth century)
- Manuscript Alexandrinus (Vth century)
- Manuscript Sinaïticus (IVth century)

The data is available, using spaCy binary format, in the `datasets` folder.

## 📖 Citation
If you use this library, please cite this work using:

```bibtex
@inproceedings{2026unccy,
  title={UncCy: Neural Parsing of New Testament Greek Manuscripts via Collation-Based Annotation Transfer,
  author={Sophie Robert-Hayek},
  booktitle={Pre-print},
  year={2026}
}
```