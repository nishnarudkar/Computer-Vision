# Computer Vision with OpenCV

A comprehensive collection of Jupyter notebooks for learning Computer Vision using OpenCV and Python. Each topic is organized in its own folder with hands-on code examples and visual outputs.

## 📋 Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Repository Structure](#repository-structure)
- [Topics Covered](#topics-covered)
- [Learning Path](#learning-path)
- [Quick Reference](#quick-reference)
- [Resources](#resources)

## 🎯 Overview

This repository is a structured learning resource for Computer Vision using OpenCV. It covers everything from basic image I/O to color thresholding and video processing — all through interactive Jupyter notebooks with visual outputs.

## 🔧 Prerequisites

- Python 3.7 or higher
- Basic Python programming knowledge
- Familiarity with NumPy (helpful but not required)

## 📦 Installation

1. **Clone the repository:**
```bash
git clone https://github.com/nishnarudkar/Computer-Vision.git
cd Computer-Vision
```

2. **Create a virtual environment (recommended):**
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

3. **Install required packages:**
```bash
pip install -r requirements.txt
```

4. **Launch Jupyter:**
```bash
jupyter lab
```

## 📁 Repository Structure

```
Computer-Vision/
│
├── README.md
├── requirements.txt
│
├── images/                                        # Shared sample images
│   ├── butterfly.jpg
│   ├── coin2.jpg
│   ├── filter.jpg
│   ├── giraffe-Kenya.png
│   ├── handwritten.jpeg
│   ├── shapes.jpg
│   └── vibgyor.jpg
│
├── Reading_and_Writing_Images/
│   ├── reading_and_writing.ipynb
│   ├── mountain.jpg
│   └── output_image.jpg
│
├── Exploring_Color_space/
│   ├── exploring_colormodels.ipynb
│   ├── butterfly.jpg
│   ├── bgr_image_generated.jpg
│   ├── rgb_image_generated.jpg
│   ├── hsv_image_generated.jpg
│   ├── lab_image_generated.jpg
│   └── gray_image_generated.jpg
│
├── Image Resizing_Scaling_interpolation/
│   ├── image_resizing_scaling_interpolation.ipynb
│   ├── Nearest.jpg
│   ├── Linear.jpg
│   ├── Cubic.jpg
│   ├── Area.jpg
│   └── Lanczos4.jpg
│
├── Flip_Rotate_Crop_Images/
│   └── image_flip_rotate_crop.ipynb
│
├── Drawing_Lines_and_Shapes_using_OpenCV/
│   └── draw_lines_and_shapes.ipynb
│
├── Adding_text_to_images/
│   └── text_opencv.ipynb
│
├── COLOR_Thresholding/
│   ├── color_thresholding.ipynb
│   ├── giraffe-Kenya.png
│   └── color_thresholding_result.png
│
└── Working_with_video_files/
    ├── working_with_video_files1.ipynb
    ├── mountain.mp4
    └── output.mp4
```

## 📚 Topics Covered

### 1. 📂 Reading and Writing Images
- Loading images with `cv2.imread()`
- Displaying images using matplotlib
- Saving output images with `cv2.imwrite()`
- Understanding supported image formats (JPG, PNG, etc.)

### 2. 🎨 Exploring Color Spaces
- BGR — OpenCV's default format
- RGB — standard display format
- HSV (Hue, Saturation, Value) — useful for color filtering
- LAB — perceptually uniform color space
- Grayscale conversion
- Converting between color spaces with `cv2.cvtColor()`

### 3. 📐 Image Resizing, Scaling & Interpolation
- Resizing to fixed dimensions
- Scaling while preserving aspect ratio
- Interpolation methods comparison:
  - `INTER_NEAREST` — Nearest Neighbor
  - `INTER_LINEAR` — Bilinear (default)
  - `INTER_CUBIC` — Bicubic
  - `INTER_AREA` — Area-based (best for downscaling)
  - `INTER_LANCZOS4` — Lanczos (best quality)

### 4. 🔄 Flip, Rotate & Crop Images
- Horizontal, vertical, and both-axis flipping
- Rotating by arbitrary angles
- Cropping regions of interest (ROI) using array slicing
- Affine transformations

### 5. ✏️ Drawing Lines and Shapes
- Lines — `cv2.line()`
- Rectangles — `cv2.rectangle()`
- Circles — `cv2.circle()`
- Ellipses — `cv2.ellipse()`
- Polygons — `cv2.polylines()`
- Filled vs outlined shapes (thickness = -1 to fill)
- Creating a blank canvas with `np.full()`

### 6. 🔤 Adding Text to Images
- `cv2.putText()` with all parameters
- Font types: `FONT_HERSHEY_SIMPLEX`, `FONT_HERSHEY_COMPLEX`, etc.
- Font scale, thickness, and color
- Text positioning (bottom-left origin)
- Anti-aliasing with `cv2.LINE_AA`
- Measuring text size with `cv2.getTextSize()`

### 7. 🌈 Color Thresholding
- Binary thresholding
- HSV-based color range detection
- Creating and applying masks with `cv2.inRange()`
- Isolating specific colors in an image
- Practical use case: detecting objects by color

### 8. 🎬 Working with Video Files
- Reading video files with `cv2.VideoCapture()`
- Iterating through frames
- Writing video output with `cv2.VideoWriter()`
- Accessing video properties (FPS, resolution, frame count)
- Frame-by-frame processing

## 🗺️ Learning Path

Recommended order for beginners:

| Step | Topic |
|------|-------|
| 1 | Reading and Writing Images |
| 2 | Exploring Color Spaces |
| 3 | Image Resizing, Scaling & Interpolation |
| 4 | Flip, Rotate & Crop Images |
| 5 | Drawing Lines and Shapes |
| 6 | Adding Text to Images |
| 7 | Color Thresholding |
| 8 | Working with Video Files |

## 🛠️ Quick Reference

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read an image
img = cv2.imread('image.jpg')

# Convert BGR to RGB for matplotlib display
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb)
plt.show()

# Resize
resized = cv2.resize(img, (640, 480), interpolation=cv2.INTER_LINEAR)

# Flip (0=vertical, 1=horizontal, -1=both)
flipped = cv2.flip(img, 1)

# Crop (NumPy slicing: [y1:y2, x1:x2])
cropped = img[50:200, 100:300]

# Draw shapes
cv2.line(img, (0, 0), (200, 200), (255, 0, 0), 2)
cv2.rectangle(img, (50, 50), (200, 200), (0, 255, 0), 2)
cv2.circle(img, (150, 150), 50, (0, 0, 255), -1)   # -1 = filled

# Add text
cv2.putText(img, "Hello!", (50, 100),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, (255, 255, 255), 2, cv2.LINE_AA)

# Save image
cv2.imwrite('output.jpg', img)
```

## 💡 Key Concepts

**BGR vs RGB**
OpenCV reads images in BGR order. Always convert to RGB before displaying with matplotlib:
```python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

**Coordinate System**
- Origin `(0, 0)` is at the **top-left**
- X increases **rightward**, Y increases **downward**

**Image as NumPy Array**
```
Grayscale → shape: (height, width)
Color     → shape: (height, width, 3)
Pixel values: 0–255 (dtype=uint8)
```

## 🔗 Resources

- [OpenCV Official Documentation](https://docs.opencv.org/)
- [OpenCV Python Tutorials](https://docs.opencv.org/master/d6/d00/tutorial_py_root.html)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ If you find this helpful, consider giving the repo a star!
