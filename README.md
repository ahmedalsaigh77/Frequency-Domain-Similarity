# Frequency Domain Similarity

## Overview
This project explores image similarity using frequency-domain analysis and signal-based comparison techniques.

It investigates how two images can be compared by extracting their frequency characteristics and analyzing the similarity between their resulting representations.

The experiment uses Python, NumPy, OpenCV, and Matplotlib to process images, extract frequency information, calculate similarity scores, and visualize the results.

## Objectives
- Understand frequency-domain image analysis.
- Apply the 2D Fast Fourier Transform (FFT) to images.
- Extract and visualize frequency magnitude spectra.
- Compare images using Pearson correlation.
- Extract one-dimensional signals from grayscale images.
- Analyze similarity between extracted signals using statistical correlation.

## Methods

### 1. Frequency Spectrum Comparison

This method compares two images using their frequency-domain representations.

**Processing Steps:**
1. Load both images in grayscale.
2. Resize each image to 256 × 256 pixels.
3. Apply the 2D Fast Fourier Transform (FFT).
4. Shift the zero-frequency component to the center using `fftshift`.
5. Calculate the logarithmic magnitude spectrum.
6. Flatten both spectra into one-dimensional arrays.
7. Calculate their similarity using the Pearson correlation coefficient.

The resulting correlation value indicates how strongly the two frequency spectra are linearly related.

### 2. Signal-Based Similarity Comparison

This method extracts one-dimensional signals from grayscale images and compares their patterns.

**Processing Steps:**
1. Load both images in grayscale.
2. Resize each image to 512 × 512 pixels.
3. Calculate the mean intensity across image rows.
4. Compute the first derivative of the extracted intensity signal.
5. Construct a signal by combining the derivative with a sinusoidal component.
6. Normalize both signals using Z-score normalization.
7. Calculate the Pearson correlation coefficient.
8. Convert the positive correlation value into a percentage.

The resulting percentage represents the positive correlation between the two normalized signals.

## Visualization

The project generates two types of visualizations:

- **Frequency Spectrum Visualization:** Displays the frequency magnitude spectra of both images side by side.
- **Signal Comparison Visualization:** Displays both normalized signals on the same plot to examine their patterns and correlation.

## Technologies Used
- Python
- OpenCV (cv2)
- NumPy
- Matplotlib

## Installation

Install the required libraries:

```bash
pip install numpy opencv-python matplotlib
```

## How to Run

1. Clone this repository.
2. Install the required dependencies.
3. Open `app.ipynb` using Jupyter Notebook or VS Code.
4. Update the image paths in the notebook to point to your own images.
5. Run the notebook cells sequentially.
6. Observe the calculated similarity scores and visualizations.

## Notes
- Both images should be readable and accessible through the specified file paths.
- The frequency spectrum comparison uses images resized to 256 × 256 pixels.
- The signal-based comparison uses images resized to 512 × 512 pixels.
- Similarity scores are based on Pearson correlation and should not be interpreted as universal measures of visual similarity.

## Conclusion

This experiment demonstrates two approaches to image similarity analysis: comparing frequency magnitude spectra using the 2D Fourier Transform and comparing image-derived signals using statistical correlation.

It provides a practical introduction to frequency-domain processing, signal extraction, correlation analysis, and image visualization.

---

**Project:** Frequency Domain Similarity  
**Language:** Python  
**Environment:** VSCode.