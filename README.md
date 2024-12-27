```markdown
# DocConverterPro

DocConverterPro is a Python-based tool that allows you to convert PDF to Word, JPG to Word using OCR, image files to PDF, and audio to text. The tool preserves the original formatting of the PDF, including logos, signs, and other graphical elements.

## Features
- Convert PDF to Word while preserving original formatting.
- Convert JPG to Word using OCR capabilities.
- Convert image files (e.g., PNG, BMP) to PDF.
- Convert audio files to text.

## Requirements
- Python 3.x
- Tesseract OCR
- Required Python libraries (listed in `requirements.txt`)
- Internet connection (required for audio to text conversion)

## Installation

### Step 1: Clone the Repository

First, you need to clone the repository from GitHub. Open your terminal or command prompt and run the following commands:

```bash
git clone https://github.com/randumduck/DocConverterPro.git
cd DocConverterPro
```

### Step 2: Set Up Virtual Environment

To ensure that your other Python projects are not disturbed, set up a virtual environment:

1. **Install Virtualenv** (if you haven't already):
   ```bash
   pip install virtualenv
   ```

2. **Create the Virtual Environment**:
   ```bash
   virtualenv docpro
   ```

3. **Activate the Virtual Environment**:
   - **On Linux**:
     ```bash
     source docpro/bin/activate
     ```
   - **On Windows**:
     ```bash
     .\docpro\Scripts\activate
     ```

### Step 3: Install Required Libraries

With the virtual environment activated, install the required libraries:

```bash
pip install -r requirements.txt
```

### Step 4: Install Tesseract OCR

Tesseract OCR is required for the OCR capabilities of the tool.

- **On Linux**:
  ```bash
  sudo apt update
  sudo apt install tesseract-ocr
  sudo apt install libtesseract-dev
  ```

- **On Windows**:
  1. Download and install Tesseract from here.
  2. Add the Tesseract executable path to your system's PATH:
     - Go to **Control Panel** > **System and Security** > **System** > **Advanced system settings**.
     - Click on **Environment Variables**.
     - Under **System variables**, find the `Path` variable, select it, and click **Edit**.
     - Click **New** and add the path to the Tesseract executable (e.g., `C:\Program Files\Tesseract-OCR`).

## Usage

Run the script and follow the prompts to choose an option and provide the file path.

```bash
python doc_converter_pro.py
```

### Options

1. Convert PDF to Word
2. Convert JPG to Word
3. Convert Image to PDF
4. Convert Audio to Text
0. Exit

### Example

```bash
Choose an option:
1. Convert PDF to Word
2. Convert JPG to Word
3. Convert Image to PDF
4. Convert Audio to Text
0. Exit
Enter your choice: 1
Enter the file path: /path/to/your/file.pdf
```

The converted file will be saved in the same location as the input file with the appropriate extension.

### Internet Requirement

- An internet connection is required for the audio to text conversion feature, as it uses Google's speech recognition service.

## License

This project is licensed under the MIT License.
```

### requirements.txt

```plaintext
pdf2docx
pytesseract
pdf2image
python-docx
pillow
SpeechRecognition
fpdf
