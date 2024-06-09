# Aspect-Based Sentiment Analysis using PyABSA

## Objective

The objective of this script is to perform aspect-based sentiment analysis on a given dataset using the PyABSA library. The script reads input data, extracts aspects and their corresponding sentiments, and saves the results into an Excel file with conditional formatting applied to sentiment cells.

## Description

This script leverages the PyABSA library for aspect-based sentiment analysis. It uses pre-trained models to extract aspects and sentiments from input sentences. The results are then stored in a pandas DataFrame and saved to an Excel file with conditional formatting to highlight positive and negative sentiments.

## Libraries and Functions

### Libraries

1. **PyABSA**: A library for aspect-based sentiment analysis. It provides pre-trained models and tools to perform aspect extraction and sentiment prediction.
    - **available_checkpoints**: Function to list available checkpoints for different languages and tasks.
    - **ATEPCCheckpointManager**: Manager class to load aspect extraction and sentiment classification models.

2. **pandas**: A powerful data manipulation library used for reading, processing, and saving data.
    - **pd.read_csv**: Reads a CSV file into a DataFrame.
    - **pd.DataFrame**: Creates a DataFrame from a list of dictionaries.
    - **pd.to_excel**: Saves a DataFrame to an Excel file.

3. **openpyxl**: A library to read/write Excel 2010 xlsx/xlsm/xltx/xltm files.
    - **Workbook, load_workbook**: Classes to create and load Excel workbooks.
    - **PatternFill**: Class to apply color fills to cells for conditional formatting.

### Functions

1. **available_checkpoints(show_ckpts=True)**: Lists all available checkpoints for aspect-based sentiment analysis models.

2. **ATEPCCheckpointManager.get_aspect_extractor(checkpoint='English')**: Loads the aspect extraction and sentiment classification model for the specified checkpoint.

3. **extract_aspects(data)**: Extracts the sentence, aspect, sentiment, and confidence from the model's output.
    - **data**: Input data containing aspect extraction results.
    - **Returns**: A list of dictionaries with keys 'sentence', 'aspect', 'sentiment', and 'confidence'.
