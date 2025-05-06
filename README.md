# Implementation-of-Erosion-and-Dilation
# Aim
To implement Erosion and Dilation using Python and OpenCV.
# Software Required
1. Anaconda - Python 3.7
2. OpenCV
# Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.
 
# Program:
## Developed by: Kishore B
## Reg NO: 212224100032
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```

## Output:

![image](https://github.com/user-attachments/assets/fc675126-5b25-469d-bc8b-efd1de8da69d)

![image](https://github.com/user-attachments/assets/5ba57752-8b3f-4e4e-8b62-07ff93c4afb3)

![image](https://github.com/user-attachments/assets/1cc3f1e3-8ee5-40e1-a4b8-c2aada6aef88)


# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
