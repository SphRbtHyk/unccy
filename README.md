# UncCy: A SpaCy Parser for Uncial Manuscripts

Uncial manuscripts have several distinctive features that render current parsers unusable for working on manuscript transcriptions: **(1)** they do not use diacritics; **(2)** they contain spelling variations linked to the evolution of Greek during the first centuries of our era. `UncCy` is a parsing library for **lemmatization**, **part of speech classification** and **morphological analysis** that supports both Greek without diacritics and is resilient to the spelling variations observed in New Testament uncials copied between the 4th and 6th centuries.

## Usage

`UncCy` is fully compatible with the `spaCy` API. The model itself is hosted on *HuggingFace*.

```

```

## Training data
This parser was trained on three manuscripts of the four Gospels () and Pauline of Epistles ():
- Manuscript Vaticanus ()
- Manuscript Alexandrinus ()
- Manuscript Sinaïticus ()

The data is available, using spaCy binary format, in the `datasets` folder.

## Learn more
The companion paper to the UncCy library is available here as a pre-print:

## 📖 Citation
If you use this library, please cite this work using:

```bibtex
@inproceedings{yourname2025unccy,
  title={UncCy: Silver and Gold Treebanks for Neural Parsing of Koinè Greek Manuscripts},
  author={Sophie Robert-Hayek},
  booktitle={Pre-print},
  year={2026}
}
```