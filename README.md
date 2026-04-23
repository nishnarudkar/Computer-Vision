# OpenCV Learning Repository

A comprehensive collection of Jupyter notebooks demonstrating various OpenCV (Open Source Computer Vision Library) techniques and operations for image processing and computer vision tasks.

## 📋 Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Repository Structure](#repository-structure)
- [Topics Covered](#topics-covered)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This repository contains hands-on tutorials and examples for learning OpenCV with Python. Each topic is organized in its own directory with Jupyter notebooks that include code examples, explanations, and visual outputs.

## 🔧 Prerequisites

- Python 3.7 or higher
- Basic understanding of Python programming
- Familiarity with NumPy (helpful but not required)
- Jupyter Notebook or JupyterLab

## 📦 Installation

1. **Clone the repository:**
```bash
git clone <repository-url>
cd <repository-name>
```

2. **Create a virtual environment (recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install required packages:**
```bash
pip install -r requirements.txt
```

## 📁 Repository Structure

```
.
├── README.md
├── requirements.txt
├── images/                          # Sample images for tutorials
│   ├── butterfly.jpg
│   ├── giraffe-Kenya.png
│   └── ...
├── Reading_and_Writing_Images/
│   └── reading_and_writing.ipynb
├── Exploring_Color_space/
│   └── exploring_colormodels.ipynb
├── Image Resizing_Scaling_interpolation/
│   └── image_resizing_scaling_interpolation.ipynb
├── Flip_Rotate_Crop_Images/
│   └── image_flip_rotate_crop.ipynb
├── Drawing_Lines_and_Shapes_using_OpenCV/
│   └── draw_lines_and_shapes.ipynb
├── Adding_text_to_images/
│   └── text_opencv.ipynb
├── COLOR_Thresholding/
│   └── color_thresholding.ipynb
└── Working_with_video_files/
    └── working_with_video_files1.ipynb
```

## 📚 Topics Covered

### 1. **Reading and Writing Images**
- Loading images using `cv2.imread()`
- Displaying images with matplotlib
- Saving images using `cv2.imwrite()`
- Understanding image formats

### 2. **Exploring Color Spaces**
- BGR (OpenCV default)
- RGB color space
- HSV (Hue, Saturation, Value)
- LAB color space
- Grayscale conversion
- Color space conversions

### 3. **Image Resizing, Scaling & Interpolation**
- Resizing images to specific dimensions
- Scaling with aspect ratio preservation
- Interpolation methods:
  - Nearest Neighbor
  - Linear (Bilinear)
  - Cubic (Bicubic)
  - Area
  - Lanczos4

### 4. **Image Transformations**
- Flipping images (horizontal, vertical, both)
- Rotating images (90°, 180°, 270°)
- Cropping regions of interest (ROI)
- Affine transformations

### 5. **Drawing Lines and Shapes**
- Drawing lines with `cv2.line()`
- Creating rectangles with `cv2.rectangle()`
- Drawing circles with `cv2.circle()`
- Creating ellipses with `cv2.ellipse()`
- Drawing polygons with `cv2.polylines()`
- Understanding BGR color format
- Working with thickness and filled shapes

### 6. **Adding Text to Images**
- Using `cv2.putText()` function
- Available font types (HERSHEY fonts)
- Font scaling and thickness
- Text positioning
- Anti-aliasing for smooth text
- Getting text size with `cv2.getTextSize()`

### 7. **Color Thresholding**
- Binary thresholding
- Color range detection
- HSV-based color filtering
- Creating masks
- Practical applications

### 8. **Working with Video Files**
- Reading video files
- Processing video frames
- Writing video output
- Video properties (FPS, frame count, dimensions)
- Real-time video processing

## 🚀 Usage

1. **Start Jupyter Notebook:**
```bash
jupyter notebook
```

2. **Navigate to any topic folder and open the notebook**

3. **Run cells sequentially** to see the examples in action

4. **Experiment** with the code by modifying parameters and observing results

## 💡 Key Concepts

### Color Format
OpenCV uses **BGR** (Blue, Green, Red) format instead of RGB:
- Blue: (255, 0, 0)
- Green: (0, 255, 0)
- Red: (0, 0, 255)
- White: (255, 255, 255)
- Black: (0, 0, 0)

### Coordinate System
- Origin (0, 0) is at the **top-left corner**
- X-axis increases **rightward**
- Y-axis increases **downward**

### Image Representation
Images are represented as NumPy arrays:
- Grayscale: 2D array (height × width)
- Color: 3D array (height × width × 3 channels)
- Values range from 0-255 (uint8)

## 📖 Learning Path

**Recommended order for beginners:**

1. Reading and Writing Images
2. Exploring Color Spaces
3. Image Resizing and Scaling
4. Flip, Rotate, and Crop Operations
5. Drawing Lines and Shapes
6. Adding Text to Images
7. Color Thresholding
8. Working with Video Files

## 🛠️ Common Operations Quick Reference

```python
# Read image
img = cv2.imread('image.jpg')

# Convert BGR to RGB for matplotlib
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Display with matplotlib
plt.imshow(img_rgb)
plt.show()

# Resize image
resized = cv2.resize(img, (width, height))

# Draw rectangle
cv2.rectangle(img, (x1, y1), (x2, y2), (255, 0, 0), 2)

# Add text
cv2.putText(img, "Text", (x, y), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 2)

# Save image
cv2.imwrite('output.jpg', img)
```

## 🤝 Contributing

Contributions are welcome! If you'd like to add new tutorials or improve existing ones:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/new-tutorial`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new tutorial'`)
5. Push to the branch (`git push origin feature/new-tutorial`)
6. Create a Pull Request

## 📝 Notes

- All notebooks include detailed comments and explanations
- Sample images are provided in the `images/` directory
- Each notebook can be run independently
- Output images are saved in respective topic directories

## 🔗 Resources

- [OpenCV Official Documentation](https://docs.opencv.org/)
- [OpenCV Python Tutorials](https://docs.opencv.org/master/d6/d00/tutorial_py_root.html)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

Created for educational purposes to help others learn OpenCV and computer vision concepts.

---

**Happy Learning! 🎓**

If you find this repository helpful, please consider giving it a ⭐!
