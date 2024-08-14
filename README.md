# Read_Write_BMP 

# BMP Image Processing 

# Overview

This project demonstrates how to read, manipulate, and write BMP image files using Python. The code is designed to support 24-bit RGB, 8-bit grayscale, and 8-bit color indexed BMP formats. The project reads BMP files, manipulates the color channels, and then saves the manipulated images.

# Files
```
image_processing.py: Contains all the functions to read, manipulate, and write BMP images.
cameraman.bmp: Sample BMP image file.
corn.bmp: Sample BMP image file.
pepper.bmp: Sample BMP image file.
corn_filter_red_channel.bmp: Image with the red channel removed.
corn_filter_blue_channel.bmp: Image with the blue channel removed.
corn_filter_green_channel.bmp: Image with the green channel removed.
```

# Functions

## read_bmp_image(filename)

This function reads a BMP file and returns its metadata and pixel data.

### Parameters:

filename: The name of the BMP file to read.

### Returns:

A dictionary containing the image's metadata and pixel data.

## write_bmp(image_data, filename) 

This function writes a BMP image to a file.

### Parameters:
```
image_data: The image data dictionary obtained from read_bmp_image.
filename: The name of the file to write the image to.
```
## remove_color(image_data, color_index, filename)

This function removes a specific color channel from the image and writes the result to a new file.

### Parameters:
```
image_data: The image data dictionary obtained from read_bmp_image.
color_index: The index of the color to remove (0 = Blue, 1 = Green, 2 = Red).
filename: The name of the file to save the modified image.
```
# Usage

## Reading BMP Files:

The code reads BMP files from a predefined list of filenames. It extracts metadata and pixel data from each file and prints them to the console.

## Writing BMP Files:

After reading the BMP files, the code writes the image data to new BMP files with _written_output appended to the original filename.

## Manipulating Color Channels:

For the corn.bmp image, the code removes specific color channels (Red, Blue, Green) and writes the resulting images to new files.

# Sample Output

After running the script, you should see the following files:
```
cameraman_written_output.bmp
corn_written_output.bmp
pepper_written_output.bmp
corn_filter_red_channel.bmp
corn_filter_blue_channel.bmp
corn_filter_green_channel.bmp
```
These files are the result of reading the original BMP files, manipulating them, and saving the outputs.

# Requirements

- Python 3.x
- No external libraries are required for this project.

# Notes

- This project is designed to handle only uncompressed BMP files.
- The project assumes that the color table is fully populated if the BMP is an 8-bit color indexed image.
