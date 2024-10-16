# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program and Output:

### Name: Sharangini T K
### Reg no:212222230143

```python
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread('cute.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![WhatsApp Image 2024-10-15 at 5 59 34 PM](https://github.com/user-attachments/assets/57291e2d-870e-4ec0-80f5-6cb00c4fd8d0)


### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined)
plt.title('sobel combined image')
plt.axis('off')
plt.show()
```
![WhatsApp Image 2024-10-15 at 5 59 36 PM](https://github.com/user-attachments/assets/2d0656f1-baf3-4358-b217-3e6ad63d0be1)

### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian)
plt.title('Laplacian image')
plt.axis('off')
plt.show()
```
![WhatsApp Image 2024-10-15 at 5 59 36 PM (1)](https://github.com/user-attachments/assets/7ec492e0-b2d3-4351-a473-aee863816a5c)

### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges)
plt.title('canny_edges Image')
plt.axis('off')
plt.show()
```
![WhatsApp Image 2024-10-15 at 5 59 36 PM (2)](https://github.com/user-attachments/assets/0731803a-4b8a-4ed4-a702-20c692323986)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

