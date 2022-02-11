# Histogram equalization algorithm on FPGA
The purpose of the project is to make a hardware component that performs an equalization algorithm of the histogram of an image, designed to recalibrate the contrast of the input image by distributing the intensity values of the pixels over a wider range. The component implements a revised version of this method, where the input images are represented as a sequence of integer values that represent the intensity on a grayscale of the pixels, following this algorithm:
```
DELTA_VALUE = MAX_PIXEL_VALUE – MIN_PIXEL_VALUE 
SHIFT_LEVEL = (8 – FLOOR(LOG2(DELTA_VALUE +1))) 
TEMP_PIXEL = (CURRENT_PIXEL_VALUE - MIN_PIXEL_VALUE) << SHIFT_LEVEL 
NEW_PIXEL_VALUE = MIN( 255 , TEMP_PIXEL)
```
