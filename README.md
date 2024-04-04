# Tripadvisor-ML
In this project I am going to make an analysis of reviews made in tripadvisor to different hotels. I will then develop a deeplearning model to predict the ratings based on people's opinions.

## Fases of creating a Machine Learning Model for text
There are differenciated fases to create a Deep Learning model for text.

### Text Cleaning

- Noise Removal: Eliminate unwanted characters such as HTML tags, special symbols, or unnecessary punctuation.
- Normalization: Convert text to a standard format, like transforming all text to lowercase, to reduce complexity.

### Tokenization

- Splitting Text into Tokens: Tokens are usually words or characters. This stage converts large blocks of text into more manageable units for analysis.

### Post-tokenization cleaning

- Stop Words Removal: Common words that typically don't contribute to the text's meaning, like "the", "and", "in", are removed.
- Stemming and Lemmatization: Reduce words to their root or base form. For example, changing "running" to "run" (lemmatization) or to "runn" (stemming).

### Token Encoding

- One-hot Encoding: Represent each token as a vector where one element is 1 and the rest are 0, indicating the presence of the token in the text.
- Word Indexing: Assign each unique word a numerical index, creating a word-index dictionary.
- Word Embeddings: Use dense vectors to represent words, where each word's embedding captures semantic aspects based on its use in the training corpus. Common examples include Word2Vec, GloVe, and task-specific trained embeddings.

### Sequence Preparation

- Padding: Deep learning models require inputs of uniform size, so zeros are added (or tokens are trimmed) to ensure all sequences have the same length.
- Data Splitting: Separate the data into training, validation, and test sets to train the model and evaluate its performance.

## RNN Models
RNN (Recurrent Neural Networks) and LSTM (Long Short-Term Memory) models are particularly suited for working with sequential data, such as text, due to their unique features that allow them to effectively process sequential information. Here’s why they are correct and useful for tasks related to understanding text:

### Handling Variable-Length Sequences

Both text and speech are presented in sequences of variable length. RNNs and LSTMs are designed to handle sequences of any length, making them ideal for processing sentences and documents that can vary significantly in size.

### Short-Term and Long-Term Memory

LSTM models, a variant of RNNs, introduce memory cells that can maintain information over time, allowing them to remember important information and forget what is not relevant for the current task. This capability is crucial for understanding context and meaning in long text sequences, where dependencies between words may span long distances within the text.

### Capturing Temporal Dependencies

RNNs and LSTMs can capture temporal dependencies in data, meaning they can understand how words in a sentence or sentences in a paragraph relate to each other over time. This feature is fundamental for many natural language processing (NLP) tasks, like machine translation, where the meaning of a word can depend on the context provided by preceding or following words in the sentence.

### Modeling Relationships Between Words

As they process a text sequence, RNNs and LSTMs generate vector representations of words that capture not just the meaning of individual words but also their relationships and the context in which they appear. This is invaluable for tasks requiring deep text comprehension, such as sentiment analysis, question answering, and automatic summarization.

### Flexibility for Various NLP Tasks

RNNs and LSTMs are highly versatile and can be adapted to a wide range of NLP tasks, whether by adjusting the model architecture or pretraining on large text corpora to learn rich linguistic representations that can then be fine-tuned for specific tasks.
Despite their advantages, traditional RNNs often face difficulties with long-term dependencies due to issues like vanishing or exploding gradients during training. LSTMs and other variants, such as GRUs (Gated Recurrent Units), were specifically designed to address these challenges, making the models more effective at learning from long text sequences.