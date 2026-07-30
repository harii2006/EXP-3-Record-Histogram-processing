# EXP-3-Record-Histogram-processing
# AIM :
To perform histogram processing and histogram equalization on grayscale and color images using OpenCV. To enhance image contrast and compare the original and equalized histograms.

# SOFTWARE REQUIRED :
## Developed By : SHRIHARI M
## Register Number: 212225230265
## Title : EXP-3-Record-Histogram processing.
```
--> Anaconda - Python 3.7
--> Jupyter Notebook (for interactive development and execution)
```
# ALGORITHM :
Step 1:
Read the input image in grayscale and display the original image with its histogram.

Step 2:
Apply histogram equalization to the grayscale image using cv2.equalizeHist().

Step 3:
Display the equalized grayscale image and its histogram for comparison.

Step 4:
Read the original image in color and convert it from BGR to HSV color space.

Step 5:
Apply histogram equalization to the V (Value) channel of the HSV image.

Step 6:
Convert the modified HSV image back to BGR color space and display the enhanced color image.

Step 7:
Compare the original and equalized images along with their histograms to observe the improvement in contrast.

# PROGRAM:
Read and Display the Original Grayscale Image :
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = cv2.imread('e.jpg', cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()

plt.hist(img.ravel(), 256, range=[0, 256])
plt.title('Original Histogram')
plt.show()

```
Perform Histogram Equalization on Grayscale Image
```
img_eq = cv2.equalizeHist(img)

plt.imshow(img_eq, cmap='gray')
plt.title('Equalized Image')
plt.show()

plt.hist(img_eq.ravel(), 256, range=[0, 256])
plt.title('Equalized Histogram')
plt.show()
```
Compare Original and Equalized Images with Histograms
```
plt.subplot(221)
plt.imshow(img[:, :, ::-1])
plt.title('Original Color Image')

plt.subplot(222)
plt.imshow(img_eq[:, :, ::-1])
plt.title('Equalized Image')

plt.subplot(223)
plt.hist(img.ravel(), 256, range=[0, 256])
plt.title('Original Histogram')

plt.subplot(224)
plt.hist(img_eq.ravel(), 256, range=[0, 256])
plt.title('Equalized Histogram')
plt.show()
```
# OUTPUT:
<img width="552" height="307" alt="image" src="https://github.com/user-attachments/assets/5f538d7a-3ca8-42eb-b540-b6b0beac629a" />

<img width="565" height="425" alt="image" src="https://github.com/user-attachments/assets/a34fd43d-5ad7-4139-95da-a90495581e3a" />

<img width="572" height="433" alt="image" src="https://github.com/user-attachments/assets/9fd8e1f4-56eb-4c17-8c93-d3e9fac2dd0a" />

<img width="557" height="306" alt="image" src="https://github.com/user-attachments/assets/712e4807-2daa-471a-96dc-df69a6d30ef5" />

<img width="570" height="318" alt="image" src="https://github.com/user-attachments/assets/ba8d7cb4-8a5f-433b-a4d0-708646223a6f" />

<img width="587" height="435" alt="image" src="https://github.com/user-attachments/assets/86341773-37e8-42b5-a175-d8905efa1b98" />

<img width="582" height="395" alt="image" src="https://github.com/user-attachments/assets/0aeb80a8-5e9d-4a23-abe4-126e4500b8fa" />

<img width="607" height="185" alt="image" src="https://github.com/user-attachments/assets/41658305-3502-4115-bcf8-ea642226fb70" />

# RESULT :
Histogram equalization successfully improved the image contrast by redistributing pixel intensity values. The equalized images showed enhanced visual quality with a more uniform intensity distribution compared to the original images.

