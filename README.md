# Automated Data Cleaning Pipeline

A Python-based utility designed to automate essential data cleaning workflows for tabular datasets (.csv and .xlsx). It handles duplicate detection and extraction, missing value imputation, and standardized data export.

## Features

- **Multi-Format Support**: Reads both CSV and Excel (`.xlsx`) datasets.
- **Duplicate Management**: Identifies, isolates, and exports duplicate records into a separate audit file before removal.
- **Missing Value Handling**:
  - Automatically identifies missing values across columns.
  - Imputes missing numeric values with the column mean.
  - Cleans non-numeric fields with null values.
- **Automated Export**: Saves cleaned data with a standard naming convention (`<dataset_name>_Clean_data.csv`).

## Project Structure

```text
├── app.py              # Main data cleaning script
├── requirements.txt    # Project dependencies
├── .gitignore          # Ignored files (temporary & generated data)
└── README.md           # Project documentation
```

## Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed.

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/Athul64/Data-Cleaning-Master.git
   cd Data-Cleaning-Master
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

Run the script from your terminal:

```bash
python app.py
```

Follow the prompts to enter:
1. **Dataset path**: Relative or absolute path to your file (e.g., `data/sales.csv`).
2. **Dataset name**: A label used for naming exported files (e.g., `sales_q1`).

### Outputs

The script generates two files upon execution:
- `<dataset_name>_duplicates.csv`: Contains all duplicate rows removed during processing (if any).
- `<dataset_name>_Clean_data.csv`: The final, cleaned dataset.
