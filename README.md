# DeBiFormer Implementation & T2T-Vit

## 安裝與使用
### 環境準備
```bash
# Install dependencies
pip install torch torchvision timm
pip install -r re.txt
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
下載Cifar10.100資料集

### DeBiFormer訓練指令
# 在 ImageNet 上訓練 DeBiFormer-Small 模型
```
python train.py --model debiformer_small --dataset imagenet --data-path ./dataset/imagenet --epochs 300 --batch-size 128
```
# 在 CIFAR-10 上訓練
```
python train.py --model debiformer_small --dataset cifar10 --epochs 100 --batch-size 64
```
# 在 CIFAR-100 上訓練
```
python train.py --model debiformer_small --dataset cifar100 --epochs 100 --batch-size 64
```


## 實驗結果
| Model/Datset | DeBiFormer-Small |BiFormer-Base|T2T-ViT-14|T2T-ViT-19|
|:---:|:---:|:---:|:---:|:---:|
|參數量(M)|25.5|57|21.5|39.1|
|計算量FLOPs(G)|4.5|9.8|4.8|8.5|
|ImageNet(Top-1)|83.8%|84.3%|81.5%|81.9%|
|CIFAR-10 (Top-1)|97.8%|98.4%|97.5%|98.3%|
|CIFAR-100 (Top-1)|88.7%|89.3%|88.4%|89.0%|

