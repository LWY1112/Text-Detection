
# Text Recognition Project

This project demonstrates how to perform Optical Character Recognition (OCR) using Python, the Python Imaging Library (PIL), and pytesseract.

## Prerequisites

Ensure you have the following installed:

- Python 3.x
- PIL (Pillow)
- pytesseract
- Tesseract-OCR

## Installation

1. **Install Python**: If you haven't already, download and install Python from [python.org](https://www.python.org/downloads/).

2. **Install PIL (Pillow)**:
   ```sh
   pip install pillow
   ```

3. **Install pytesseract**:
   ```sh
   pip install pytesseract
   ```

4. **Install Tesseract-OCR**:
   - Download and install Tesseract-OCR from [here](https://github.com/UB-Mannheim/tesseract/wiki).

## Usage

1. **Include Tesseract executable in your path**:
   - Make sure to set the path to the Tesseract executable in your script:
     ```python
     pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
     ```

2. **Create an image object using PIL**:
   - Open the image file you want to perform OCR on:
     ```python
     from PIL import Image
     image = Image.open("C:\\Users\\Wei Yi\\PycharmProjects\\textrecognition\\text.jpg")
     ```

3. **Perform OCR using pytesseract**:
   - Pass the image object to the `image_to_string` method of pytesseract:
     ```python
     import pytesseract
     image_to_text = pytesseract.image_to_string(image, lang='eng')
     ```

4. **Print the extracted text**:
   ```python
   print(image_to_text)
   ```

## Example

Here is a complete example of the script:

```python
from PIL import Image
import pytesseract

# Include tesseract executable in your path
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"

# Create an image object of PIL library
image = Image.open("C:\\Users\\Wei Yi\\PycharmProjects\\textrecognition\\text.jpg")

# Pass image into pytesseract module
# pytesseract is trained in many languages
image_to_text = pytesseract.image_to_string(image, lang='eng')

# Print the text
print(image_to_text)
```

## Notes

- Ensure the path to the Tesseract executable is correct.
- The `lang` parameter in `image_to_string` can be changed to perform OCR in different languages, provided the language data is available in Tesseract-OCR.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README provides a comprehensive overview of your project, from installation to usage. Adjust any paths and details as necessary to fit your specific setup.
