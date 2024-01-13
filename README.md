# Big-Data-Analysis-Rake-MongoDB-MRJob

## Overview
This assignment focuses on extracting and analyzing data from tweets using various Natural Language Processing (NLP) techniques. The project is divided into five main tasks, each addressing different aspects of data processing and analysis.

### Task 1: Keyword and Named Entity Extraction
This task involves extracting keywords and named entities from the tweet body using the Rake module and natural language processing techniques.

#### 1.1 Keyword Extraction
- Utilizes the Rake module to extract keywords from tweets.
- Implements `find_keywords_in_text()` function to process the text and return a CSV string of keywords.

#### 1.2 Named Entity Extraction
- Extracts named entities from the tweet body.
- Applies tokenization, stop word removal, word stemming, and POS tagging.
- The extracted entities are written to a text file and updated in the MongoDB database.

### Task 2: Word Occurrence Count
Objective: Count the occurrence of words in 10,000 tweets.

- Pre-processes tweet text (lowercasing, removing special characters, hyperlinks, etc.).
- Uses the MRJob library for MapReduce processing.
- The process involves mapping, shuffling, sorting, and reducing steps to count word occurrences.

### Task 3: Tweet Summarization by City
Focuses on summarizing the number of tweets related to each city in Australia.

- Extracts location information (country and city) from tweets.
- Uses MRJob for processing.
- The mapper separates ID and city, and the reducer sums up the tweet counts per city.

### Task 4: Tweet ID Sorting
Part 1: Sorts tweet IDs using the QuickSort algorithm in MRJob.
Part 2: Implements a merge sort function for direct sorting of tweet IDs.

- Compares the efficiency of MRJob and direct Merge Sort for different data sizes.
- Explains the suitability of each approach based on dataset size.

### Task 5: TF-IDF Calculation
Objective: Calculate TF-IDF scores for keywords in tweets.

- Implements a pipeline using Dask for large-scale data processing.
- Calculates TF-IDF scores to identify significant keywords in the dataset.

## Limitations and Possible Improvements
- The approach may not handle informal text elements like misspellings or slang effectively.
- Does not consider the sentiment or context of keywords.
- Limited to single-word analysis, not considering n-grams.
- Suggested improvements include using a robust tokenizer, spell-checker, extending analysis to n-grams, incorporating sentiment analysis, and optimizing Dask usage for better parallelism.

## Additional Notes
- Ensure MongoDB is set up and accessible for tasks involving database operations.
- Install all required libraries (e.g., NLTK, MRJob, Dask) before running the scripts.


