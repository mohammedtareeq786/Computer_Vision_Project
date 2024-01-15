#Computer_Vision_Project

# Automatically Masking Cartridge Case Images
This Computer Vision project is a Python script that uses OpenCV and Matplotlib libraries to automatically mask cartridge case images for forensic analysis[1][2][3]. The script identifies different areas of a cartridge case image based on contours and applies different color masks to each area. This can be particularly useful in forensic analysis where different parts of the cartridge case need to be identified and analyzed separately.The process involves several steps:

Preprocessing Image: The first step involves reading an image file using a function like cv2.imread(). The image is then converted to grayscale using cv2.cvtColor(), which simplifies the image data and prepares it for thresholding. A binary threshold is applied to the grayscale image using cv2.threshold(), which separates the cartridge case regions from the background. The cv2.findContours() function is then used to find the contours of the cartridge case regions in the thresholded image[4].

Filtering Contours: The next step is to filter out unwanted contours. This is done by calculating the area and perimeter of each contour using cv2.contourArea() and cv2.arcLength(), and then applying conditions to these values to filter out contours that are too small or too large. The shape of each contour is also considered in the filtering process. The remaining contours are then labeled with indices for easy identification[5][6][7].


![image](https://github.com/mohammedtareeq786/Computer_Vision_Project/assets/133824825/60b1e6b8-7a3b-4da3-a59a-3eb24f9cc465)
Above is the Processes Image Filtering out The contours based on area and perimiter and then labeled with indices for easy identification.

Masking Contours: The final step is to mask the contours of interest with different colors. This is done by creating a blank mask image and then filling in the contours with cv2.drawContours()[8][9][10]. Different colors are used for different features of the cartridge case: red for the breech-face impression, green for the aperture shear, purple for the firing pin impression, and light blue for the firing pin drag. An arrow is also drawn on the image to indicate the direction of the firing pin drag.

![image](https://github.com/mohammedtareeq786/Computer_Vision_Project/assets/133824825/80bdcc3f-01bf-41e1-8565-2cc44c69adab)


Installation and Usage
To run this project, you need to have Jupyter Notebook and the following packages installed:

1. opencv-python
2. matplotlib
3. numpy 

You can install OpenCV using pip:

- pip install opencv-python
- pip install numpy
- pip install matplotlib

To use this project, you need to have a cartridge case image file named Cartridge_Cases.png in the same directory as the script. You can also change the image path in the code if you want to use a different file name or location.

Output:
The script allows you to mask different parts of the cartridge case image by specifying the contours. Here’s an example of how you might use it:

- Breech-face Impression (Red): To mask the breech-face impression in red, subtract Contour 7 from Contour 5. (First Enter Contour Index 5 Then Enter Contour Index 7)
- Aperture Shear (Green): To mask the aperture shear in green, use Contour 6.
- Firing Pin Impression (Purple): To mask the firing pin impression in purple, use Contour 8.
- Firing Pin Drag (Light Blue): To mask the firing pin drag in light blue, use Contour 7.
- Blue Arrow is drawn from Center of the Firing Pin impression to the direction of Firing Pin Drag.

After running the script with these inputs, you’ll see the image with the specified contours masked in their respective colors.

## References:


1. https://www.geeksforgeeks.org/using-matplotlib-with-jupyter-notebook/
2. https://numpy.org/install/
3. https://pypi.org/project/opencv-python/

4. https://docs.opencv.org/3.4/d4/d73/tutorial_py_contours_begin.html
5. https://www.geeksforgeeks.org/find-and-draw-contours-using-opencv-python/
6. https://medium.com/mlearning-ai/how-to-detect-contours-in-an-image-in-python-using-opencv-3c245cb1d4d
7. https://dontrepeatyourself.org/post/edge-and-contour-detection-with-opencv-and-python/

8. https://stackoverflow.com/questions/74463028/create-mask-with-filled-color-using-opencv
9. https://www.tasq.ai/glossary/image-masking/#:~:text=Imagine%20masking%20is%20an%20important,more%20precise%20and%20accurate%20results.
10. https://pyimagesearch.com/2021/01/19/image-masking-with-opencv/



Accesss Full Report: 

[Data Scientist (207729) Assignment Report.pdf](https://github.com/mohammedtareeq786/Computer_Vision_Project/files/13942968/Data.Scientist.207729.Assignment.Report.pdf)

