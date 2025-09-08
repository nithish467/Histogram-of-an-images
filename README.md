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
```python
# Developed By: NITHISHKUMAR S
# Register Number: 212223240109

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('nithish.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

equalized_image = cv2.equalizeHist(gray_image)

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

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
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()

```
## Output:
### Input Grayscale Image and Color Image
<img width="277" height="307" alt="image" src="https://github.com/user-attachments/assets/14cfac09-5e0d-47f1-9286-c3247d203d29"/>




### Histogram of Grayscale Image and any channel of Color Image
<img width="277" height="307" alt="image" src="https://github.com/user-attachments/assets/7f92ca7e-09d1-44a7-a7c3-6c973862f821" />

<img width="462" height="335" alt="image" src="https://github.com/user-attachments/assets/e6e3916b-b895-4768-905d-fe612b0b85e2" />


### Histogram Equalization of Grayscale Image.
<img width="236" height="307" alt="image" src="https://github.com/user-attachments/assets/bd72e7c7-72e1-48ef-875d-9a19a712b03b" />

<img width="472" height="326" alt="image" src="https://github.com/user-attachments/assets/f48af9f9-7792-483a-9019-fa4d27ec89bf" />






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
