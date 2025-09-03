# AI Text Operations

This project is a web-based application that provides a suite of tools for text manipulation, including summarization, translation, and text extraction from images and PDFs. The application is built with Python and uses the Eel library to create a seamless desktop-like experience with a web-based GUI.

## Features

- **Text Summarization:** Summarize long texts into concise summaries of varying lengths (short, medium, or long).
- **Text Translation:** Translate text between a wide variety of languages using the Google Translate API.
- **Text Extraction (OCR):** Extract text from various image formats (PNG, JPG, etc.) and PDF files.

## Technologies Used

- **Backend:** Python
- **GUI:** Eel
- **Text Summarization:** Hugging Face Transformers (`Falconsai/text_summarization` model)
- **Text Translation:** `googletrans`
- **Text Extraction (OCR):** `pytesseract` for images and `PyPDF2` for PDFs
- **Frontend:** HTML, CSS, JavaScript

## Setup and Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/prasad-gade05/AI-Text-Summarizer-Translator-and-Extractor.git
    cd AI-Text-Summarizer-Translator-and-Extractor
    ```

2.  **Create a virtual environment:**

    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**

    - **Windows:**
      ```bash
      venv\Scripts\activate
      ```
    - **macOS/Linux:**
      ```bash
      source venv/bin/activate
      ```

4.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Configuration

This application uses Tesseract for Optical Character Recognition (OCR). You will need to have Tesseract installed on your system.

1.  **Install Tesseract:**

    - **Windows:** Download and install Tesseract from the official repository: [Tesseract at UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki)
    - **macOS (using Homebrew):**
      ```bash
      brew install tesseract
      ```
    - **Linux (Debian/Ubuntu):**
      ```bash
      sudo apt update
      sudo apt install tesseract-ocr
      ```

2.  **Update the Tesseract Path in `src/main.py`:**
    Open the `src/main.py` file and locate the following line:
    ```python
    file_reader = FileReader(r'C:\Program Files\Tesseract-OCR\tesseract.exe')
    ```
    Change the path to the location of your Tesseract executable. For example:
    - **macOS/Linux:**
      ```python
      file_reader = FileReader(r'/usr/local/bin/tesseract')
      ```

## How to Run

To run the application, execute the `main.py` file from the `src` directory:

```bash
python src/main.py
```

This will start the application and open the user interface in a new window.

## Project Structure

The project is organized as follows:

```
AiTextOperations/
├── src/
│   ├── main.py
│   ├── templates/
│   │   ├── index.html
│   │   ├── style.css
│   │   ├── summery logo.png
│   │   └── static/
│   │       └── script.js
│   └── assets/
│       ├── nashik.jpg
│       └── nashik.pdf
├── requirements.txt
├── .gitignore
└── README.md
```
