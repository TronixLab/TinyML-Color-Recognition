# TinyML-Color-Recognition
Embedded Machine Learning (TinyML) on Arduino Nano 33 BLE Sense. 

This project is based on [fruit identification using Arduino and TensorFlow](https://blog.arduino.cc/2019/11/07/fruit-identification-using-arduino-and-tensorflow/).

Just do the followinng steps:
1. **Create your own data sets**
   -  Use *ObjectColor_Capture.ino* Arduino sketch to gather the object color data and display it in serial monitor.
   -  Copy the data in serial monitor in text file then save it as csv file format.
   -  You can make color datasets as many as you can. For this repo, it can detect RGB colors based on colred paper.

2. **TinyML with TensorFlow Lite on Arduino**
   -  Open your google [colab](https://colab.research.google.com/), then use the file *TFlite_color.ipynb*.
   -  Upload your color object datasets in google colab folder section.
   -  Run each cells (set of program) from the top to bottom, it will train your TensorFlow model and create a file *color_model.h*.
   -  Download the *color_model.h* file, and you will use it for arduino sketch.

3. **Deploy your ML model on microcontroller**
   -  Copy the *color_model.h* file, and replace the existing *color_model.h* file in *ObjectColor_Classifier* folder.
   -  Upload the sketch on your Arduino Nano 33 BLE Sense.
   -  Enjoy your embedded machine learning on Arduino. It run on real-time processing!
