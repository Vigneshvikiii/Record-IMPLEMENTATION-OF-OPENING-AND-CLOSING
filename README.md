# EXP - 10 - OPENING--AND-CLOSING

# Developed By: Vignesh S

# Reg No : 212223230240

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
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'VIGNESH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

original_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opened_rgb = cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB)
closed_rgb = cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(12,5))

plt.subplot(1,3,1)
plt.imshow(original_rgb)
plt.title("Input Image with Text")
plt.axis('off')

plt.subplot(1,3,2)
plt.imshow(opened_rgb)
plt.title("Opening Operation")
plt.axis('off')

plt.subplot(1,3,3)
plt.imshow(closed_rgb)
plt.title("Closing Operation")
plt.axis('off')

plt.show()

```
## Output:

### Display the input Image

<img width="203" height="187" alt="image" src="https://github.com/user-attachments/assets/8016f345-0822-43ef-81ab-e7510f43a74b" />

### Display the result of Opening

<img width="181" height="187" alt="image" src="https://github.com/user-attachments/assets/30d35c46-6949-40ce-bd32-b8a9554605d5" />

### Display the result of Closing

<img width="172" height="187" alt="image" src="https://github.com/user-attachments/assets/b81cbf4e-9f66-4ff7-9c47-b548d3db35e5" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
