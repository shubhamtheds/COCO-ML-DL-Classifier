# Multi-Class Image Classification using COCO Dataset
This project provides a multi-class image classification model using the COCO dataset 2017. The dataset contains images with object annotations for 80 different classes. Initially, classical machine learning algorithms were attempted, but then the Keras API was used to build a convolutional neural network (CNN) to improve accuracy. After optimization, the project achieved an accuracy of up to 82%.

## Installation
Before using this project, fork this repository from GitHub into your Google Colab account. It is also recommended to set the GPU as the default runtime environment as it is required for training our model using the CNN architecture.

Additionally, ensure that all the required libraries and packages are installed. These are listed in the requirements.txt file. Before starting the project, please install all the packages mentioned in the file using the following command:
!pip install -r requirements.txt

## Usage
To use this project, you first need to run the CocoDatasetDownloader class to download and process the dataset. If you already have the dataset, you can skip this step and directly move to the ImageClassifier class.

Next, use the ImageClassifier class via classical machine learning approaches to check the metrics achieved by our model. The final prediction was made using the random forest classifier, but you are free to try out other algorithms as well if required.

Finally, use the ImageClassifier class via CNN architectures to see the improvement in the model's performance. This class uses a highly optimized CNN architecture, which was tested on multiple parameters. It is recommended not to make changes to this class unless you are sure of what you are doing. However, your contributions to other parts of the project are most welcome. If you find any issues, feel free to mention them to me.

### CocoDatasetDownloader Class
The CocoDatasetDownloader class is used to download and process images from the Common Objects in Context (COCO) dataset. It has the following methods:

* download_annotations: downloads the annotations file from the COCO dataset.
* download_images: downloads images from the COCO dataset that match the specified categories.
* process_images: processes the downloaded images by resizing them and saving them to disk.

### ImageClassifier Class via Classical Approaches
The ImageClassifier class is used to classify individual images using classical machine learning approaches. It has the following methods:

* load_image: loads an image from disk.
* preprocess_image: preprocesses an image for classification.
* classify_image: classifies an image using a pre-trained model.

### Image Classifier Class via CNN Architectures
The ImageClassifier class is used to classify objects in a dataset using CNN architectures. It has the following methods:

* load_and_preprocess_data: loads and preprocesses the data from the dataset folder.
* create_model: creates the CNN model architecture using Keras.
* train_and_evaluate: trains and evaluates the model using the preprocessed data.
* plot_classification_report: plots the classification report using seaborn.

## Contributing
If you want to contribute to this project, you can follow these guidelines:

- Fork the project on GitHub.
- Clone the forked project to your local machine.
- Create a new branch for your changes.
- Make your changes and commit them to the new branch.
- Push the branch to GitHub and create a pull request.
- Follow the project's coding standards and file organization.
- Submit bug reports or feature requests using GitHub issues.

## License
This project is licensed under the MIT License. You can use the code for any purpose, modify it, and distribute it as long as you include the original license in your distribution.

## Acknowledgments
We would like to thank the authors of the COCO dataset used in this project for providing a comprehensive collection of object images. We would also like to thank the Keras and scikit-learn development teams for their excellent libraries.
