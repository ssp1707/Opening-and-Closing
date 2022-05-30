# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

## PROGRAM:
```
/*
Developed by   : S. Sanjna Priya
Register Number: 212220230043
*/
```

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Sanjna',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()
```

# Create the structuring element
```
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
```

# Use Opening operation
```
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()
```

# Use Closing Operation
```
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image
![11 1](https://user-images.githubusercontent.com/75234965/170945206-d28ca859-0013-4f68-ad1b-990029f3ebc6.PNG)

### Display the result of Opening
![11 2](https://user-images.githubusercontent.com/75234965/170945269-814c4091-363d-4ee4-8168-9da7afff3be9.PNG)

### Display the result of Closing
![11 3](https://user-images.githubusercontent.com/75234965/170945313-5d8b3c4f-c66f-44fb-9529-23d51a46b23a.PNG)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
