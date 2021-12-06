# shadow_removal


**Results of model trained with simulated shadow images**

ISTD results: 

```/home/shadow_removal_simudata/ISTDresults/images```

Some SBU results:

```/home/shadow_removal_simudata/SBUresults```

**Results of model trained with real shadow images**

*ISTD results:*

```/home/supervised_training/ISTDresults/model2/test_latest```

*Some SBU results:*

```/home/supervised_training/SBUresults```


**Training with simulated shadow images** 

*Project path:*

```/home/shadow_removal_simudata```

*Path of pretrained network:*

```/home/shadow_removal_simudata/checkpoints/shadow_removal/iter_480000_net_G1.pth```

Process:

1. Make the files which contain the paths of images and masks and name them as img.flist and mask.flist.

2. run the command

```python train.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```

**Training with real shadow images**

*path:*
```/home/supervised_training```

Process:

1. Make the files which contain the paths of shadow images and masks and name them as img.flist and mask.flist.

2. run the command

```python train.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```

**Testing**

1. Download the models and save them into ./checkpoints/shadow_removal/. Or train the model yourself.

2. Make the files which contain the paths of shadow images and masks and name them as img.flist and mask.flist. Flist can be made by the file in ```/home/mask_list.py.```

3. run the command:

```python test.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```

**Evaluation**

The shadow removal results are evaluated with MAE(Mean Absolute Error). The matlab code is available in ```/home/matlab_eval/ISTDtest.m```



