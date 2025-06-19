# DeBiFormer Implementation
### Vision Transformer with Deformable Agent Bi-level Routing Attention - Student Project

## 安裝與使用
### 環境準備
```bash
# Install dependencies
pip install torch torchvision timm
pip install -r requirements.txt
```
### 資料準備
下載 ImageNet 資料集並按以下結構組織：
```
dataset/imagenet/
├── train/
│   ├── n01440764/
│   │   ├── image1.JPEG
│   │   └── ...
│   └── ...
└── val/
    ├── n01440764/
    │   ├── image1.JPEG
    │   └── ...
    └── ...
```
## 實驗結果
| Model/Datset | DeBiFormer-Small |BiFormer-Base|T2T-ViT-14|T2T-ViT-19|
|:---:|:---:|:---:|:---:|:---:|
|參數量(M)|25.5|57|21.5|39.1|
|計算量FLOPs(G)|4.5|9.8|4.8|8.5|
|ImageNet(Top-1)|83.8%|84.3%|81.5%|81.9%|
|CIFAR-10 (Top-1)|97.8%|98.4%|97.5%|98.3%|
|CIFAR-100 (Top-1)|88.7%|89.3%|88.4%|89.0%|
