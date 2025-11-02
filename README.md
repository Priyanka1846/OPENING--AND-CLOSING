# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
 Import the necessary packages


### Step2:
 Give the input text using cv2.putText()


### Step3:
 Perform opening operation and display the result


### Step4:
 Similarly, perform closing operation and display the result



 
## Program:
DEVELOPES BY: PRIYANKA K

REG:212223230162

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'SIVA DINESH',(5,70), font,2,(255),5,cv2.LINE_AA)

```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation

```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<img width="542" height="497" alt="image" src="https://github.com/user-attachments/assets/42dcf410-a94e-4667-ab08-28d1f56375c5" />


### Display the result of Opening
<img width="541" height="499" alt="image" src="https://github.com/user-attachments/assets/724458f3-0395-4491-a7f6-6094d4ab16b0" />


### Display the result of Closing
<img width="538" height="494" alt="image" src="https://github.com/user-attachments/assets/0fd95306-c680-4b8e-88d9-a20a10a65780" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
