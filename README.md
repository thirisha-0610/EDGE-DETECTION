# EDGE-DETECTION
# NAME : THIRISHA A
# REG NO: 212223040228
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

(i) Display the original image
```
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("dog cat.jpg")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display Original Image
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()
```
(ii) Apply Sobel Edge Detection
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
# Display Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```
(iii) Apply Laplacian Edge Detection
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()

```
(iv) Apply Canny Edge Detection
```
canny_edges = cv2.Canny(gray_image, 50, 150)
# Display Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
# OUTPUT:
# ORIGINAL IMAGE:

<img width="371" height="370" alt="image" src="https://github.com/user-attachments/assets/92f37ddc-e195-4643-9cef-53d7f7b659ef" />

# SOBEL EDGE DETECTOR:
<img width="374" height="374" alt="image" src="https://github.com/user-attachments/assets/e6173d92-86e0-4a74-b346-e5442418815c" />

# LAPLACIAN EDGE DETECTOR:
<img width="369" height="375" alt="image" src="https://github.com/user-attachments/assets/db657bb6-3f5e-4797-ae5c-44a996f56860" />

# CANNY EDGE DETECTOR:
<img width="361" height="368" alt="image" src="https://github.com/user-attachments/assets/b2cca068-a75b-4705-94a9-bfe7fb20f1db" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
