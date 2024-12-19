# Edge Detection Project

This project implements an **Edge Detection** algorithm for processing images. It converts a color image to grayscale, applies a convolutional mask, and visualizes the edges detected in the image.

---

## How the Project Works

### 1. **Input**
- An image is provided as input.
- The script converts the image to grayscale and processes it to detect edges.

### 2. **Core Steps**
- **Convert to Grayscale**: The color image is converted to grayscale using a weighted average of RGB channels.
- **Apply Convolution Mask**:
  - A 3x3 mask is defined for processing.
  - For each pixel, the mask is applied to its local neighborhood to compute the new value.
- **Output**:
  - The original image and the edge-detected image are visualized side by side.

---

## Project Files

### **`helper_functions.py`**
Contains helper functions for processing and visualizing images:
- `read_colorimg(imgpath)`: Reads a color image, converts it to grayscale, and pads it with zeroes.
- `verify_result(pixel_values, new_pixel_values, mask)`: Verifies the edge detection results against the expected output.
- `view_images(imgpath, new_pixel_values)`: Displays the original and processed images.

### **`edgedetect_assgn.py`**
Contains the main logic of the project:
- Reads the input image and converts it to grayscale.
- Defines a 3x3 convolutional mask.
- Applies the mask to detect edges.
- Verifies and visualizes the results.

---

## Python Libraries Used

This project relies on the following Python libraries:

- **`numpy`**: For numerical computations and matrix manipulations.
- **`matplotlib`**: For visualizing the original and processed images.
- **`scipy`**: For validating edge detection using convolution.
- **`skimage`**: For additional image processing functions.

---

## How to Run the Project

1. **Install Dependencies**:
   Make sure the required libraries are installed. Use the following command to install them:
   ```bash
   pip install numpy matplotlib scipy scikit-image
   ```

2. **Prepare Input Images**:
   - Place your images in the specified folder.
   - Update the `datafolder` variable in `edgedetect_assgn.py` with the correct folder path.

3. **Run the Script**:
   Execute the main script using Python:
   ```bash
   python edgedetect_assgn.py
   ```

4. **View Results**:
   - The original and edge-detected images will be displayed side by side.

---

## Example Usage

### Input Folder Setup
Ensure the `datafolder` variable in `edgedetect_assgn.py` points to your image directory:
```python
# Example folder setup
datafolder = "C:/path-to-your-images-folder/"
imgpath = datafolder + "example.jpg"
```

### Running the Script
Run the script and observe the results:
```bash
python edgedetect_assgn.py
```

---

## Future Enhancements
- Support for additional convolution masks for different edge detection algorithms (e.g., Sobel, Prewitt).
- Batch processing of multiple images in the folder.
- Adding command-line arguments for mask configuration and file paths.

---

Enjoy exploring image processing with this project! 🎨
