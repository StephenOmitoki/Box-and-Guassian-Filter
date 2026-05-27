# Box-and-Guassian-Filter
A hands-on image processing pipeline built with Python and OpenCV, covering spatial filtering, intensity segmentation, histogram analysis, and ROI extraction. Developed as part of my coursework in Image Processing &  Computer Vision at Northwestern Polytechnic, Alberta (NWP).

Image Processing Pipeline

A Python-based image processing pipeline implementing common computer vision operations including filtering, segmentation, histogram analysis, and region-of-interest (ROI) extraction using manually implemented and library-supported techniques.

Features
Image Processing Operations
Grayscale Conversion
Converts a color image from BGR format to grayscale for downstream processing.
5×5 Box Filter
Applies a manually constructed averaging kernel using mirror border reflection.
Gaussian Filtering
Performs Gaussian smoothing at two sigma values to compare blur intensity:
σ = 1
σ = 2
16-Level Intensity Segmentation
Quantizes the grayscale intensity range (0–255) into 16 equal intervals and maps each segment to a unique RGB color.

Histogram Analysis
Computes a manual pixel-frequency histogram across all 256 grayscale intensity levels.

ROI Mask Extraction
Detects the dominant image intensity and generates a binary ROI mask using a ±15 intensity tolerance window.

Output

The script generates two Matplotlib figures:

Figure 1 — Image Processing Results (2×3 Grid)
Original Image
Grayscale Image
5×5 Box Filter Output
Gaussian Filter (σ = 1)
16-Level Color Segmentation
ROI Binary Mask

Figure 2 — Histogram Visualization
Bar chart showing grayscale intensity frequencies (0–255)

Console Output
ROI intensity with highest number of pixels = <value>
Number of pixels in ROI intensity = <count>

Requirements

Install dependencies:

pip install opencv-python numpy matplotlib

Usage
1. Clone or Download the Repository

git clone <repository-url>
cd <repository-folder>

2. Specify the Input Image Path

Update the image_path variable in the script:

image_path = "path/to/your/image.jpg"

3. Run the Script
python image_pipeline.py

Concepts Covered:

Concept	Implementation
Spatial Filtering	Manual box kernel + cv2.filter2D()
Gaussian Smoothing	cv2.GaussianBlur() with σ = 1 and σ = 2
Intensity Quantization	Integer division (// 16) for 16-level segmentation
Colour Mapping	Custom  16-color lookup table (LUT)
Histogram Computation	Manual pixel-counting loop
ROI Detection	Dominant intensity + tolerance window masking

References
Gonzalez & Woods, Digital Image Processing (4th Edition) — Chapters 3 & 5
OpenCV Documentation: https://docs.opencv.org

Author

Stephen Omitoki
Computer Systems Technology
Northwestern Polytechnic (NWP), Alberta, Canada

Course: Image Processing & Computer Vision
