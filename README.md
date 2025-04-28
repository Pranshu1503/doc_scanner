# Document Scanner

This is a Python-based document scanner that processes an input image, detects the edges of a document, and applies a perspective transform to produce a top-down scanned version of the document.

## Features
- Detects edges in an image.
- Finds the contours of a document.
- Applies a perspective transform to create a scanned effect.
- Converts the scanned document to a black-and-white format.

## Requirements
Make sure you have the following Python libraries installed:
- `numpy`
- `opencv-python`
- `imutils`
- `scikit-image`

You can install the required libraries using:
```bash
pip install numpy opencv-python imutils scikit-image
```

## Usage
1. Place the image you want to scan in the project directory.
2. Run the script with the following command:
   ```bash
   python scan.py -i <path_to_image>
   ```
   Replace `<path_to_image>` with the path to your image file.

### Example
```bash
python scan.py -i example.jpg
```

## How It Works
1. **Edge Detection**: The script detects edges in the input image using the Canny edge detector.
2. **Contour Detection**: It identifies the largest contours in the image and approximates the document's shape.
3. **Perspective Transform**: A four-point perspective transform is applied to get a top-down view of the document.
4. **Thresholding**: The transformed image is converted to grayscale and thresholded to create a black-and-white effect.

## Output
The script displays:
- The original image.
- The edge-detected image.
- The outlined document.
- The final scanned document.

## Notes
- Ensure the input image has good lighting and contrast for better results.
- The script is designed for rectangular documents.

