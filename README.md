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
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image using angle function.

## Program:
```python
Developed By: Thirisha.S
Register Number: 212222230160
```

### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("rajini.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/7b314342-0c35-43c7-806d-1701d0dc535a)

![Screenshot 2024-04-12 085246](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/ff605f8d-2b85-4252-93e6-1a72ca452303)



### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/dc2cae8c-c241-4b45-9f0d-f8f7f237ec2d)

![Screenshot 2024-04-12 085322](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/4fcf6d0a-5a44-4522-8fca-a0b03523c136)


### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/f8a49715-b4d7-4bcf-b480-e3ec75378c9f)
      
![Screenshot 2024-04-12 085406](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/1a1a275d-58a8-4f97-aad3-247b09a709c3)

### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/e5f72f15-5f68-4a76-8a6d-033dd0ccb102)
       
![Screenshot 2024-04-12 085439](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/82ca39a9-c7b9-4740-942c-d7ea6e2b525b)



### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/98dc10bb-8828-4814-80cf-b577e10be794)

![Screenshot 2024-04-12 085519](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/edcc5cc7-9956-4ed9-a418-b05d8225cea3)



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```
![image](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/1cc57c04-c6c0-49e9-85c7-c35178aaf087)

![Screenshot 2024-04-12 085553](https://github.com/Thirisha-s/IMAGE-TRANSFORMATIONS/assets/120380280/07786a18-f989-47fb-97fb-1b146def240f)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
