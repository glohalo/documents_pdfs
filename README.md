# 01_abbbrv_search: Abbreviation Extractor
### README.md

This repository provides a simple Python script to help editors, writers, and researchers extract unique abbreviations from PDF documents. It can be particularly useful when editing documents such as theses, articles, or research papers to ensure consistency and proper usage of abbreviations throughout the text.

---

## Features

- Extracts all unique abbreviations from a PDF file.
- Filters out common dictionary words (e.g., avoids including uppercase titles or standard English words like `ANALYSING`).
- Handles multi-page PDFs and outputs a clean list of abbreviations.
- Identifies potential document titles for additional context during editing.

---

## How It Works

1. The script reads the full text of the PDF document.
2. It identifies sequences of uppercase letters (at least two characters long) as potential abbreviations using regular expressions.
3. It excludes common dictionary words and allows customization for specific needs.

---

## Prerequisites

### Install Required Libraries
This script requires the following Python libraries:

- `PyMuPDF` (`fitz`) for reading PDF files.
- `nltk` for filtering out common dictionary words (optional, for better accuracy).

You can install them using pip:

```bash
pip install pymupdf nltk
```

---

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pdf-abbreviation-extractor.git
   cd pdf-abbreviation-extractor
   ```

2. Download the English dictionary for `nltk` (if using the filtering feature):
   ```python
   import nltk
   nltk.download('words')
   ```

3. Place your PDF file in the repository directory.

---

## Usage

1. Replace the `example.pdf` in the script with the path to your PDF file.
2. Run the script:

   ```bash
   python extract_abbreviations.py
   ```

3. The script will output:
   - **Unique abbreviations:** A list of abbreviations found in the document.
   - **Potential titles:** A list of uppercase titles for context.

---

## Example Output

For a document named `research_paper.pdf`:

```plaintext
Identified Titles:
1. INTRODUCTION
2. METHODS AND MATERIALS
3. CONCLUSION

Unique Abbreviations Found:
1. AI
2. NASA
3. PDF
4. ML
5. UN
```

---

## Contributions

Contributions are welcome! If you’d like to enhance this tool or add new features, feel free to open an issue or create a pull request.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments

- Thanks to the creators of `PyMuPDF` and `nltk` for their powerful tools.
- Inspired by the needs of document editors and researchers to ensure clarity and consistency.
