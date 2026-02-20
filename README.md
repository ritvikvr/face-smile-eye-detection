# Face, Smile & Eye Detection

A computer vision project that detects faces, smiles, and eyes in images and video streams using OpenCV and Haar Cascades. This project demonstrates the practical application of classical machine learning techniques for real-time object detection.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technical Details](#technical-details)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project implements a multi-cascade detection system to identify faces, smiles, and eyes in real-time using OpenCV's pre-trained Haar Cascade classifiers. The implementation is provided as a Jupyter notebook with comprehensive documentation and examples.

## Features

✨ **Core Capabilities:**
- Face Detection: Accurately identifies faces in images and video streams
- Eye Detection: Detects both eyes within detected faces
- Smile Detection: Recognizes smiling expressions in real-time
- Real-time Processing: Works with webcam feeds and video files
- Easy Integration: Well-documented code for easy understanding and modification

## Requirements

- Python 3.7 or higher
- OpenCV (cv2)
- NumPy
- Jupyter Notebook
- Matplotlib (for visualization)

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/ritvikvr/face-smile-eye-detection.git
cd face-smile-eye-detection
```

### 2. Install dependencies
```bash
pip install opencv-python numpy matplotlib jupyter
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook
```

Then open `Face,Eye&Smile_Detection.ipynb` in your browser.

## Usage

### Basic Image Detection

The notebook includes examples for detecting faces, eyes, and smiles in static images:

```python
import cv2

# Load the cascade classifiers
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')
eye_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_eye.xml')
smile_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_smile.xml')

# Read image
img = cv2.imread('image.jpg')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect faces
faces = face_cascade.detectMultiScale(gray, 1.3, 5)
```

### Real-time Webcam Detection

The project supports real-time detection from your webcam. Run the notebook and follow the instructions to start a live detection stream.

## Project Structure

```
face-smile-eye-detection/
├── Face,Eye&Smile_Detection.ipynb    # Main project notebook
├── README.md                          # This file
└── [haarcascades]                     # Pre-trained cascade files (included with OpenCV)
```

## Technical Details

### Haar Cascades

The project uses Haar Cascade Classifiers, which are:
- **Fast**: Can process video in real-time
- **Lightweight**: Minimal computational requirements
- **Pre-trained**: Ready to use out-of-the-box
- **Interpretable**: Based on classical computer vision principles

### Detection Algorithm

1. **Preprocessing**: Convert image to grayscale
2. **Feature Detection**: Apply Haar features at multiple scales
3. **Cascade Filtering**: Use boosted classifiers for robust detection
4. **Localization**: Return bounding boxes for detected objects

### Cascade Files Used

- `haarcascade_frontalface_default.xml` - Face detection
- `haarcascade_eye.xml` - Eye detection
- `haarcascade_smile.xml` - Smile detection

## Results

The detection system achieves:
- High accuracy for well-lit images
- Real-time performance on standard hardware
- Robust detection across various face orientations (frontal)
- Reliable eye and smile detection within detected face regions

### Performance Notes

- **Faces**: Best with frontal faces, requires adequate lighting
- **Eyes**: Works well within detected face regions
- **Smiles**: Most effective when person is genuinely smiling

## Contributing

Contributions are welcome! Here are ways you can help:

1. **Report Issues**: Found a bug? Open an issue
2. **Suggest Improvements**: Have ideas? Submit a feature request
3. **Submit PRs**: Improvements in code, documentation, or examples
4. **Share Results**: Show how you're using the project

## License

This project is open source and available under the MIT License.

## Acknowledgments

- OpenCV for the excellent computer vision library
- The OpenCV community for Haar Cascade classifiers
- All contributors and users of this project

## Contact & Support

For questions, suggestions, or support:
- Open an issue on GitHub
- Check existing documentation in the notebook
- Review OpenCV documentation for advanced usage

---

**Happy Detecting!** 🎉
