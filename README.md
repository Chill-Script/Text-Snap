# Text-Snap
TextSnap is a comprehensive Python application designed for extracting, editing, and managing text from images.
The application utilizes Optical Character Recognition (OCR) to convert images into text, which can then be edited, saved as txt, copied to the clipboard, or processed further through OpenAI's ChatGPT.

## Features

### 1. OCR (Optical Character Recognition)
- Supports image formats such as PNG, JPG, JPEG, BMP, and TIFF.
- Utilizes the `pytesseract` library to extract text from images.
- Processes multiple images selected by the user and cleans the extracted text for readability.

### 2. User Interface
- Command-line-based interface built using the `curses` library.
- Interactive menus for scanning images, editing text, saving text to files, copying text to the clipboard, and uploading text to ChatGPT.
- Customizable color schemes for the interface.

### 3. File Management and Security
- Extracted text can be saved to new or existing text files.
- The application ensures the directory where files are saved (`textsnapmapa`) is hidden and protected.
- Configuration data, including encryption keys and admin passwords, is securely stored using the `cryptography` library.

### 4. ChatGPT Integration
- Users can upload the extracted text to ChatGPT via OpenAI's API and receive responses.
- The OpenAI API key is securely managed and can be saved directly into the script for persistent use.

### 5. Customization
- Users can customize the interface's color scheme.
- Admin features include changing the admin password, removing the `textsnapmapa` directory, and viewing or resetting scan statistics.

### 6. Multi-threading and UI Feedback
- A loading bar is displayed during initialization to provide feedback to the user during potentially time-consuming operations.

### 7. Error Handling and Robustness
- Includes robust error handling to manage issues such as failed image processing, API interactions, and file permissions.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/de3jeh/Text-Snap
   ```
2. **Navigate to the directory:**
   ```bash
   cd TextSnap
   ```
3. **Install the required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Set up Tesseract OCR:**
   - Download and install Tesseract OCR from [here](https://github.com/tesseract-ocr/tesseract).
   - Update the `pytesseract.pytesseract.tesseract_cmd` path in the script to point to your Tesseract installation.

5. **Set up OpenAI API key:**
   - Replace `YOUR_OPEN_API_KEY` in the script with your OpenAI API key.
   - Or use the script UI to do this

## Usage

1. **Run the script:**
   ```bash
   python TextSnap.py
   ```
2. **Navigate the menu:**
   - Use arrow or number keys to navigate and press Enter to select options.
   - Options include adding images for OCR, editing text, saving text, copying text to the clipboard, and interacting with ChatGPT.

3. **Customize Interface:**
   - Change the color scheme through the options menu to suit your preferences. 'this is still in work in progress'


## Contributing

If you would like to contribute to TextSnap, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a pull request.

## License

This project is licensed under the MIT License.
