# Crowd Counting in Images

A simple image processing project that automatically estimates the number of people in crowded images using OpenCV.

## What it does

This project takes a crowd image as input and outputs:
- The estimated number of people in the image
- A density map showing where people are concentrated
- A visual result with detected people marked

## Dataset

I used the **ShanghaiTech Part B** dataset from Kaggle.
- 482 labeled street-level crowd images
- Average of 123 people per image
- Link: https://www.kaggle.com/datasets/tthien/shanghaitech-with-people-density-map

## How it works

1. Load the image
2. Convert to grayscale
3. Apply Gaussian blur to reduce noise
4. Use Canny edge detection to find boundaries
5. Use blob detection to count people
6. Generate a density map
7. Evaluate accuracy with MAE and MSE

## Tools used

- Python 3
- OpenCV
- NumPy
- Matplotlib
- SciPy
- Google Colab

## Results

- Estimated count per image using SimpleBlobDetector
- Density map visualization (red = many people, blue = fewer)
- MAE and MSE calculated on 10 test images

## Limitations

- Blob detector sometimes misses people who are overlapping
- Accuracy depends on image quality and lighting
- Works on static images only, not real-time video

## Future work

- Try a CNN model for better accuracy
- Extend to real-time video
- Build a simple web interface

## Author

Rahimova Zuhra — ID: 230104
