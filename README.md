# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

```
# Developed By: DILIP M P
# Register No: 212223230048

import cv2
import numpy as np
import matplotlib.pyplot as plt


image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'DILIP M P', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

dilated_image = cv2.dilate(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')





```
## Output:

### Display the input Image:
![Screenshot 2025-05-06 094854](https://github.com/user-attachments/assets/539fda9c-61e1-43f5-92a3-411e72f2d829)




### Display the Eroded Image:
![Screenshot 2025-05-06 094909](https://github.com/user-attachments/assets/7818c9fe-9284-4033-be8e-1ca8dba1c924)



### Display the Dilated Image:
![Screenshot 2025-05-06 094924](https://github.com/user-attachments/assets/5193254e-dd81-4332-8a24-5da124d72c37)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
