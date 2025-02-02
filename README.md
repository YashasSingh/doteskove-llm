# Kaggle NLP Pipeline for Dostoevsky-Inspired Language Modeling

## Overview
This project processes and analyzes text extracted from PDF files using machine learning techniques. It focuses on developing a language model inspired by Fyodor Dostoevsky’s writing style, capturing his unique narrative structures, themes, and linguistic patterns.

## Features
- **PDF Text Extraction**: Reads and extracts text from multiple PDFs containing Dostoevsky's works.
- **Data Cleaning**: Removes noise, unwanted characters, and repeated phrases while preserving Dostoevsky’s stylistic elements.
- **Text Chunking**: Splits text into manageable segments for NLP tasks.
- **Tokenization**: Converts text into numerical representations using Falcon tokenizer.
- **Repeated Phrase Analysis**: Identifies frequently occurring phrases and motifs common in Dostoevsky’s literature.
- **Language Model Training**: Implements a transformer-based neural network using PyTorch for text generation that mimics Dostoevsky’s writing style.

## Requirements
The following Python libraries are required:

```bash
pip install PyPDF2 datasets transformers accelerate torch numpy pandas matplotlib tqdm
```

## Directory Structure
- **`/kaggle/input/`**: Contains the input PDF files.
- **`/kaggle/working/`**: Stores processed output files.
- **`/kaggle/temp/`**: Used for temporary file storage.

## Steps

### 1. PDF Text Extraction
- Extracts text from PDFs in the `/kaggle/input/dataaaaaaa/works` directory.
- Uses `PyPDF2.PdfReader` to read text from each page.

### 2. Data Cleaning
- Removes unwanted headers, footers, numbers, and excess whitespace.
- Ensures that Dostoevsky’s sentence structures and stylistic nuances are preserved.
- Stores cleaned text in `cleaned_book.txt`.

### 3. Text Chunking
- Splits the text into chunks of 512 words to prepare for tokenization.
- Maintains narrative flow and coherence in Dostoevsky’s lengthy, complex sentences.

### 4. Tokenization
- Uses `tiiuae/falcon-7b` tokenizer to process the text.
- Converts text into tokenized datasets suitable for deep learning models.
- Ensures compatibility with Dostoevsky’s intricate phrasing and frequent philosophical digressions.

### 5. Repeated Phrase Analysis
- Identifies and ranks commonly occurring multi-word phrases.
- Filters and lists frequently repeated phrases appearing more than 5 times.
- Detects Dostoevsky’s signature phrases, recurring themes, and stylistic patterns.

### 6. Language Model Training
- Implements a GPT-style model in PyTorch.
- Trains the model on Dostoevsky’s works to generate text in his literary style.
- Uses multi-head self-attention for improved text understanding.
- Fine-tunes the model to replicate Dostoevsky’s characteristic themes of existentialism, morality, and human psychology.

## Usage
1. Place your PDF files containing Dostoevsky’s works in the `/kaggle/input/` directory.
2. Run the script to process and extract text.
3. The cleaned text will be saved in `cleaned_book.txt`.
4. Tokenization and repeated phrase analysis will be performed automatically.
5. Train the GPT-style model for text generation inspired by Dostoevsky.

## Output
- **Extracted text**: Displays extracted text snippets.
- **Cleaned text file**: Saved as `cleaned_book.txt`.
- **Tokenized dataset**: Prepared for NLP processing.
- **Repeated phrases list**: Displays frequently occurring phrases and motifs.
- **Trained model**: Generates text resembling Dostoevsky’s writing style.

## Notes
- The Falcon tokenizer is used for text processing.
- GPU acceleration is enabled when available for faster training.
- Ensure Kaggle's file structure is properly set up before running the script.
- The `tqdm` library is used for progress tracking in the training process.
- The training approach is designed to capture Dostoevsky’s unique voice, philosophical depth, and complex narrative structures.

## License
This project is for educational and research purposes.

