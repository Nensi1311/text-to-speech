# Text-to-Speech with OCR

A Python project that extracts text from images using Tesseract OCR and converts it into speech using Google Text-to-Speech (gTTS).

## Features

- **Image Preprocessing**: Uses OpenCV for grayscale conversion and Otsu's thresholding to improve OCR accuracy.
- **OCR Text Extraction**: Leverages `pytesseract` to extract text from processed images.
- **Text Cleaning**: Replaces non-alphanumeric characters to ensure clear speech output.
- **Text-to-Speech (TTS)**: Converts extracted text into MP3 audio files using `gTTS`.
- **Audio Playback**: Automatically plays the generated audio file.

## Prerequisites

Before running the project, you need to install Tesseract OCR on your system:

1.  **Install Tesseract OCR**:
    - Download and install from [Tesseract at UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki).
    - Note the installation path (default: `C:\Program Files\Tesseract-OCR\tesseract.exe`).

## Installation

Install the required Python libraries using pip:

```bash
pip install pytesseract pillow opencv-python gTTS playsound
```

## Usage

1.  Open the Jupyter notebook `ocr_its.ipynb`.
2.  Ensure you have an image named `input_image.jpg` in the project directory (or update the filename in the code).
3.  Update the `tesseract_cmd` path if it differs from the default:
    ```python
    pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
    ```
4.  Run the cells sequentially to preprocess the image, extract text, and hear the audio output.

## Project Structure

- `ocr_its.ipynb`: Main Jupyter notebook containing the implementation logic.
- `input_image.jpg`: Input image for testing (user-provided).
- `processed_image.png`: Intermediate result of image preprocessing.
- `output_audio_image.mp3`: Generated audio file.
- `README.md`: Project documentation.
