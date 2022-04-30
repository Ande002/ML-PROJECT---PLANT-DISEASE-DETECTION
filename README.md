# ML-PROJECT---PLANT-DISEASE-DETECTION

Plant Disease Detection is one of the Biggest issue that exits when we talk about using Technology in Agriculture.
Although researches have been done to detect weather a plant is healthy or diseased using Deep Learning and with the help of Neural Network, new techniquies are still being discovered.

In this project CNN was used

ABOUT THE DATASET

The dataset used for this project has been taken from Plant-Village- Dataset found at Kaggle


PROPERTIES OF IMAGES

Type of File : JPG File.

Dimensions : 256 * 256.

Width : 256 Pixels.

Height : 256 Pixels.

Horizontal Resolution : 96 dpi.

Vertical Resolution : 96 dpi.

Bit Depth : 24.

STEPS INVOLVED

Data Preprocessing

1 ) Load Original Image. A total of 800 images for each class Diseased and Healthy is fed for the machine.

    Conversion of image from RGB to BGR. Since Open CV (python library for Image Processing), accepts images in RGB coloring format so it needs to be converted to the original format that is BGR format.

    Conversion of image from BGR to HSV. The simple answer is that unlike RGB, HSV separates luma, or the image intensity, from chroma or the color information. This is very useful in many applications. For example, if you want to do histogram equalization of a color image, you probably want to do that only on the intensity component, and leave the color components alone. Otherwise you will get very strange colors.

    Image Segmentation for extraction of Colors. In order to separate the picture of leaf from the background segmentation has to be performed, The color of the leaf is extracted from the image.

    Applying Global Feature Descriptor. Global features are extracted from the image using three feature descriptors namely :

    • Color : Color Channel Statistics (Mean, Standard Deviation) and Color Histogram

    • Shape : Hu Moments, Zernike Moments

    • Texture : Haralick Texture, Local Binary Patterns (LBP)

After extracting the feature of images the features are stacked together using numpy function “np.stack”.

According to the images situated in the folder the labels are encoded in numeric format for better understanding of the machine.

The Dataset is splitted into training and testing set with the ratio of 80/20 respectively.

    Feature Scaling Feature Scaling is a technique to standardize the independent features present in the data in a fixed range. It is performed during the data pre-processing to handle highly varying magnitudes or values or units. 
    

    Saving the Features. After features are extracted from the images they are saved in HDF5 file. The Hierarchical Data Format version 5 (HDF5), is an open source file format that supports large, complex, heterogeneous data. HDF5 uses a "file directory" like structure that allows you to organize data within the file in many different structured ways, as you might do with files on your computer.

    Modeling The Model is trained over CNN

9 ) Prediction The models with best performance is them trained with whole of the dataset and score for testing set is predicted using Predict function.
