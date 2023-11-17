# About Semantic Segmentation 

- My assignment DL for competition: https://www.kaggle.com/competitions/bkai-igh-neopolyp  
- Run my solution: 

1. Input Data 
2. Download my pretrain_model:
- I use Unet++ with Resnet101 which has been pre-trained on the pytorch semantic segmentation library, then trained on the competition data set.
- You can download at my Drive link: 
...
3. Run my solution at Kaggle:




B1: clone my repo
```python
!git clone https://github.com/DoanNgocCuongBKEGNH/submit_Hw3DL_DNC210141 # link to my repo
```

B2: Thêm my pretrain model vào /kaggle/working/submit_Hw3DL_DNC210141
Bạn ấn vào `Add data` ở thanh bên phải và search URL link sau: https://www.kaggle.com/datasets/cngonngc/submit-model-pth để `add data`. Hoặc dùng code bên dưới

```python
# Load my pretrain model on Polyp Dataset
!kaggle datasets download -d /cngonngc/submit-model-pth --unzip
```

B3: Di chuyển/Copy submit_model.pth vào /kaggle/working/submit_Hw3DL_DNC210141 và đổi tên thành model.pth

```python
!cp /kaggle/input/submit-model-pth/submit_model.pth /kaggle/working/submit_Hw3DL_DNC210141/model.pth
```

B4: Di chuyển vào thư mục submit_Hw3DL_DNC210141

```python
%cd /kaggle/working/submit_Hw3DL_DNC210141
```

B5: Cài thư viện

```python
!pip install -r requirements.txt
```

B5: Run my solution

```python
!python infer.py  # args run
```

