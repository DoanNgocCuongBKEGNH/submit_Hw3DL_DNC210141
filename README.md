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
!git clone https://github.com/  # link to my repo
```
```python
!cp /kaggle/working/model.pth /kaggle/working/unet-semantic-segmentation/
```

```python
!pip -r requirements.txt
```

```python
!python /kaggle/working/unet-semantic-segmentation/infer.py  # args run
```

