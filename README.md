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


plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

# Erode the image



plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

# Dilate the image

plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")





```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/86e9cd9f-ff4a-4909-bdee-a6a0c13fb35a)

### Display the Eroded Image
![image](https://github.com/user-attachments/assets/23e297bf-7d6e-44e3-9f93-773145727d42)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/3a2f2b20-5892-486d-96e3-f9f7a1c5b0bb)

### RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.



