# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages


### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image.

 
## Program:

``` Python
 Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt



# Step 1: Load the input image using cv2.imread()
image = cv2.imread("fish.jpg") 

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 3: Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)

# Step 4: Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

# Plot the original, eroded, and dilated images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

# Erode the image

plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

# Dilate the image
plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")





```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/8403bfbd-ef86-4c25-99fa-b73ed21afb6a)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/4cf47db1-9058-45f5-8937-532b16e19b09)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/d19b44b6-3242-4420-b710-95d4117eeb02)

## Result.
Thus the generated text image is eroded and dilated using python and OpenCV.
