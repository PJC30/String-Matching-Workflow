# String Matching Workflow

## Overview
This script performs string matching on an input CSV file, identifying pairs of strings that differ by exactly one character. It processes data in adjustable chunks to optimize memory usage, generates temporary output files, and merges them into a final result.

## Features
- **Adjustable Chunk Size**: Input file is read in chunks to optimize memory usage.
- **One-Letter Difference Matching**: Pairs of strings differing by exactly one character are identified.
- **Final Output**: Results from all chunks are combined into one CSV file.
- **Clean-Up**: Temporary files are deleted after processing.

## Technologies Used
- **Python**: The primary language used for the script.
- **pandas**: For reading and processing CSV files.
- **glob**: To locate and manage temporary files.
- **os**: For file clean-up.
- **itertools**: For generating string combinations.

## Workflow
1. Read input file in chunks of adjustable size.
2. Compare strings within each chunk for one-letter differences.
3. Save chunk results into temporary CSV files.
4. Merge all chunk results into a final output CSV.
5. Delete temporary files after processing.
