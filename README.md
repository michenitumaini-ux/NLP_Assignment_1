# N-Gram Language Model with Smoothing Techniques

This project implements and evaluates statistical N-Gram language models using the IMDB Movie Review Dataset. The notebook explores different smoothing techniques and compares their performance using perplexity and cross-validation.

## Project Overview

The notebook covers the following:

* Data loading and preprocessing
* Tokenization and sentence preparation
* N-Gram generation and frequency counting
* Maximum Likelihood Estimation (MLE)
* Smoothing techniques:

  * Laplace (Add-One) Smoothing
  * Good-Turing Discounting
  * Kneser-Ney Smoothing
* Perplexity evaluation
* K-Fold Cross-Validation
* Data visualization and performance analysis

The project demonstrates how probabilistic language models work and how smoothing improves predictions for unseen word sequences.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* NLTK
* KaggleHub
* Jupyter Notebook

---

# Dataset

The project uses the **IMDB Movie Review Dataset** for training and evaluation.

Dataset features:

* Movie review text
* Sentiment labels
* Large vocabulary suitable for language modeling

Example dataset path used in the notebook:

```python
C:/Users/USER/Desktop/NLP/IMDB Dataset.csv
```


---

# Project Structure

```bash
Assignment_1.ipynb
```

The notebook is divided into the following sections:

## Step 1: Data Preparation

* Load dataset
* Clean and preprocess text
* Tokenize sentences
* Train/Test split

## Step 2: Implement N-Gram Models

* Generate unigrams, bigrams, trigrams, and 4-grams
* Compute frequency counts
* Calculate MLE probabilities

## Step 3: Apply Smoothing Techniques

* Laplace smoothing
* Good-Turing smoothing
* Kneser-Ney smoothing

## Step 4: Evaluate Model Performance

* Perplexity calculation
* K-Fold Cross-Validation

## Step 5: Visualization and Analysis

* Perplexity comparison plots
* Bar chart comparisons
* Frequency distribution analysis
* Final analysis report

---

# Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

Install required dependencies:

```bash
pip install nltk numpy pandas matplotlib kagglehub
```

---

# Running the Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```bash
Assignment_1.ipynb
```

Run all cells sequentially.

---

# Key Concepts Covered

## N-Gram Language Models

An N-Gram model predicts the next word based on the previous (n-1) words.

Examples:

* Unigram → single words
* Bigram → pairs of words
* Trigram → sequences of three words

---

## Smoothing Techniques

### 1. Laplace Smoothing

Adds one to all counts to avoid zero probabilities.

### 2. Good-Turing Discounting

Adjusts probabilities for unseen events based on frequency of frequencies.

### 3. Kneser-Ney Smoothing

A more advanced smoothing method that improves probability estimation using continuation probabilities.

---

# Evaluation Metric

## Perplexity

Perplexity measures how well a language model predicts a sequence of words.

Lower perplexity indicates better model performance.

---

# Visualizations

The notebook generates:

* Perplexity vs N-Gram size plots
* Smoothing method comparison charts
* N-Gram frequency distribution graphs

These visualizations help compare model effectiveness and analyze language patterns.

---

# Learning Outcomes


* How statistical language models work
* The importance of smoothing techniques
* How to evaluate NLP models using perplexity
* How different N-Gram orders affect performance
* Practical implementation of NLP concepts in Python

---

# Future Improvements

Possible extensions for this project:

* Implement neural language models
* Add stemming and lemmatization
* Use larger datasets
* Compare with transformer-based models
* Optimize memory usage for higher-order N-Grams

---


---

# License

This project is for educational and academic purposes.
