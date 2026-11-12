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

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/06600635-6339-4ab8-8982-a9282dfe8a22" />




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

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/54f62f34-5971-4841-bbc0-0b449e84fde7" />


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

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/eb8c1219-dc1a-404f-a074-6c0098d7f0a2" />


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

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/63828900-eef6-42a7-8397-f37d23ba3ee1" />



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

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/33daab44-d247-47c5-9d53-d767d3bc2785" />


```python
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)


# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/f75bf734-d68b-4695-a6a4-91fc95f1cff9" />
```
# Load the image
image = cv2.imread(image_path)
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
```

```
(1536, 1024, 3)
```

```
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/81141338-1f3c-4909-a08e-b194efa00304" />


```python
# Convert RGB to GRAYa
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/b431e28c-6a78-4600-a305-f28eadcee130" />

```
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/a5771b71-8b9e-4921-94d5-3b7db4bbc392" />


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

```
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/c4c0c045-4d3f-4171-b792-269b85ba727d" />

```
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

<img width="294" height="411" alt="image" src="https://github.com/user-attachments/assets/339ca716-efb7-4f67-9342-a09b4e727cb0" />

```
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
```
```
(300, 384, 3)
```

```
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

<img width="493" height="411" alt="image" src="https://github.com/user-attachments/assets/0592e214-d2e1-404d-9c3d-733e2b7e271d" />

```
# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/02321761-7b78-4e12-ac40-377fe5d0de11" />

```
# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)
# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/e3220a6b-61f1-4130-bd49-db4e575c3ae1" />


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
<img width="266" height="411" alt="image" src="https://github.com/user-attachments/assets/4f7c5d3a-1ad5-4a4b-bd2f-bf0335878e50" />



## Result
Thus, the Python program to perform basic image handling operations—reading, resizing, color space transformation, drawing geometric shapes (line, circle, rectangle), and annotating text onto the image using OpenCV and Matplotlib—was executed successfully.
