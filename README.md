# Project Title: Tooth_segmentation using Generative U-Net Model
## Problem Statement
Dental segmentation presents a significant challenge for many dentists, especially when it comes to analyzing adult teeth in panoramic images. A common issue is identifying the extent and roots of teeth, which is crucial in various dental procedures like implants and extractions. Dentists often find these cases complex.

This research suggests employing generative neural models to delve deeper into the teeth fragmentation process.
## Dataset
World’s first dataset of children’s dental panoramic radiographs for caries segmentation and dental disease detection by segmenting and detecting annotations is published in this dataset.

There are three folders: i) adult tooth segmentation (semantic segmentation), ii) children's dental caries segmentation (instance segmentation), and iii) pediatric dental disease detection (object detection).

Data can be seen at the following link.
* https://www.kaggle.com/datasets/truthisneverlinear/childrens-dental-panoramic-radiographs-dataset/data

## Methodology
The U-Net architecture improved by was chosen for this project due to its success in image segmentation tasks.

## Deployment
The model was deployed using Flask and TensorFlow Serving. Flask was used to create a web service, while TensorFlow Serving was used to serve the model as a API.

## Files
* `Pipfile` and `Pipfile.lock` : library requirement for deployment
* `u-net-lung-segmentation.ipynb` : Notebook file contains EDA and Modeling, originally from kaggle [notebook](https://www.kaggle.com/code/mohammademadsharifi/tooth-segmentation)
* `save-test-model.ipynb` : Notebook file to save and test TensorFlow Serving
* `gateway.py` : python script for serving ML models using Flask
* `proto.py` : python script for convert np tp protobuf
* `test.py` : python script to send a request to the API
* `image-gateway.dockerfile` : Docker file build service container
* `image-model.dockerfile` : Docker file to build model server container
* `docker-compose.yaml` : to run service and model server container

## How to Run

