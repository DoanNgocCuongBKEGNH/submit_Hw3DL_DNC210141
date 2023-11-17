# About Semantic Segmentation 

- My assignment DL for competition: https://www.kaggle.com/competitions/bkai-igh-neopolyp  
- Run my solution quickly: [Run on Kaggle]()   update sau.
    - Hoặc truy cập nhanh file `quickly_infer_kaggle.ipynb` và chạy all. 
    - Hoặc làm theo các hướng dẫn bên dưới: 

B1: Clone my repo
```python
!git clone https://github.com/DoanNgocCuongBKEGNH/submit_Hw3DL_DNC210141 # link to my repo
```

# B2: Load my best_model.pth from wandb

```python
# Load best_model.pth from Unet++152resnet(best_at82/200 epochs)

import wandb

wandb.login(key = "c8767797aae76cbcd389ff29929ace1ac3021161")    # key's DoanNgocCuong
run = wandb.init(project = "PolypSegment")

# run = wandb.init()     # Nhập API, cách được đề xuất: https://wandb.ai/doanngoccuong_nh/PolypSegment/artifacts/model/best_model/v1/usage
artifact = run.use_artifact('doanngoccuong_nh/PolypSegment/best_model:v1', type='model')
artifact_dir = artifact.download()

# Hoặc nếu có best model thì upload lên và copy vào /kaggle/working/best_model.pth  (di chuyển đổi tên)
# %cp /kaggle/input/best-mode-v2-pth/best_model_v2.pth /kaggle/working/best_model.pth
```

# B3: Di chuyển/Copy submit_model.pth vào /kaggle/working/submit_Hw3DL_DNC210141 và đổi tên thành model.pth
```python
!cp /kaggle/working/artifacts/best_model:v1/best_model.pth /kaggle/working/submit_Hw3DL_DNC210141/model.pth
```

# B4: Di chuyển vào thư mục (cd) submit_Hw3DL_DNC210141

```python
%cd /kaggle/working/submit_Hw3DL_DNC210141
```

# B5: Cài thư viện cần thiết

```python
!pip install -r requirements.txt
```

# B6: Run my solution
Nếu bạn muốn dùng file infer.py của mình thì nhớ set resnet34, resnet101 hay resnet152 tương ứng với model.pth của bạn nhé. 

```python
!python infer.py  # args run
```

-------------------------------
1. Input Data 
2. Download my pretrain_model:
- I use Unet++ with Resnet101 which has been pre-trained on the pytorch semantic segmentation library, then trained on the competition data set.
- You can download at my Drive link: 
3. Report for Unet++101resnet và Unet++152resnet: 