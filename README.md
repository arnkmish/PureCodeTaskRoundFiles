# PureCode Task Round Files

**Approach:** CNN-LSTM Based Image Captioning Model Trained for 100 Epochs with No Validation

- Train-Test Split: Randomly split into 90% training data and 10% testing data resulting in 270 samples for training and 30 samples for testing for each dataset.

- Model Architecture: A CNN-LSTM based image captioning model is used with ResNet50 based Encoder CNN and LSTM based Decoder RNN. The ResNet50 architecture is mostly frozen(with ImageNet-1k weights) except for the FC layer weights and biases. This is done because the number of samples that we have is quite less and the pretrained model will be able to extract decent complex visual features. The FC layers and the complete Decoder RNN is trained for 100 epochs in order to arrive at the trained model.

- Implementation Environment: The entire implementation is done in the freely available GPU based environment of Google Colab. The package details: PyTorch(2.0.0+cu118), Torchvision(0.15.1+cu118), Pillow(8.4.0), Scikit-Learn(1.2.2), Pandas(1.4.4), Numpy(1.22.4), Spacy(3.5.1).

- Training: Since the all the code is submitted as iPython Notebook files, the model training is performed using the train() function present in the Notebook files for each of the dataset. For all the three datasets, separate Notebooks have been created as mentioned below:

Dataset 1: PRCD_Dataset1.ipynb

Dataset 2: PRCD_Dataset2.ipynb

Dataset 3: PRCD_Dataset3.ipynb

- Testing: The testing and visualization can be performed using the code block identified with the comment "Visualize INFERENCE Results". Using this block of code both the correct and predicted captions can be observed along with the input image for all samples present in the test set. Further evaluation of performance can be performed using the subsequent blocks identified with the section "EVALUATE PREDICTIONS VIA ROUGE SCORES", where ROUGE-1,2, and L metrics are considered to observe the Precision, Recall and F1-Score on the test set.

- The following are the test set results on all the three datasets in terms of ROUGE-1, 2, and L metrics:

![ROUGE-1 Evaluation Results](https://user-images.githubusercontent.com/8967554/230759477-e747d0fb-0eb4-45c6-a3d7-0495e8de572e.png)
![ROUGE-2 Evaluation Results](https://user-images.githubusercontent.com/8967554/230759526-5e1697dc-0aeb-4f18-8035-5cd034ffe79c.png)
![ROUGE-L Evaluation Results](https://user-images.githubusercontent.com/8967554/230759551-0c23a8c5-6de5-4418-a2be-5314fb3e5787.png)

Trained model checkpoints are available for download at: https://drive.google.com/drive/folders/1MHM6iHPajY5jKQyYwlWuMxzvBoJ-8nij?usp=sharing
