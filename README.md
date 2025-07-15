# Local Binary Pattern (LBP) Feature Extraction

This repository contains both built-in and custom implementations of the Local Binary Pattern (LBP) algorithm used for texture feature extraction in image processing tasks.

## Overview

Local Binary Pattern (LBP) is a powerful texture descriptor that encodes the relationship between a pixel and its surrounding neighbors. By thresholding the neighborhood of each pixel, LBP captures micro-patterns useful for tasks such as texture classification and facial recognition.

## Features

- Built-in LBP using `skimage.feature.local_binary_pattern`
- Custom 3x3 LBP implementation for greater control and understanding
- Works on grayscale images
- Ideal for texture analysis and classification

## Logic of Custom LBP

The `custom_lbp()` function processes a grayscale image by sliding a 3x3 window across each pixel. It compares each neighbor with the center pixel: if the neighbor is greater than or equal, it assigns a binary 1; otherwise, 0. The resulting 8-bit binary string is then converted to a decimal value, which replaces the center pixel in the output image. This process encodes the local texture around each pixel.

## Requirements
## Usage

### Built-in LBP

```python
from skimage.feature import local_binary_pattern

P = 8      # Number of neighbors
R = 1      # Radius
METHOD = 'uniform'

lbp_image = local_binary_pattern(gray_image, P, R, METHOD)


