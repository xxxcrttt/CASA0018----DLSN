# CASA0018----DLSN-
This contains the workshop and coursework for CASA0018 -- Deep Learning for Sensor Network

## Coursework -- [Hearing the mask ](https://github.com/xxxcrttt/CASA0018----DLSN/tree/main/coursework)

Edge Impulse link: [mask3](https://studio.edgeimpulse.com/studio/88274)

### Research Question 
Most mask recognition detection systems use cameras - computer vision offers a wide range of facial detection algorithms and techniques.   
OpenCV uses the Haar-based cascade classifier, Deep learning image training uses CNNs.  

However, when using cameras for training I found them to be expensive and have defectives such as being difficult to deploy and the training process being time consuming. Instead I use a microphone on the Arduino Nano 33 BLE sense, to test whether a mask can be distinguished by human speech.

### Dataset 
![dataset](https://github.com/xxxcrttt/CASA0018----DLSN/blob/main/coursework/image/%E6%88%AA%E5%B1%8F2022-03-22%20%E4%B8%8A%E5%8D%8811.02.42.png)

### Deep Learning Procedure 
#### Processing – MFCC
Mel-Frequency Cepstral Coefficients,  is a function widely used for automatic speech recognition, where the speech signal is pre-reinforced, and Fourier transformed through a high-pass filter to transform the signal into the frequency domain. Typically, 12 coefficients are used, which are superimposed on the frame energy to give a 13-dimensional coefficient.
#### Learning -- Classification 
A classification algorithm is used to predict the category label for a given example in the input data.

![MFCC](https://github.com/xxxcrttt/CASA0018----DLSN/blob/main/coursework/image/%E6%88%AA%E5%B1%8F2022-03-22%20%E4%B8%8B%E5%8D%882.41.02.png)

### Training and Testing
After several experiments, a 1D CNN was chosen, creating a convolutional kernel to generate the output tensor by convolving the layer inputs in a single spatial (or temporal) dimension.

![training](https://github.com/xxxcrttt/CASA0018----DLSN/blob/main/coursework/image/%E6%88%AA%E5%B1%8F2022-03-22%20%E4%B8%8B%E5%8D%882.48.15.png)
![testing](https://github.com/xxxcrttt/CASA0018----DLSN/blob/main/coursework/image/%E6%88%AA%E5%B1%8F2022-03-22%20%E4%B8%8B%E5%8D%883.10.15.png)



