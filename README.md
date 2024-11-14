# Web Scraping and NLP with Requests, BeautifulSoup, and spaCy

This project leverages Natural Language Processing (NLP) techniques using Python and spaCy to analyze the content of an article. The main goals are to identify and rank frequent words and concepts, score sentences based on word relevance, and visualize the distribution of interesting terms.

## Overview

The project performs the following key tasks:

* Text Extraction and Processing: Loads article content from an HTML file, parses it, and extracts meaningful text data.
* Tokenization and Lemmatization: Analyzes the article text to identify the most frequent tokens and their base forms (lemmas), filtering out irrelevant elements like punctuation, stopwords, and whitespace.
* Sentence Scoring: Scores sentences based on the concentration of selected "interesting" words or concepts, allowing for relevance-based analysis of sentence structure.
* POS-based Filtering: Modifies word selection criteria to focus on specific parts of speech (nouns), refining the analysis to more relevant terms in the context of the article’s subject.
* Visualization: Plots histograms of sentence scores to observe the distribution and concentration of interesting terms throughout the text.

## Requirements
* Python 3.x
* Libraries:
    * pickle: For loading and saving serialized data.
    * BeautifulSoup (from bs4): For HTML parsing.
    * spaCy: For natural language processing (NLP).
    * matplotlib: For data visualization.
    * collections: For counting word frequencies.
* spaCy Language Model: en_core_web_sm (Install with python -m spacy download en_core_web_sm)

## Installation
Install the required libraries and spaCy model using:

pip install spacy bs4 matplotlib
python -m spacy download en_core_web_sm

## Running the Project
1. Ensure that the article’s HTML content is saved as a .pkl file for loading into the project.
2. Run the code in a Jupyter notebook or Python script to analyze the article, calculate sentence scores, and generate visualizations.
3. Modify the "interesting" words list or part-of-speech filters as needed to adjust the focus of the analysis.

## Key Functions
* Token and Lemma Frequency Analysis: Identifies the most common terms in the article, helping to highlight the main topics and repeated concepts.
* Sentence Scoring: Scores sentences based on the presence of important terms, allowing for relevance ranking within the text.
* Visualization: Histogram plots show the distribution of sentence scores, providing insights into how frequently key terms appear across sentences.

## Visualization and Interpretation
The histograms of sentence scores allow for easy interpretation of the text’s structure:

* High-Frequency Terms: Tokens and lemmas that appear most frequently can indicate the main subjects and themes of the article.
* POS Filtering: By focusing on nouns or other specific parts of speech, the analysis can be tailored to emphasize concepts or entities over actions or attributes.