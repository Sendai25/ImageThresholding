# ImageThresholding
A C++ project converting bitmap to greyscale and thresholding it to binary image with standard lib only.

## Technique
Image thresholding is a common task in many computer vision and graphics applications. The goal of
thresholding an image is to classify pixels as either “dark” or “light”. 

### Adaptive Thresholding
Adaptive thresholding is a form of thresholding
that takes into account spatial variations in illumination. This technique is designed for real-time adaptive thresholding
using the integral image of the input, which is an extension of a previous method. However, this solution
is more robust to illumination changes in the image. The technique is suitable for processing live video streams at a real-time frame-rate, making it a valuable tool for interactive applications such as augmented reality.

### Integral Image
An integral image (also known as a summed-area table) is a tool that can be used whenever we have a function
from pixels to real numbers f(x,y) (for instance, pixel intensity), and we wish to compute the sum of this function
over a rectangular region of the image. In image thresholding, the integral image helps to identify the illumination status of any specific rectangular, and it requires only one traverse of the image matrix, which is efficient for the performance.

## Instuction and Examples
This C++ standard lib based project requires an image input named "raw.bmp" and outputs "gray.bmp" and "binary.bmp" successively. "gray.bmp" is the grayscale image of the input while "binary.bmp" is the product binary image. The console would output the information of the image and the processing duration of each phase.

### Console Output
![raw.bmp](https://github.com/Sendai25/ImageThresholding/blob/master/Compressed_image/console.jpg)

### Example "raw.bmp"
![raw.bmp](https://github.com/Sendai25/ImageThresholding/blob/master/Compressed_image/raw.jpg)

### Example "gray.bmp"
![raw.bmp](https://github.com/Sendai25/ImageThresholding/blob/master/Compressed_image/gray.jpg)

### Example "binary.bmp"
![raw.bmp](https://github.com/Sendai25/ImageThresholding/blob/master/Compressed_image/binary.jpg)

## Reference
Introduction of the technique is extracted from *Adaptive Thresholding Using the Integral Image* by Derek Bradley and Gerhard Roth.
