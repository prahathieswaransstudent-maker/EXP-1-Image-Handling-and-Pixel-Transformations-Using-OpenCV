# EXPERIMENT 01: Image Handling and Pixel Transformations Using OpenCV


**Name:** Prahathieswaran S

**Register Number:** 212225240107  

---

## Aim
To perform basic image handling operations—reading, resizing, converting color spaces, drawing geometric shapes (lines, circles, rectangles), and overlaying text—using OpenCV and Matplotlib in Python.

---

## Software Required
- Python 3.x
- OpenCV (`opencv-python`)
- Matplotlib (`matplotlib`)
- Jupyter Notebook / Google Colab / VS Code

---

## Algorithm

### 1. Image Loading and Color Conversion
1. Start the program and import the required libraries: `cv2` and `matplotlib.pyplot`.
2. Read the source image (`Qno. 1.jpg`) into a variable using `cv2.imread()`.
3. Convert the color channel arrangement from BGR (OpenCV's default) to RGB using `cv2.cvtColor(image, cv2.COLOR_BGR2RGB)`.
4. Plot and render the original image with axes turned off using `plt.imshow()`, `plt.title()`, and `plt.show()`.

### 2. Resizing and Annotations
1. Resize the original image matrix to dimensions $768 \times 600$ using `cv2.resize()`.
2. Convert the resized image from BGR to RGB for canvas drawing.
3. Draw a line from the top-left coordinate `(0, 0)` to the bottom-right coordinate `(768, 600)` with RGB color `(255, 0, 0)` and line thickness `2` using `cv2.line()`.
4. Draw a circle centered at `(400, 180)` with a radius of `150`, RGB color `(255, 0, 0)`, and thickness `8` using `cv2.circle()`.
5. Draw a bounding rectangle from top-left `(250, 50)` to bottom-right `(550, 350)` with color `(0, 255, 0)` and thickness `3` using `cv2.rectangle()`.
6. Overlay the string `"OpenCV Drawing"` at coordinate `(30, 50)` using `cv2.putText()` with font `FONT_HERSHEY_SIMPLEX`, scale `1.2`, color `(0, 0, 255)`, thickness `2`, and anti-aliased line type `cv2.LINE_AA`.

### 3. Output Display
1. Configure a Matplotlib figure of size $8 \times 6$.
2. Display the annotated image with the title `"Modified Image with Shapes and Text"` and axes disabled.
3. End the program.

---

```python
## Program

import cv2
import matplotlib.pyplot as plt


# Read the image using OpenCV
img = cv2.imread('Qno. 1.jpg', cv2.IMREAD_COLOR)

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Display the image using Matplotlib
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```

<<<<<<< HEAD
![alt text](image.png)



```python
# Load the image
image = cv2.resize(image, (768, 600))

image = cv2.imread('Qno. 1.jpg') 


# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)


# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)


plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```


```python
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)

plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

```python
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)


# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)


plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```


```python
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Add text to the image
text_img = cv2.putText(img_rgb, "MUTHUAKASH M", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 0), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)


plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```


```python
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)


# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```


```python
# Convert RGB to GRAYa
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```


```python
# Load the image
image = cv2.imread('Qno. 1.jpg') 

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)


# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```



```python
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)


# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```



## Result
Thus, the Python program to perform basic image handling operations—reading, resizing, color space transformation, drawing geometric shapes (line, circle, rectangle), and annotating text onto the image using OpenCV and Matplotlib—was executed successfully.
