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
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'MABBU ADARSH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))

# Use Opening operation
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

# Use Closing Operation
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")

```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/472afd5a-8856-437c-a200-a3dd132ed3b6)

### Display the result of Opening
![image](https://github.com/user-attachments/assets/6f0e6124-8958-482e-bee9-be768593578a)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/1a005484-61f8-4a21-9a17-1aa7df812de1)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
