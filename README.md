# Named Entity & Parts of Speech Tagging

A comprehensive analysis and comparison of six advanced machine learning models for Named Entity Recognition (NER) and Part-of-Speech (POS) tagging.

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Features](#features)
- [Methodology](#methodology)
- [Results](#results)
- [Streamlit Application](#streamlit-application)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project undertakes a detailed comparison of six advanced machine learning models tailored for Named Entity Recognition (NER) and Part-of-Speech (POS) tagging. The models include Conditional Random Field (CRF), Bidirectional Long Short-Term Memory (BiLSTM), BiLSTM combined with CRF (BiLSTM+CRF), Convolutional Neural Network (CNN), Bidirectional Encoder Representations from Transformers (BERT), and XLNet.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Lokesh-Balamurugan/ner-pos-tagging.git
    cd ner-pos-tagging
    ```

2. Download the dataset:
    - [NER Dataset](https://www.kaggle.com/code/bavalpreet26/ner-using-crf/input?select=ner_dataset.csv)

3. Place the dataset files in the appropriate directory:
    ```plaintext
    ner-pos-tagging/
    ├── data/
    │   ├── ner_dataset.csv
    ```

## Features

- **Named Entity Recognition (NER)**:
  - Identifies and categorizes entities like person names, organizations, and locations.
  
- **Part-of-Speech (POS) Tagging**:
  - Assigns grammatical categories such as nouns, verbs, and adjectives to words in sentences.

## Methodology

### Data Preprocessing

1. **Data Collection**:
   - The dataset includes sentences labeled with IOB format tags for named entities and POS tags.

2. **Data Merging**:
   - Merged data from various sources into a single dataset for analysis.

3. **Data Cleaning**:
   - Handled missing values and removed sentences with mismatched tokens and tags.

4. **Feature Extraction**:
   - Extracted word-level and contextual features necessary for model training.

### Preprocessing for Different Methods

Different models require specific preprocessing steps to ensure optimal performance:

1. **CRF**: utilizes dependencies between adjacent labels for sequence labeling
   - Features include word tokens, POS tags, and other contextual information.
   - Input format is a structured feature dictionary for each word.

2. **BiLSTM**: captures contextual information by processing sequences in both directions
   - Tokenized sentences are converted to integer indices.
   - Padding ensures uniform sequence length across batches.
   - Embedding layers are used to convert tokens to dense vectors.

3. **BiLSTM+CRF**: combines BiLSTM and CRF for enhanced sequence tagging
   - Combines the preprocessing steps of BiLSTM and CRF.
   - Tokenized sequences with features structured for CRF layer integration.

4. **CNN**: leverages feature extraction capabilities for sequence tagging
   - Tokenized sentences are converted to integer indices.
   - Padding and embedding layers are used to ensure consistent input size and dense vector representation.

5. **BERT**: employs an attention mechanism for contextual relation learning
   - Sentences are tokenized using BERT’s tokenizer, including special tokens ([CLS], [SEP]).
   - Attention masks are created to differentiate between padding and actual tokens.
   - Tokenized inputs are converted to IDs and passed through BERT’s embedding layer.

6. **XLNet**: extends the Transformer-XL model with an autoregressive approach for bidirectional context learning
   - Similar preprocessing steps as BERT, with additional attention to autoregressive input formatting.
   - Tokenization, attention masks, and positional embeddings are prepared for XLNet’s transformer architecture.

## Results

### Named Entity Recognition (NER)

- **CRF**: Precision: 0.85, Recall: 0.84, F1 Score: 0.85
- **BiLSTM**: Precision: 0.81, Recall: 0.80, F1 Score: 0.81
- **BiLSTM+CRF**: Precision: 0.84, Recall: 0.82, F1 Score: 0.83
- **CNN**: Precision: 0.79, Recall: 0.80, F1 Score: 0.80
- **BERT**: Precision: 0.83, Recall: 0.84, F1 Score: 0.84
- **XLNet**: Precision: 0.83, Recall: 0.84, F1 Score: 0.83

### Part-of-Speech (POS) Tagging

- **CRF**: Precision: 0.97, Recall: 0.97, F1 Score: 0.97
- **BiLSTM**: Precision: 0.96, Recall: 0.93, F1 Score: 0.93
- **BiLSTM+CRF**: Precision: 0.95, Recall: 0.96, F1 Score: 0.95
- **CNN**: Precision: 0.97, Recall: 0.93, F1 Score: 0.93
- **BERT**: Precision: 0.97, Recall: 0.97, F1 Score: 0.97
- **XLNet**: Precision: 0.95, Recall: 0.97, F1 Score: 0.96

### Conclusion

The analysis highlights the strengths and weaknesses of each model for NER and POS tagging tasks. BERT and XLNet demonstrate superior performance, particularly in handling complex language patterns. The CRF and BiLSTM+CRF models also perform well, indicating their robustness for sequence tagging tasks.

## Streamlit Application

The application demonstrates the functionality of NER and POS tagging models. Users can input text and receive tagged outputs based on pre-trained models. 

Access the application here: [NER and POS Tagging App](https://huggingface.co/spaces/lokeshbalamurugan20/NamedEntityandPOS).

## Contributing

Contributions are welcomed! Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
