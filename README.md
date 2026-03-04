# Evaluating Machine Translation for Public Service Announcements (PSAs)

## Project Overview

Public Service Announcements (PSAs) play an important role in informing communities about safety, security, and public awareness issues. In multilingual regions, these messages must often be translated into multiple languages to ensure accessibility.

This project evaluates the performance of neural machine translation models when translating PSAs into Somali. The study investigates whether multi step translation affects translation accuracy compared with direct translation.

The project uses the **No Language Left Behind (NLLB) model** developed by Meta and evaluates translation quality using the **BLEU score**, a standard metric for machine translation evaluation.

---

## Objectives

This project focuses on the following tasks:

### 1. Translation from Swahili to Somali
Public Service Announcements are translated from Swahili into Somali using a neural machine translation model.

### 2. Back Translation
The Somali translations are translated back into English to evaluate whether the original meaning of the messages is preserved.

### 3. BLEU Score Evaluation
The BLEU score is calculated to quantitatively measure the quality of the round trip translation.

### 4. Direct English to Somali Translation Evaluation
The original English PSAs are translated directly into Somali and a BLEU score is calculated. This allows comparison between direct translation and multi step translation to determine whether multiple translations reduce accuracy.

---

## Translation Model

This project uses the **NLLB model** available through the Hugging Face Transformers library.

Model used:

```
facebook/nllb-200-distilled-600M
```

This model supports translation across many languages including English, Swahili, and Somali.

---

## Project Workflow

The translation pipeline follows these steps:

1. Load the PSA dataset  
2. Translate the text into Somali  
3. Perform back translation into English  
4. Compute BLEU score for translation evaluation  
5. Perform exploratory text analysis on the PSA dataset  

---

## Text Analysis

In addition to translation evaluation, the project includes exploratory analysis of the PSA dataset.

### Word Count Distribution

The number of words in each PSA is calculated to analyze the length distribution of the announcements.

### Word Frequency Analysis

The most common words in the dataset are extracted after removing stop words. This helps identify the dominant themes present in the PSAs.

### Word Cloud

A word cloud is generated to visually represent the most frequent words appearing in the PSA dataset.

---

## Technologies Used

- Python  
- Pandas  
- Hugging Face Transformers  
- PyTorch  
- SacreBLEU  
- Matplotlib  
- WordCloud  

---

## Evaluation Metric

Translation quality is measured using the **BLEU score (Bilingual Evaluation Understudy)**.

BLEU score interpretation:

| Score Range | Interpretation |
|-------------|---------------|
| 0 – 10 | Poor translation |
| 10 – 25 | Understandable but contains errors |
| 25 – 40 | Good translation |
| Above 40 | Very high quality translation |

This metric compares machine generated translations with reference translations to evaluate how closely they match.

---

## Repository Structure

```
project/
│
├── data/
│   └── PSA datasets
│
├── notebooks/
│   └── Translation and analysis notebooks
│
├── results/
│   └── BLEU score outputs and visualizations
│
└── README.md
```

---

## Results

The BLEU scores obtained from the experiments allow comparison between:

- Multi step translation (Swahili → Somali → English)  
- Direct translation (English → Somali)

This comparison helps determine whether translation accuracy is affected by using multiple intermediate languages.

---

## Future Work

Possible extensions of this project include:

- Evaluating additional translation models  
- Applying semantic similarity metrics such as BERTScore  
- Expanding the dataset to include more PSAs  
- Testing translation performance across additional languages  

---

## Contributors

This project was completed collaboratively as part of a machine translation analysis study by:

**Faniyo Noor**  
**Nafisah Adams** 

BSc Data Science and Analytics  
