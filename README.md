# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

## Program:
```python
Developed By:MARINO SARISHA T
Register Number:212223240084
i)Image Translation

import cv2
import matplotlib.pyplot as plt
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Original Image")  
plt.axis('off') 
tx, ty = 100, 50 
M_translation = np.float32([[1, 0, tx], [0, 1, ty]]) 
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))  
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))
plt.title("Translated Image")  
plt.axis('off')

ii) Image Scaling

fx, fy = 5.0, 2.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))
plt.title("Scaled Image")
plt.axis('off')

iii)Image shearing

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))
plt.title("Sheared Image")
plt.axis('off')

iv)Image Reflection

reflected_image = cv2.flip(image, 2) 
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB)) 
plt.title("Reflected Image")  
plt.axis('off')

v)Image Rotation

(height, width) = image.shape[:2]  
angle = 45  
center = (width // 2, height // 2) 
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))  
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
### INPUT IMAGE
![pb](https://github.com/user-attachments/assets/ea304bca-0a36-4503-b878-1e2500c68c30)

### i)Image Translation
![Screenshot 2025-04-11 111219](https://github.com/user-attachments/assets/41ba605f-fcc2-4c7f-bfa2-80fc74037c03)

### ii) Image Scaling
![Screenshot 2025-04-11 111229](https://github.com/user-attachments/assets/0cd35b30-f440-476e-88ad-c78f9692535d)

### iii)Image shearing
![Screenshot 2025-04-11 111237](https://github.com/user-attachments/assets/545325d8-1733-4f1b-9ef1-625755ec7167)

### iv)Image Reflection
![Screenshot 2025-04-11 111246](https://github.com/user-attachments/assets/3bbef5af-82ea-4f64-b130-48b1d9af7a9b)

### v)Image Rotation
![Screenshot 2025-04-11 111253](https://github.com/user-attachments/assets/a67ef1db-0d90-40ca-a60d-25548415134e)


### vi)Image Cropping
![Screenshot 2025-04-11 111306](https://github.com/user-attachments/assets/f999ba02-cb55-4b9f-b185-497dedc2ec5d)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
