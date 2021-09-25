# Implementing CNN(Convolutional Neural Network) using TENSORFLOW on TFDS(TensorFlow DataSet).
<p align="center">
  <img src = "https://user-images.githubusercontent.com/67642750/134743252-82bc7a7c-b274-46fa-b52a-c86254638ca8.png" width="400" height="350" align="centre">
</p>

## Project: _Rock_Paper_Scissor_
------

:information_source: Dataset: https://www.tensorflow.org/datasets/catalog/rock_paper_scissors

:heavy_exclamation_mark: _Important Libraries and Modules:_ Numpy, Pandas, Tensorflow and Tensorflow Dataset

:dart: _Primary Goal:_ Classifying the images(Rock, Paper, Scissor) using CNN.

:bulb: _Approaches:_ Rather than taking input in form of dictionary i.e {inpuy: "input", label: "label"}, by using **"as_supervised = True"** now will have 2-tuple structure i.e. (input, label). Then created 16 batches for both training as well as testing. The main task starts here! 
1. Created INPUT LAYER of 300x300 for <br> tf.keras.layers.InputLayer(input_shape=(300,300,3)
2. Created CONVOLUTIONARY LAYERS <br> This layer has _Convo2D_ with parameters such as **number of filters**, **size of kernel** and **activation_function** <br> Following the Convo2D layer _MaxPool2D_ is created with parameters such as **pool_size** and **strides**
3. Used DROPOUT<br> Model was outfitting at early stage of training so used dropout of **08** which helped to reduce some overfitting issues.
4. FLATTEN the layers<br> Layer flattened to **1024** with 5 convolutionary layers.
5. Created DENSE LAYERS<br>Units in dense layer needed to change accordingly to the flatten layer. **4** dense layers were created by gradually decreasing the number of units and keeping same **RELU** as same activation function. Also used activation as **SOFTMAX** in last dense layer which helps to get probability rather than getting value of vector.

:chart_with_upwards_trend: _Result:_ Was able to achive the *TRAINING ACCURACY* of **99.40%** and *TESTING ACCURACY* of **97.58%**

Technologies: <img src = "https://user-images.githubusercontent.com/67642750/134745049-58537d7a-4803-483a-8666-394e35931e0e.png" width="30" height="30">
<img src = "https://user-images.githubusercontent.com/67642750/134744907-ca78d295-716d-41fe-a676-f409b10ac4f4.png" width="30" height="30">

