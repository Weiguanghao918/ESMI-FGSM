# Evaulations setting for Table 2 and Table 3
+ MI-FGSM: Please refer to https://github.com/dongyp13/Non-Targeted-Adversarial-Attacks and https://github.com/dongyp13/Targeted-Adversarial-Attack
+ NI-FGSM: Please refer to https://github.com/JHL-HUST/SI-NI-FGSM
+ VMI-FGSM: Please refer to https://github.com/JHL-HUST/VT
+ AST-NI-FGSM and EM-RE-FGSM are self-completed code reproductions based on the formulae described in the related papers.


# Evaulations setting for Table 4

+ [HGD](https://github.com/lfz/Guided-Denoise), [R\&P](https://github.com/cihangxie/NIPS2017_adv_challenge_defense), [NIPS-r3](https://github.com/anlthms/nips-2017/tree/master/mmd): We directly run the code from the corresponding repo.
+ [Bit-Red](https://github.com/thu-ml/ares/blob/main/ares/defense/bit_depth_reduction.py): step_num=4, alpha=200, base_model=Inc_v3_ens.
+ [JPEG](https://github.com/thu-ml/ares/blob/main/ares/defense/jpeg_compression.py): No extra parameters.
+ [FD](https://github.com/zihaoliu123/Feature-Distillation-DNN-Oriented-JPEG-Compression-Against-Adversarial-Examples): resize to 304\*304 for FD and then resize back to 299\*299, base_model=Inc_v3_ens
+ [ComDefend](https://github.com/jiaxiaojunQAQ/Comdefend): resize to 224\*224 for ComDefend and then resize back to 299\*299, base_model=Resnet_101
+ [RS](https://github.com/locuslab/smoothing): noise=0.25, N=100, skip=100
+ [NRP](https://github.com/Muzammal-Naseer/NRP): purifier=NRP, dynamic=True, base_model=Inc_v3_ens

+ HGD: Please refer to https://github.com/lfz/Guided-Denoise
+ R\&P: Please refer to https://github.com/cihangxie/NIPS2017_adv_challenge_defense
+ NIPS-r3: Please refer to https://github.com/anlthms/nips-2017/tree/master/mmd
+ Bit-Red: We provide the code for [bit reduction](./bit_depth_reduction.py). You can process the input image by ``bit_depth_reduction`` before feeding them to the model Inc-v3_ens3. 
+ JPEG: We provide the code for [JPEG](./jpeg.py). You can process the input image by ``jpeg_compress`` before feeding them to the model Inc-v3_ens3. 
+ FD: We provide the code for [FD](./feature_distillation.py). You can process the input image by ``FD_jpeg_encode`` before feeding them to the model Inc-v3_ens3. 
+ ComDefend: Please refer to https://github.com/jiaxiaojunQAQ/Comdefend. You can first run the ``compression_imagenet.py`` to generate the processed images. Then you can run ``Resnet_imagenet.py`` to test the method. 
+ RS: Please refer to https://github.com/locuslab/smoothing. We run the code with the [script](RS.sh).
+ NRP: Please refer to https://github.com/Muzammal-Naseer/NRP. We run the code with the following script:
```
    python purify.py --dir adv_images --purifier NRP --dynamic
```






