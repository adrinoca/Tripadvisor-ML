# Tripadvisor-ML
In this project I am going to make an analysis of reviews made in tripadvisor to different hotels. I will then develop a deeplearning model to predict the ratings based on people's opinions.

## Fases of creating a Machine Learning Model for text
There are differenciated fases to create a Deep Learning model for text.

### Tokenization

1. Text Cleaning
- Noise Removal: Eliminate unwanted characters such as HTML tags, special symbols, or unnecessary punctuation.
- Normalization: Convert text to a standard format, like transforming all text to lowercase, to reduce complexity.

2. Tokenization
- Splitting Text into Tokens: Tokens are usually words or characters. This stage converts large blocks of text into more manageable units for analysis.

3. Post-Tokenization Cleaning
- Stop Words Removal: Common words that typically don't contribute to the text's meaning, like "the", "and", "in", are removed.
- Stemming and Lemmatization: Reduce words to their root or base form. For example, changing "running" to "run" (lemmatization) or to "runn" (stemming).

4. Token Encoding
- One-hot Encoding: Represent each token as a vector where one element is 1 and the rest are 0, indicating the presence of the token in the text.
- Word Indexing: Assign each unique word a numerical index, creating a word-index dictionary.
- Word Embeddings: Use dense vectors to represent words, where each word's embedding captures semantic aspects based on its use in the training corpus. Common examples include Word2Vec, GloVe, and task-specific trained embeddings.

5. Sequence Preparation
- Padding: Deep learning models require inputs of uniform size, so zeros are added (or tokens are trimmed) to ensure all sequences have the same length.
- Data Splitting: Separate the data into training, validation, and test sets to train the model and evaluate its performance.