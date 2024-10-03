# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

# Developed By: Dhivyapriya.R
# Register Number: 212222230032
```
// for bright image

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('img1.tif')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()

// for dark image

import cv2
import numpy as np
from matplotlib import pyplot as plt

image = cv2.imread('img2.tif')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

equalized_image = cv2.equalizeHist(gray_image)

plt.figure(figsize=(10, 7))

plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

plt.subplot(2, 2, 3)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
```
## Output:
### Bright image:
![image](https://github.com/user-attachments/assets/b355aec8-220b-4b29-b749-5239ea22d8d1)

![image](https://github.com/user-attachments/assets/0f756a57-50a5-46f4-8143-c4bcedfdce1d)

//histogram image

![image](https://github.com/user-attachments/assets/a66ab973-014d-40c6-9ef0-3e5dc9a16f77)

![image](https://github.com/user-attachments/assets/b51a3faa-ad5d-4e9a-9af6-7d469cdb1944)

### Dark image:

![image](https://github.com/user-attachments/assets/c0c00067-475d-4465-b172-11624131cc3a)

![image](https://github.com/user-attachments/assets/2c999a37-138c-471b-8098-1376d64250bf)

//histogam image

![image](https://github.com/user-attachments/assets/09b6f00a-5edf-4ca1-ace9-f62f7f35c86a)

![image](https://github.com/user-attachments/assets/bd691663-888d-40d0-9714-b66624fb9524)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
