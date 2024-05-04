# Sign-Language-Gesture-Recognition-
Developed a cutting-edge real-time sign language recognition and translation system leveraging Python, TensorFlow, Keras, and OpenCV. This innovative solution serves as a bridge between the hearing-impaired and the hearing population by seamlessly translating sign language into spoken language and vice versa. Through the application of advanced deep learning techniques, the system facilitates fluid communication, effectively breaking down barriers and fostering inclusivity in diverse environments.

## Overview of My Work

1. Gesture Sample Creation: Initially, I generated 44 gesture samples employing OpenCV. Each gesture comprised 1200 grayscale images sized 50x50 pixels, all stored within the "gestures/" directory. Furthermore, to enhance the dataset, I utilized a script called flip_images.py to horizontally flip each image, resulting in a total of 2400 images per gesture.

2. Understanding Convolutional Neural Networks (CNNs): Subsequently, I delved into comprehending CNNs and their functionality. My primary learning resources included the official website of TensorFlow and machinelearningmastery.com.

3. **CNN Model Development: I proceeded to develop a CNN model utilizing both TensorFlow and Keras, drawing inspiration from the architecture of the MNIST classifying model available on TensorFlow's tutorials. It's worth noting that for incorporating additional gestures, one may need to customize the network architecture by adding layers and adjusting parameters accordingly.

4. Model Implementation: Once the model was trained using Keras, I integrated it with a video stream to facilitate real-time gesture recognition.

5. Current Status: At present, I have assembled a dataset consisting of 44 gestures, encompassing the 26 alphabets, 10 numbers from American Sign Language, and several additional gestures. The model has been trained on this dataset, paving the way for efficient gesture recognition.


## How to Utilize This Repository

Before delving into the usage instructions, it's essential to note that this repository lacks an interactive interface to guide users through its functionalities. Hence, users must navigate and make necessary script adjustments independently. Here's a basic overview:

### Creating a Gesture
0. Setting the hand histogram 
1. Set your hand histogram, a crucial step for optimal gesture recognition. Execute the following command and adhere to the subsequent instructions:

    
    python set_hand_hist.py
    

   - Follow on-screen instructions to position your hand within the designated squares.
   - Ensure all squares are covered by your hand and press 'c' to capture the histogram.
   - Repeat until you achieve a satisfactory histogram, then press 's' to save and exit.

2. Optionally, create or replace gestures. Execute:

   
    python create_gestures.py
   

   - Follow prompts to specify gesture number and name/text.
   - A window titled "Capturing gestures" will appear, showcasing a green box for gesture creation.
   - Press 'c' to initiate capturing. Move your hand within the box until completion.
   - Images will be saved to augment the dataset.

3. Flip images for enhanced dataset variety:
   
    python flip_images.py
    

4. Once gestures are finalized, execute `load_images.py` to load them:

    
    python load_images.py
    `

### Displaying All Gestures
Execute the following command to view all stored gestures:

python display_all_gestures.py


### Model Training
Choose between TensorFlow or Keras for model training:
- TensorFlow: Execute `cnn_tf.py`.
- Keras: Execute `cnn_keras.py`.

  
    python cnn_tf.py
    python cnn_keras.py
  

### Get Model Reports
Generate classification reports using the trained model:

python get_model_reports.py


### Testing Gestures
Test gesture recognition with the following command:

python recognize_gesture.py

### Using fun_util.py
Explore various functionalities in text or calculator mode:
- Text Mode: Press 't'.
- Calculator Mode: Press 'c'.

Ensure proper hand histogram setup before transitioning to these modes. Good Luck for your Project
