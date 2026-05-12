# MLK Rhetoric Analysis

## Computational Analysis of Linguistic Elevation in Martin Luther King Jr.’s Speeches

This project explores rhetorical movement in the speeches and sermons of Martin Luther King Jr. through computational linguistic analysis.

The original goal of the project was to investigate whether MLK’s rhetorical power emerged from shifts between simple and sophisticated language over time. Using NLP feature engineering, I constructed a **linguistic elevation score** to measure sentence-level variation in:

* sentence length,
* syllabic complexity,
* rare-word usage,
* and abstract language.

Rather than finding dramatic swings between linguistic simplicity and sophistication, the analysis revealed something more interesting: MLK’s language remains relatively stable across many speeches. This suggests that the power of his communication may come less from changing vocabulary complexity and more from delivery, cadence, and vocal performance — directions identified for future work.

---

# Project Goals

This repository investigates three questions:

1. Can rhetorical “elevation” be operationalized computationally?
2. Does MLK alternate between grounded simplicity and elevated abstraction in patterned ways?
3. What can quantitative analysis reveal — and fail to reveal — about rhetorical charisma?

---

# Methodology

## Data

The dataset consists of 17 manually collected MLK speeches and sermons transcribed from archival audio recordings.

Each transcript was:

* cleaned,
* sentence-segmented,
* and analyzed at the sentence level.

---

## Linguistic Elevation Score

Each sentence receives a composite **linguistic elevation score** built from the following features:

| Feature                    | Description                                                    |
| -------------------------- | -------------------------------------------------------------- |
| Word count                 | Length/extension of the sentence                               |
| Average syllables per word | Phonological complexity                                        |
| Rare word ratio            | Use of uncommon language                                       |
| Abstract word ratio        | Use of conceptual, philosophical, moral, or religious language |

Features were transformed and normalized before being combined into a weighted composite score.

---

## Sequential Rhetorical Analysis

After constructing the linguistic elevation score, sentences were classified into rhetorical states relative to MLK’s own stylistic baseline using z-scores:

* **Simple**
* **Medium**
* **Sophisticated**

This allowed the project to analyze:

* rhetorical transitions,
* recurring movement patterns,
* and “dance-like” sequences between linguistic states.

The project treats rhetorical movement as sequential rather than static.

---

# Key Finding

One of the most important findings was actually the relatively **low variance** of the linguistic elevation scores.

Rather than dramatically oscillating between simple and sophisticated language, MLK tends to maintain a remarkably stable rhetorical register across speeches.
---

# Repository Structure

```text
mlk_rhetoric_analysis/
├── data/
│   ├── raw_transcripts/
│   ├── cleaned_transcripts/
│   ├── linguistic_elevation/
│   └── segments/
├── notebooks/
│   ├── 01_text_cleaning.ipynb
│   └── 02_linguistic_analysis.ipynb
└── README.md
```

# Limitations

This project is exploratory in nature. 

Some limitations include:

* transcript quality variability,
* imperfect sentence segmentation,
* handcrafted feature definitions,
* and the difficulty of reducing rhetorical force to numerical metrics.

The project is intended less as a final model and more as a computational framework for thinking about rhetoric, language, and performance.

---

# Why I Built This

I’m interested in the intersection of:

* data science,
* communication,
* oral tradition,
* and human interpretation.

This project allowed me to combine technical analysis with questions that are fundamentally cultural, rhetorical, and humanistic — exploring not just what language means, but how it moves people.
