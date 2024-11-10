# Bee Species Identification using Machine Learning
---
- This project focuses on developing a machine learning model to classify bee species as either honey bee (Apis) or bumble bee (Bombus) based on images. By leveraging image processing techniques and machine learning algorithms, this model helps identify bee species from various backgrounds, positions, and image resolutions, which can aid researchers in monitoring and understanding bee populations essential for ecological and agricultural systems.

## Features
- Image Preprocessing: Converts images from RGB to grayscale to simplify data for machine learning models.
- Histogram of Oriented Gradients (HOG): Extracts features from the images to highlight edges and shapes, enabling the model to better understand the bee's physical characteristics.
- Machine Learning Classification: Uses various models such as Support Vector Machine (SVM) to predict whether a bee is a honey bee or a bumble bee.

## Requirements
- Python 3.x
- Libraries:
    os
    matplotlib
    pandas
    numpy
    PIL (Pillow)
    scikit-image
    scikit-learn
  
## Installation
You can install the required libraries using pip:
`pip install matplotlib pandas numpy pillow scikit-image scikit-learn`

### Usage - Load and Process Data:

- Loads images of honey bees and bumble bees from a dataset.
- Converts images to grayscale using the rgb2grey function from scikit-image.

## Feature Extraction:

- Extracts HOG features from the grayscale images to help the model identify important patterns.
Model Training and Evaluation:
- The model uses these features to train a classifier, like Support Vector Machine (SVM), for predicting bee species.
```
# Load a sample image of a honey bee
apis_row = labels[labels.genus == 0.0].index[5]
plt.imshow(get_image(apis_row))
plt.show()

# Load a sample image of a bumble bee
bombus_row = labels[labels.genus == 1.0].index[5]
plt.imshow(get_image(bombus_row))
plt.show()

# Convert the image to grayscale
bombus_image = get_image(bombus_row)
grey_bombus = rgb2grey(bombus_image)
plt.imshow(grey_bombus, cmap='gray')
plt.show()
```
