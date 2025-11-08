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



