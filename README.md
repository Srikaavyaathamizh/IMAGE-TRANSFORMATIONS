# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required libraries and images for the experiment
</br

### Step2:
<br>
Translate the image using wrapAffine and the same can be used for Shearing the image



### Step3:
<br>
Use cv2.resize() to scale the image



### Step4:
<br>

use cv2.flip(img,2) to get the reflected image



### Step5:
<br>
Crop the image by using slicing



## Program:
```
Developed By: SRIKAAVYAA T
Register Number:212223230214
i)Image Translation

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('5.png')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB) 
plt.imshow(image_rgb)
plt.title("Original Image")

rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')


ii) Image Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR) 
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')



iii)Image shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')


iv)Image Reflection
reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')




v)Image Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')




vi)Image Cropping
 x, y, w, h = 100, 100, 200, 150 
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB)) 
plt.title("Cropped Image")  
plt.axis('off')


```
## Output:
### i)Image Translation
![image](https://github.com/user-attachments/assets/71511483-b561-4b99-9ccd-e5cb325b0597)

### ii) Image Scaling
![image](https://github.com/user-attachments/assets/ed6d806b-49f3-4830-8a86-ef0835dd997e)



### iii)Image shearing
![image](https://github.com/user-attachments/assets/6780b21d-c91f-4469-894b-5db3c78f4b34)


### iv)Image Reflection
![image](https://github.com/user-attachments/assets/92c6df74-8bd5-4a19-9d3c-b4f695381778)




### v)Image Rotation
![image](https://github.com/user-attachments/assets/469b310d-fc92-461b-a75e-0928ded769fd)





### vi)Image Cropping


![image](https://github.com/user-attachments/assets/501eb1b2-51f6-45d9-bc37-125c5b5da7dc)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
