# MNSIT Digit Recognition Model

This project covers basics of Deep Learning Concepts such as FCNN, RNN, CNN, etc .

To analyze which model is better, we need to consider various aspects such as loss, accuracy, precision, and recall. Here is a detailed analysis of each model used in the project:

### 1. Fully Connected Neural Network (FCNN)
- **Loss:** 0.0990
- **Accuracy:** 0.9739

**Analysis:**
- The FCNN shows a good performance with a high accuracy of 97.39%. 
- However, it does not incorporate spatial information effectively since it's a fully connected network, which can limit its performance on image data like MNIST.

### 2. Recurrent Neural Network (RNN)
- **Loss:** 0.1294
- **Accuracy:** 0.9640
- **Precision:** 0.9695
- **Recall:** 0.9599

**Analysis:**
- RNNs are generally better suited for sequential data rather than image data.
- The accuracy is slightly lower at 96.40%, with precision and recall close to each other indicating a balanced performance but slightly lower compared to the FCNN.
- The loss is higher compared to the FCNN.

### 3. RNN with Early Stopping
- **Loss:** 0.1140
- **Accuracy:** 0.9675
- **Precision:** 0.9740
- **Recall:** 0.9625

**Analysis:**
- Early stopping helps prevent overfitting, resulting in a slightly better performance compared to the plain RNN.
- The accuracy, precision, and recall are improved compared to the plain RNN, making it a better option than the basic RNN but still not as good as CNN-based models for this task.

### 4. Convolutional Neural Network (CNN) (Encoder Architecture, Batch Normalization, Early Stopping)
- **Loss:** 0.0435
- **Accuracy:** 0.9903
- **Precision:** 0.9915
- **Recall:** 0.9900

**Analysis:**
- CNNs are particularly well-suited for image data due to their ability to capture spatial hierarchies.
- This model shows a significant improvement with an accuracy of 99.03% and very high precision and recall.
- The loss is much lower, indicating a better fit to the data.

### 5. Encoder-Decoder Architecture (CNN, Early Stopping, Batch Normalization, Pooling, Dropout)
- **Loss:** 0.0185
- **Accuracy:** 0.9946
- **Precision:** 0.9947
- **Recall:** 0.9943

**Analysis:**
- This model achieves the best performance among all the models.
- The loss is the lowest, and the accuracy is the highest at 99.46%.
- Precision and recall are also the highest, indicating an excellent balance and superior performance.
- The encoder-decoder architecture, combined with batch normalization, pooling, and dropout, provides robust regularization and effective feature extraction.

### Conclusion
The Encoder-Decoder Architecture with CNN, Early Stopping, Batch Normalization, Pooling, and Dropout outperforms all other models in this comparison. It achieves the highest accuracy, precision, and recall with the lowest loss, making it the best model for MNIST digit recognition in this analysis.


### In this Project

**MNIST Digit Recognition Model**  
Tech Stack: Python, TensorFlow, OpenCV, NumPy
- Developed and compared various deep learning models to classify digits from the MNIST dataset.
- Evaluated five different architectures and incorporated techniques like batch normalization, dropout, pooling, and early stopping.
- Achieved 99.46% accuracy by integrating Encoder-Decoder Architechture, CNN, early stopping, batch normalization, pooling, and dropout, outperforming traditional FCNN and RNN models
