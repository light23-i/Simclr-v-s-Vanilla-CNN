# Simclr-v/s-Vanilla-CNN
This repo will try to compare compare results of two different deep learning models for CIFAR10 Dataset. Both neural networks were trained for 10 epochs, and the accuracy on the validation data is mentioned below for both the models.

It is clear that for small amount of training, simclr outperforms Vanilla CNN.
# SIMCLR:
   SimCLR mainly works on the principle of self supervised learning, i.e. the model will try to first learn from the unlabelled data. The trained model, which will have ability to recognise different types of data will then be finetuned for the task required.
   In this case, a resnet-18 is used as the base model, which will learn the representation from the CIFAR-10 data. Further the trained resnet is finetuned for the image classification task on cifar 10.
   
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/1477c5f5-ad7a-4b99-977a-01a3fc7c3e6b)

To reproduce the results for SIMCLR, follow these steps:

```
pip install -r requirements.txt

python learnrepresentations.py -n num_epochs -p pathtotrainedresnet
python trainclassifier.py -n num_epochs -p pathtotrainedresnet
```
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/69f01e05-8538-4804-992f-9e93795a3287)
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/c24e60f7-46a9-4dbe-8f0a-0591942e3c68)
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/6f8337f2-7135-4b62-a11e-ef31915a9fef)

![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/3bcea814-ef7b-4ef0-87a9-1301822d46f1)
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/61c35761-796c-4a41-a67a-6b513e499dae)
![image](https://github.com/light23-i/Simclr-v-s-Vanilla-CNN/assets/74209656/add280a8-687a-480e-a09a-c124958606c2)

The above images, are the images formed after applying random transformations on the input image


# Vanilla CNN:

To train vanilla cnn, follow these steps:

```
pip install -r requirements.txt
python traincnn.py -n num_epochs
```
