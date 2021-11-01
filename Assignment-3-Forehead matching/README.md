# Forehead Image Matching
## Introduction
In this report, the results of forehead matching using image matching and feature extraction algorithms are shown. Bio-metric authentication using forehead becomes important due to the current pandemic because everyone has to wear a mask and hence, a system which authenticates using forehead wrinkles would be much more convenient. Moreover, the methods used in this report are inexpensive and do not require any complicated equipment to function.

## Dataset
Students of BITS Pilani, Pilani campus that were enrolled in the Deep Learning course gathered the data. Data was gathered over the course of two sessions, with a minimum of 12 hours between them. Each session resulted in ten photographs, five of which were taken up close and five of which were taken from a distance. The experiment employed 336 pictures from the total data gathered. There were three close-up photos and three far-off images for each of the 28 subjects in each session.

## Model Pipeline
### RoI Extraction
The extraction for the region of interest was done manually. The users had to align their forehead in a box while frowning such that their wrinkles are visible. The images were also taken from two poses, one far-off pose and one pose from near the camera. Finally there were 336 RGB RoI extracted images.

### Image Enhancement
CLAHE (Const Limited Adaptive Histogram Equalization) was used to convert the pictures to grayscale. The CLAHE method outperforms the conventional histogram equalization method. CLAHE is a version of adaptive histogram equalization (AHE) that corrects for contrast overamplification. CLAHE works by dividing the image into tiles, which are tiny areas of a picture rather than the full image. To remove the false borders, the nearby tiles are merged using bilinear interpolation. It was found that using CLAHE gave better results than the normal histogram equalization methods, and as a whole these preprocessing techniques gave a better result than using the default RGB images, as wrinkles seemed to be enhanced using these methods.

