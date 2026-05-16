# Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
## Experiment 8
## Name
Dharanya N
## Reg no 
212223230044
# Aim
To implement Erosion and Dilation using Python and OpenCV.

### Software Required
Anaconda - Python 3.7
OpenCV
# Algorithm:
### Step 1:
Import necessary libraries, including OpenCV (cv2) and Matplotlib (plt), to load, manipulate, and display images.

### Step 2:
Use cv2.putText() to add text to the image at a specific location with chosen font, size, color, and thickness.

### Step 3:
Define a structuring element using cv2.getStructuringElement() to specify the shape and size for morphological transformations.

### Step 4:
Apply erosion to the image using cv2.erode() with the structuring element to shrink white regions and reduce noise.

### Step 5:
Dilate the eroded image using cv2.dilate() with the structuring element to expand white regions and enhance features.

### Step 6:
Display the original and processed images using plt.imshow() with proper axis configuration and titles for comparison.

### Step 7:
Finalize by calling plt.show() to display all images in a single figure for easy visualization and comparison.

# Program:
Name : Dharanya N
Reg No : 212223230044
### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create a blank image
```python
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
### Add text on the image using cv2.putText
```python
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Dharanya', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
### Display the input image
```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
### Create a simple square kernel (3x3) and Apply erosion (shrinking effect)
```python
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
### Display the eroded image
```python
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
### Apply dilation (expanding effect) and Display the dilated image
```python
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```

# Output:
Display the input Image

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/3787aa60-b806-468a-b6fb-88a3cfbb0d1d" />






Display the Eroded Image

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/ebc20187-3d19-4a4b-930e-88cde57124f6" />




Display the Dilated Image


<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/77830a21-da3e-4c2c-84a2-4ad5cf9eb393" />





# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
