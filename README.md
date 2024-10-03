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

## Output:
```
 NAME:BALA MURUGAN P
 REG NO: 212222230017
```
```
import matplotlib.pyplot as plt
import cv2
# Read the image using imread
img = cv2.imread('goat.jpg')  # Replace 'image_path.jpg' with the actual path to your image

# Convert the color to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)

# Sobel X axis
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# Sobel Y axis
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

# Sobel XY axis
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
```
# Laplacian Edge Detector
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(lap, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
```
# Canny Edge Detector
canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/9838960e-2925-4409-a656-9d8946f78cb0)

![image](https://github.com/user-attachments/assets/e95e24fa-d6c6-4717-9c4c-d4bba795732b)

![image](https://github.com/user-attachments/assets/418cbb23-2082-447f-be21-d0343cad56a1)

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/5287dcd4-86bd-43dc-a0ea-2d401e017882)



### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/22ca6521-4f84-4ecb-ad11-6dfd1460bd14)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
