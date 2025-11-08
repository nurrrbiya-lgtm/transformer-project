# Transformer from Scratch - IWSLT2017 English-German Translation

基于PyTorch从零实现的Transformer模型，在IWSLT2017英德翻译数据集上的实验。

## 项目结构
transformer-project/
├── src/
│ ├── model2.py # Transformer模型实现
│ ├── dataset_IWSLT.py # 数据加载与预处理
│ └── utils.py # 工具函数（掩码生成等）
├── scripts/
│ └── run.sh # 训练脚本
├── results/ # 训练结果（曲线图、模型权重）
├── requirements.txt # Python依赖包
├── train_IWSLT.py # 主训练文件
└── README.md # 项目说明

## 环境配置

### 1. 创建conda环境
```bash
conda create -n transformer python=3.10
conda activate transformer

pip install -r requirements.txt

python -m spacy download de_core_news_sm
python -m spacy download en_core_web_sm

# 使用默认参数训练
python train_IWSLT.py

# 指定批大小和设备
python train_IWSLT.py --batch_size 32 --device cuda

# 设置随机种子并开始训练
python -c "import torch; torch.manual_seed(42)" && python train_IWSLT.py --batch_size 16 --epochs 5

模型配置
当前实现的Transformer参数：

嵌入维度: 128

注意力头数: 2

前馈网络维度: 256

编码器层数: 2

解码器层数: 2

词汇表大小: 英语35,437 / 德语61,841

