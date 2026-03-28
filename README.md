# Lane-Detection-OpenCV
A computer vision pipeline implemented in Python to detect road lanes using Canny edge detection and bitwise masking to isolate specific regions of interest.

This project implements a foundational computer vision pipeline used in autonomous vehicle systems. It focuses on isolating road lanes from a complex environment by defining a spatial "Region of Interest" (ROI) and applying edge detection algorithms.

## 🚀 Key Features
* **Dynamic ROI Masking**: Uses a custom polygonal mask to isolate the road surface, effectively ignoring background noise like trees, buildings, and the sky.
* **Canny Edge Detection**: Implements multi-stage gradient analysis to identify sharp intensity changes corresponding to lane markings.
* **Bitwise Operations**: Utilizes `cv2.bitwise_and` to combine edge maps with spatial masks for high-precision feature extraction.
* **Gaussian Blurring**: Includes noise reduction preprocessing to ensure the edge detector focuses on actual road lines rather than pavement texture.
* **Layered Visualization**: A comparative layout showing the grayscale conversion, the isolated ROI, and the final detected edges.

## 🗺️ Navigation Flow
The project is organized into a clear processing stream:

1.  **Dependency Setup**: Loads `cv2`, `numpy`, and `matplotlib`.
2.  **Interactive Image Input**: A Google Colab upload widget allows you to test the pipeline on different road conditions.
3.  **Image Preprocessing**:
    * Conversion to Grayscale for intensity analysis.
    * Gaussian Noise reduction.
4.  **Spatial Filtering**:
    * Definition of the triangular/polygonal vertices for the road area.
    * Creation of a zero-intensity mask.
    * Application of the mask to the Canny output.
5.  **Output Analysis**: Displays the final processed frame where only the relevant lane lines are highlighted.

## 🛠️ Requirements
- Python 3.x
- OpenCV (`opencv-python`)
- NumPy
- Matplotlib

## 📖 How to Use
1. Open `Lab_Task_05.ipynb` in Google Colab.
2. Run the cells in order.
3. Upload an image of a road or highway when prompted.
4. Adjust the ROI vertices in the code if you are using an image with a different camera angle!
