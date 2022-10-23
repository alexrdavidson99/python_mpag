# python_mpag
This is for feedback on my python code for the python mpag course.
images are taken of a  laser focused onto a CCD with different experimental set up`s i.e. laser with more power, we want to measure the size of the area the focused laser takes up on the CCD so that we are not pixel limiting when we set the actual experiment. knowing the pixel size and distribution this can be worked out.  



The idea of the code is to take pixel data (1D/2D arrays) from cropped images inputted in to output a 1D/2D plot to see if the distribution of the dataset is gaussian and if it is not gaussian get the closest distribution we can get i.e. super gaussian e.c.t.  using these distributions and getting FWHM and CCD pixel size for that image the area can be determined. 

#steps...

# 1) converting it into grayscale, 

# 2) take out data we don’t need, i.e. crop the image and take away noise 
then it will look for the highest pixel over a certain pixel threshold  value. it will then crop the image around this pixel by a set pixel value. (the user will have control of image size) 
images of when the laser was off were taken this is use for image subtraction. 

# 3) using matplot.lib a 2D scaled graph is created showing the cropped image (2D array). taking a certain y value a 1D plot of the distribution is created. 

# 4) using iminuit to find the gaussian distribution or not 

# 5) measure FWHM 
from that work with give you the diameter of the distribution scale this up to get the area, i.e. the final results.
