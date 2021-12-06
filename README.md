# shadow_removal

Pytorch implementation for manuscript "Towards Real-world Shadow Removal with a Shadow Simulation Method and a Two-stage Framework".

**Testing**

1. Download the models and save them into ./checkpoints/shadow_removal/. Or train the model yourself.

2. Make the files which contain the paths of shadow images and masks and name them as img.flist and mask.flist. Flist can be made by the file in /home/notebook/data/group/gaojianhao/CVPR2022/mask_list.py.

3. run the command:

```python test.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```

**Training with simulated shadow images** 
path:/home/notebook/data/group/gaojianhao/CVPR2022/shadow_removal_simudata

1. Make the files which contain the paths of images and masks and name them as img.flist and mask.flist.

2. run the command

```python train.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```

**Training with real shadow images**

path:/home/notebook/data/group/gaojianhao/CVPR2022/supervised_training

1. Make the files which contain the paths of shadow images and masks and name them as img.flist and mask.flist.

2. run the command

```python train.py --name shadow_removal --img_flist img.flist --mask_flist mask.flist```


