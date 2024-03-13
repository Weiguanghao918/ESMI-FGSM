# ESMI-FGSM

This repository contains code to reproduce results from the paper:

Adversarial Attack Method Based on Enhanced Spatial Momentum

Jun Hu, [Guanghao Wei](https://github.com/Weiguanghao918)

## Requirements
+ GPU: NVIDIA A40 RTX3090 RTX A4000
+ Operating System: Ubuntu 20.04
+ Python >= 3.6.5
+ Tensorflow >= 1.12.0
+ Numpy >= 1.15.4
+ opencv >= 3.4.2
+ scipy > 1.1.0
+ pandas >= 1.0.1
+ imageio >= 2.6.1

## Qucik Start

### Prepare the data and models

You should download the [data](https://drive.google.com/drive/folders/1CfobY6i8BfqfWPHL31FKFDipNjqWwAhS) and [pretrained models](https://drive.google.com/drive/folders/10cFNVEhLpCatwECA6SPB-2g0q5zZyfaw) and place the data and pretrained models in dev_data/ and models/, respectively.

### Variance Tuning Attack

All the provided codes generate adversarial examples on inception_v3 model. If you want to attack other models, replace the model in `graph` and `batch_grad` function and load such models in `main` function.

#### Runing attack

Taking ESMI-FGSM attack for example, you can run this attack as following:

```
CUDA_VISIBLE_DEVICES=gpuid python ESMI-FGSM.py 
```

The generated adversarial examples would be stored in directory `./outputs`. Then run the file `simple_eval.py` to evaluate the success rate of each model used in the paper:

```
CUDA_VISIBLE_DEVICES=gpuid python simple_eval.py
```

## Acknowledgments

Code refers to [VMI-FGSM](https://github.com/JHL-HUST/VT).

## Contact

Questions and suggestions can be sent to guanghwei@163.com.
