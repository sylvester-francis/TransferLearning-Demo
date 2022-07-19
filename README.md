# TransferLearning-Demo
A demo for Transfer-learning using CNN and TensorFlow Object Detection API </br>


## References 
https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/training.html#install-labelimg  </br>

## STEPS TO USE THIS DEMO </br>
## Prerequisites </br>
- Python 3.7 + </br>
- LabelImg - Data preparation tool  </br>

-- Folder structure <br>
---assets/ </br>
    -----inference_graphs </br>
    -------frozen_inference_graph.pb </br>
    ---data/ </br>
    -----images/ </br>
    -----annotations/ </br>
    -----test_images/ </br>
    ---object_detection/ </br>
    ---export_inference_graph.py </br>
    ---generate_tfrecord.py </br>
    ---resize_images.py </br>
    ---train.py </br>
    ---xml_to_csv.py </br>

## Data Preparation and pre-requisites - Images

Step 1 : Install LabelImg by using the command  pip install labelImg </br>
Step 2 : Run LabelImg by using the command python -m labelImg  </br>
Refer https://github.com/heartexlabs/labelImg#usage if you require further information about labelImg </br>
Refer to https://www.youtube.com/watch?v=K_mFnvzyLvc&t=553s to learn more about using label img </br>

![alt text](https://raw.githubusercontent.com/sylvester-francis/TransferLearning-Demo/main/Readmeimg1.jpg) </br>

Step 3: Annotate the images and label all the images required for training </br>
Step 4: After the annotation is completed you will have a set of .xml files present in the training folder (this xml file contains the pixel locations of your bounding box and the class label) </br>

![alt text](https://raw.githubusercontent.com/sylvester-francis/TransferLearning-Demo/main/Readmeimg2.jpg) </br>

The above image contains the contents of a single xml file for a particular test image </br>

Step 5: Create a labelmap.pbtxt file and place it in the annotations folder which is present in data folder </br>
        The labelmap.pbtxt is a json file in the below provided format (This file is required by tensorflow for classification)
![alt text](https://raw.githubusercontent.com/sylvester-francis/TransferLearning-Demo/main/Readmeimg3.jpg) </br>

Step 6: Download a pre-trained model to apply transfer learning
--Download any pre-trained model of your choice from the TensorFlow 2 Detection Model Zoo. </br>
 https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md </br>

Step 7: Once the initial data preparation is completed - create the folder structure and upload the following files to github following the same folder structure </br>
    ---assets/ </br>
    -----inference_graphs </br>
    -------frozen_inference_graph.pb (The downloaded model) </br>
    ---data/ </br>
    -----images/ </br>
    -----annotations/ </br>
    -----test_images/ </br>
    ---object_detection/ </br>
    ---export_inference_graph.py </br>
    ---generate_tfrecord.py </br>
    ---resize_images.py </br>
    ---train.py </br>
    ---xml_to_csv.py </br>

## Training and testing the model in google colab
Step 1: Navigate to https://colab.research.google.com/?utm_source=scs-index  </br>
Step 2: Open the code present in "Tyre_classifier-colab.ipynb" and run it in google colab </br>
 PS: change the repo url to the url of your git repository </br>
Step 3: Congratulations you built your first image classifier using Tensorflow object detection api and google colab </br>
     

## References 
https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/training.html
https://medium.com/swlh/tensorflow-2-object-detection-api-with-google-colab-b2af171e81cc






