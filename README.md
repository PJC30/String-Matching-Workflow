# String Matching Workflow

## Overview
This script performs **string matching** to identify pairs of strings that differ by exactly one letter. It processes large input data by reading it in adjustable chunks, comparing the strings, and outputting the matching results to a final CSV file. Temporary output files from each chunk are generated and later cleaned up.

## Features
- **CSV Input**: The script reads strings from a CSV file and identifies pairs that differ by exactly one character.
- **Batch Processing**: The input file is processed in adjustable chunks, optimizing memory efficiency based on your preferred chunk size.
- **Matching Logic**: Pairs of strings are compared character by character, and the script identifies pairs with only one differing character.
- **Temporary Output Files**: Results from each chunk are saved into temporary CSV files and then combined into a final result.
- **Clean-Up**: After the final output is generated, temporary files from chunk processing are deleted.

## Code Overview
- **foo**: A helper function that generates combinations of items to be compared.
- **String Matching**: The script generates combinations of strings and compares them, checking for a one-character difference.
- **Data Processing**: The input file is read in chunks, with string comparison applied to each chunk.
- **Output Handling**: After processing each chunk, results are saved in temporary CSV files (`output_file_X.csv`), where `X` is the chunk number.
- **Final Output**: After all chunks are processed, the results are combined into a single `output.csv` file.
- **Clean-Up**: Temporary chunk files are deleted after combining them into the final output.

## Technologies Used
- **Python**: The primary scripting language for the workflow.
- **pandas**: Used for reading, processing, and merging the CSV files.
- **glob**: To locate and manage the temporary output files.
- **os**: Used for file clean-up.
- **itertools**: Provides combinations for efficient pair generation.

## Workflow
1. **Data Ingestion**: The input file is read in adjustable chunks to optimize memory usage based on the chunk size specified.
2. **String Comparison**: For each chunk, pairs of strings are compared to identify those that differ by exactly one letter.
3. **Intermediate Output**: For each chunk, the results are saved to temporary CSV files (`output_file_X.csv`).
4. **Final Output**: After all chunks are processed, the results from all temporary files are combined into one final CSV file (`output.csv`).
5. **Clean-Up**: After combining the results, all temporary chunk files are deleted to free up space.
