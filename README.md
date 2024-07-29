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
    git clone https://github.com/username/ner-pos-tagging.git
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

### Sequence Tagging Models

1. **Conditional Random Field (CRF)**:
   - Utilizes dependencies between adjacent labels for sequence labeling.

2. **Bidirectional LSTM (BiLSTM)**:
   - Captures contextual information by processing sequences in both directions.

3. **BiLSTM+CRF**:
   - Combines BiLSTM and CRF for enhanced sequence tagging.

4. **Convolutional Neural Network (CNN)**:
   - Leverages feature extraction capabilities for sequence tagging.

5. **Bidirectional Encoder Representations from Transformers (BERT)**:
   - Uses an attention mechanism for contextual relation learning.

6. **XLNet**:
   - Extends the Transformer-XL model with an autoregressive approach for bidirectional context learning.

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

## Streamlit Application

Access the application here: [NER and POS Tagging App](https://huggingface.co/spaces/lokeshbalamurugan20/NERProject).

## Contributing

Contributions are welcomed!!! Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
