# About Semantic Segmentation 

- My assignment DL for competition: https://www.kaggle.com/competitions/bkai-igh-neopolyp  
- Run my solution: 

1. Input Data 
2. Download my pretrain_model:
- I use Unet++ with Resnet101 which has been pre-trained on the pytorch semantic segmentation library, then trained on the competition data set.
- You can download at my Drive link: 
...
3. Run my solution at Kaggle:

```python
# Load my pretrain model on Polyp Dataset
!kaggle datasets download -d /cngonngc/submit-model-pth --unzip
```

```python
https://github.com/DoanNgocCuongBKEGNH/submit_Hw3DL_DNC210141 # link to my repo
```
```python
!cp /kaggle/working/model.pth /kaggle/working/submit_Hw3DL_DNC210141/
```

```python
!pip -r requirements.txt
```

```python
!python infer.py  # args run
```

