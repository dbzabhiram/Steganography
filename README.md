# Steganography

In this project, we hide a secret message inside an Image by changing the bit values of respective R, G and B values of the image's pixel values. These are done seperately in three scripts: hide.py (blue bits), hidered.py(red bits), hidegreen.py(green bits). We use chm.py for qualitative measures on stego and original image. This project is work of two-member team, under the Minor project of college semester.

Help for how to use the given Python scripts
--------------------------------------------

Pre-requisite
-------------

1. Linux Terminal
2. Python 2.7.5 or above
3. Image file in '.png' or '.jpg' format
4. Python scripts (hide.py, hidered.py and hidegreen.py)

(Keep the given Python files and images in same folder.)


Encryption
----------

1. For encryption purpose, open the terminal and go the folder containing the Python script along with the image.
2. Use the following command: python (python-scriptname).py -e (image-filename).png
3. Enter the text which is to be hidden in the image.
4. If hide.py is used, then file name of stego-image so created will be "image-filename.pngblue". 
If hidered.py is used, then file name of stego-image so created will be "image-filename.pngred". 
If hidegreen.py is used, then file name of stego-image so created will be "image-filename.pnggreen".

Decryption
----------

1. For decryption purpose, open the terminal and go the folder containing the Python script along with the stego-image.
2. If stego-image is ending with extension ".pngblue", use command: python hide.py -d (image-filename).pngblue. 
If stego-image is ending with extension ".pngred", use command: python hidered.py -d (image-filename).pngred. 
If stego-image is ending with extension ".pnggreen", use command: python hidegreen.py -d (image-filename).pnggreen.
3. The secret text will be obtained in the next line.


Image Distortion Measurement
----------------------------

1. For calculation of Mean Squared Error (MSE), Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity Index Measure (SSIM) of two images, we use chm.py program. You must keep the images and chm.py script in the same folder.
2. Open the terminal and go to that particular folder.
3. Use the following command: python chm.py (image1-filename) (image2-filename)
For example, "python chm.py 1.png 1.pngblue"
4. The result of these measures will be displayed on the screen. Please keep in mind that if two exactly same images is used for comparison, then error will occur due to division by zero error in SSIM method.

Credits
-------

Video on YouTube by DrapsTV (Steganography Tutorial - Hiding Text inside an Image: https://youtu.be/q3eOOMx5qoo)
