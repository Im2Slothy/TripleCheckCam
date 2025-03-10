# Photo2Text-AISolver (Shit name idk what else to call this)
### Inspired from https://x.com/vikvang1/status/1898144704077652443

# NOW I TESTED THIS A FEW TIMES AND IT WASN'T PERFECT, ILL KEEP WORKING ON IT BUT IF YOU HAVE BETTER METHODS PLS MAKE A PR. 

This is a Python app. made to capture text from a webcam, process it using OpenCV for image preprocessing, and perform Optical Character Recognition (OCR) with EasyOCR.

## Features
- Captures text via webcam using OpenCV.
- Preprocesses images to reduce noise and isolate text.
- Uses EasyOCR for accurate text recognition.
- Displays results in the console.
- Lightweight and easy to use on Windows.

---

## Prerequisites
- Python 3.8 or higher.
- Required libraries: `opencv-python`, `numpy`, `easyocr`.

---

## Installation
git clone https://github.com/your-username/Slothy-Photo2Text-AISolver.git
cd Slothy-Photo2Text-AISolver
pip install opencv-python numpy easyocr


### (Optional) For NVIDIA GPU Users:
pip uninstall torch -y
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip install easyocr

---


## Usage

1. Ensure your webcam is connected and functional.
2. Take a picture (with spacebar) of text, I found better results in a darker room. 
3. Position the text 10–20 cm from the webcam under bright, even lighting, filling 1/3 to 1/2 of the frame.
4. Run the application:
python -m src.main
5. Press **SPACE** to capture the text. The OCR result will display in the console along with simulated triple-check results.
6. Press **ESC** to exit.

---

## Example Output
Starting TripleCheckCam... Press SPACE to capture text, ESC to exit.

TRIPLE CHECK RESULTS
Q: is the earth flat?
GPT-4: No (0.94s)
Grok: No (1.21s)
All models agree.

--------------------------------------------------

(Triple Check - Press Space to continue)


---

## Troubleshooting

### OpenCV Error (`cv2.imshow not implemented`):
This occurs if you installed `opencv-python-headless` instead of `opencv-python`. Fix it by reinstalling:
pip uninstall opencv-python opencv-python-headless -y
pip install opencv-python


### OCR Not Recognizing Text:
- Ensure input text is clear, well-lit, and on a plain background.
- Check `debug_processed_image.png` in the project root for the preprocessed image.

### EasyOCR Slow on CPU:
Install CUDA and PyTorch with GPU support for faster processing.

---

## Contributing

✅ Feel free to fork this repository, make improvements, and submit pull requests.

✅ Issues and suggestions are welcome!

