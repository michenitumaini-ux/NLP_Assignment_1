## Hate Speech Analysis Project

This project focuses on analyzing a Hate Speech dataset to identify common themes, preprocess text data, and visualize key insights.

### Project Goal

The primary objective is to load a raw text dataset, perform a series of text preprocessing steps (cleaning, tokenization, stemming, lemmatization, stop-word removal), and then visualize the characteristics of the cleaned text to gain insights into the dataset's content.

### Setup and Installation

To run this notebook, you'll need to install the following Python libraries:

```bash
!pip install textblob wordcloud
```

Additionally, several NLTK data packages are required. These will be downloaded automatically when the notebook runs:

*   `punkt_tab`
*   `stopwords`
*   `wordnet`

### Data Loading and Preprocessing

1.  **Data Loading**: The project loads a CSV file (`OmbuiHSRaw.csv`) into a pandas DataFrame.
2.  **Duplicate Removal**: Duplicate entries based on the `tweet` column are identified and removed to ensure data integrity and prevent bias in analysis.
3.  **Text Preprocessing Pipeline**: A custom preprocessing function (`class_style_preprocessing`) is applied to the `tweet` column, which performs the following steps:
    *   Removes HTML tags and non-alphabetic characters.
    *   Handles whitespace and extra spaces.
    *   Converts text to lowercase (normalization).
    *   Tokenizes the text into individual words.
    *   Removes common English stopwords.
    *   Applies lemmatization and Snowball stemming to reduce words to their root forms, consolidating vocabulary.
    
    *(Note: A resource-intensive spelling correction step using `TextBlob().correct()` was temporarily commented out for faster execution on large datasets.)*

### Visualizations

Two main visualizations are generated to explore the preprocessed text:

1.  **WordCloud**: A visual representation of the most frequent words in the cleaned text, where the size of each word indicates its frequency.
2.  **Word Frequency Histogram**: A bar plot showing the top 20 most frequent words and their counts, providing a quantitative view of prominent terms.
3.  **Word Count Drift (KDE Plot)**: A Kernel Density Estimate plot illustrating the distribution of word counts before and after preprocessing, demonstrating the structural shift in text density.

### Summary of Insights Gained

1.  **Noise Extraction & Vocabulary Pruning**: The preprocessing successfully removed HTML tags, special characters, and extraneous whitespace, leading to a consolidated and cleaner vocabulary.
2.  **Structural Consolidation via Normalization**: Lowercasing, stemming, and lemmatization effectively reduced inflectional variations, ensuring that words with similar meanings are treated as a single feature, which is crucial for downstream modeling.
3.  **High-Frequency Term Profiling**: By eliminating common stopwords, the visualizations effectively highlighted the contextual root vocabulary of the dataset. This helps in quickly identifying actionable markers and potential abusive patterns, especially relevant in hate speech analysis.



---

# License

This project is for educational and academic purposes.
