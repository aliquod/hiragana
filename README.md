# Handwritten Hiragana Classifier
## About the project

This project is a Convolutional Neural Network (CNN) model that classifies handwritten hiragana characters (part of the Japanese alphabet), based on the ETL7 dataset. One can provide a directory to an image, and then a wrapper function would load the image and use the model to classify it as one of the hiraganas.

### Details
The model takes an image that satisfies:
* has a character written on a black background with a white ink
* has unvoiced characters only (i.e. without dakuten or handakuten)
*  *has a (64,64) shape,  with no color channels*
* *contains values in the interval (0,1), representing brightness with 1 being a white pixel*

The wrapper function preprocesses images, hence the last two requirements are unnecessary (as long as the image is square).

Frameworks: Tensorflow, Keras, PIL, Matplotlib

## About the repository
* `kana.ipynb`: the jupyter notebook used to build the model
* `classifikanation`: the model with accuracy of ~98% (in form of a folder), can be loaded with `keras.model.load(classifikanation)`
* `hatest.jpg`: the test image used in the notebook, which is not included in the sample and comes in a different size than the ones used to train the model (still a square image, though)

## Credits
* Data Source
	* [the ETL Character Database](http://etlcdb.db.aist.go.jp/): the homepage of the entire database
	* [the ETL7 Dataset](http://etlcdb.db.aist.go.jp/specification-of-etl7): the dataset of handwritten hiragana used for this project
	* [Explanation of the file format](http://etlcdb.db.aist.go.jp/etlcdb/etln/form_m.htm): how the samples are organized in the dataset
	* [Download request page](http://etlcdb.db.aist.go.jp/download-request): the data is available after a brief request (5-min max)
* Some code are adapted from Francois Chollet's book *Deep Learning with Python (2018)*, and they are indicated in the notebook
