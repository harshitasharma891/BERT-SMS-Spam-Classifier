# BERT SMS Spam Classifier

## Project Overview

This project implements an SMS spam classification system using a fine-tuned BERT model.

The model classifies text messages into two categories:

- **HAM** — legitimate or non-spam messages
- **SPAM** — unwanted or suspicious messages

The project uses the Hugging Face `sms_spam` dataset and fine-tunes the `bert-base-uncased` transformer model for sequence classification.

## Key Features

- SMS spam classification using BERT.
- Fine-tuning of `bert-base-uncased`.
- Dataset loading using Hugging Face Datasets.
- Text tokenization with the BERT tokenizer.
- Train and test data splitting.
- Model training using the Hugging Face Trainer API.
- Classification evaluation using a classification report.
- Prediction probabilities for HAM and SPAM classes.
- Testing with sample spam and legitimate messages.

## Dataset

The project uses the Hugging Face:

`sms_spam`

dataset.

The dataset is split into training and testing sets using an 80/20 split.

## Model

### BERT

`bert-base-uncased`

The pre-trained BERT model is fine-tuned for binary sequence classification.

The output labels are:

| Label ID | Class |
|---|---|
| 0 | HAM |
| 1 | SPAM |

## Project Workflow

```text
SMS Dataset
     ↓
Train/Test Split
     ↓
BERT Tokenization
     ↓
Fine-Tuning BERT
     ↓
Model Training
     ↓
Model Evaluation
     ↓
HAM / SPAM Prediction
```

## Training Configuration

The model is trained with:

- Learning rate: `2e-5`
- Training batch size: `16`
- Evaluation batch size: `16`
- Number of epochs: `4`
- Weight decay: `0.01`

## Evaluation

The trained model is evaluated using the `classification_report` function from scikit-learn.

The evaluation compares the predicted labels with the actual labels and reports classification performance for both HAM and SPAM messages.

## Sample Predictions

The project tests the model with different types of messages, including:

- Promotional messages
- Prize and reward messages
- Normal conversational messages
- Meeting and class-related messages

The prediction function returns:

- Input text
- HAM probability
- SPAM probability
- Final prediction

## Technologies Used

- Python
- Hugging Face Transformers
- Hugging Face Datasets
- BERT
- PyTorch
- scikit-learn
- Google Colab

## Installation

Install the required libraries:

```bash
pip install transformers datasets torch scikit-learn
```

## Running the Project

1. Install the required libraries.
2. Load the `sms_spam` dataset.
3. Split the dataset into training and testing sets.
4. Tokenize the SMS messages using the BERT tokenizer.
5. Load the BERT sequence classification model.
6. Fine-tune the model using the Hugging Face Trainer API.
7. Evaluate the model using the classification report.
8. Test the trained model with new SMS messages.

## Repository Structure

```text
BERT-SMS-Spam-Classifier/
│
├── BERT_SMS_Spam_Classifier.ipynb
└── README.md
```

## Author

**Harshita Sharma**

AI/ML Engineer

GitHub: github.com/harshitasharma891  
LinkedIn: linkedin.com/in/harshita-sharma-b843031b5
