# Simple Liveness Classifier with Deep Learning
This project presents a deep learning-based liveness detection system that combines a Visual Model (e.g., ResNet50, MobileNetV2, or ViT) with a Texture Model (Deep Texture Encoding Network - Deep TEN).
## Files list
|     File name     |    Function    |
| :---------------: | :--------: |
| 0.5_ViT_liveness-classifier.ipynb    |  Contains the training and evaluation code    (Example with ViT and alpha = 0.5)|
| LeTienQuyet_Section1.pdf    | The rationale for my design choices, including model selection, training strategy   |
| requirements.txt   |  file lists all the Python libraries and their versions required to run the project   |
## About code & enviroment
The Deep TEN model is implemented via the PyTorch-Encoding library, which includes a set of CUDA and C++ extensions. However, when used with newer versions of PyTorch (≥ 2.1), you may encounter errors due to the use of tensor.data\<T\>(), which has been deprecated.
To resolve this, you’ll need to modify a few lines in the source code before rebuilding the library. [See the first code cell in **0.5_ViT_liveness-classifier.ipynb** for a step-by-step fix — setup takes about 5 minutes].
To avoid compatibility issues and save enviroment setup time, I recommend running the code on platforms like Kaggle, where the environment is already configured and easy to use.