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

(i) Display the original image
```
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("rose.jpg")  # Replace with your image path
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

<img width="506" height="459" alt="495624128-ed4e1d40-9c3e-4888-8879-d0b434743cb8" src="https://github.com/user-attachments/assets/c362c733-4e4a-4e70-9dda-9558a51dc497" />
# SOBEL EDGE DETECTOR:

<img width="423" height="434" alt="495624283-c1ca338a-fa36-4b90-adf1-909425e6d7be" src="https://github.com/user-attachments/assets/9054719f-ef61-467b-adf8-e00ab5e7d106" />

# LAPLACIAN EDGE DETECTOR:
<img width="406" height="442" alt="495625534-25622cb3-3072-4835-b959-d68ab2362294" src="https://github.com/user-attachments/assets/77e9fb58-d5a1-4b64-8013-66b6c57b3bc5" />
# CANNY EDGE DETECTOR:
<img width="458" height="446" alt="495624449-7679638b-5d56-43f7-baff-b5453f34e5bc" src="https://github.com/user-attachments/assets/5510487a-33ac-4230-822f-00c3ab9d2a4f" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
