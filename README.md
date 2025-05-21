# IMAGE-TRANSFORMATIONS

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules

### Step2:
Choose an image and save it as filename.jpg

### Step3:
Use imread to read the image

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

## Program:
```
Developed By:POPURI SRAVANI
Register Number:212223240117
import cv2
import numpy as np
import matplotlib.pyplot as plt

input_image=cv2.imread("img0.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()

i)Image Translation

rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

ii) Image Scaling

rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()

iii)Image shearing

rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

iv)Image Reflection

rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()

v)Image Rotation

rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()


vi)Image Cropping

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("img0.jpg")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
print("Image Cropping:")
plt.axis("off")
plt.show()

```
## Output:
![image](https://github.com/user-attachments/assets/e0bbeff7-5b4c-45ad-98d3-19cbed0656bf)


### i)Image Translation
![image](https://github.com/user-attachments/assets/70e74594-ca8f-4b63-8ea3-064ade44eff9)


### ii) Image Scaling
![image](https://github.com/user-attachments/assets/d0b73b3f-e8c8-4bab-847f-5eb1487bd75c)


### iii)Image shearing
![image](https://github.com/user-attachments/assets/b3dd7fe5-3e78-4095-a719-47f7edfef57e)


### iv)Image Reflection
![image](https://github.com/user-attachments/assets/37d22899-4e6f-49ce-99cd-261861393974)


### v)Image Rotation
![image](https://github.com/user-attachments/assets/b38fb002-4c92-47f0-a738-59e0bff2ee9c)


### vi)Image Cropping
![image](https://github.com/user-attachments/assets/c3d7188b-ab19-44bb-ad65-7f40a1dde4fb)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
