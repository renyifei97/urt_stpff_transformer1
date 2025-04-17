
# 🚆 城轨线网客运量预测（Transformer模型）

本项目基于PyTorch实现了Transformer，用于预测城轨线网15分钟粒度的客运量数据。

## 📂 项目结构

```
.
├── transformer_model.py        # 主程序，包含数据读取、模型训练与预测
├── transformer_model.pth       # 保存的模型参数文件
├── Transformer.png             # 模型预测结果可视化图
└── README.md                   # 项目说明文档
```

## 🛠️ 环境配置

- Python 3.x
- PyTorch
- SQLAlchemy
- psycopg2
- pandas
- numpy
- matplotlib
- scikit-learn

## 🔧 使用方法

### 1. 配置数据库连接

修改`transformer_model.py`中的数据库配置（`db_config`），确保连接到你的本地PostgreSQL数据库。

### 2. 运行代码

```bash
python transformer_model.py
```

- 首次运行时，模型会训练并保存参数到`transformer_model.pth`。
- 再次运行时，会自动加载模型进行预测，无需重复训练。
- 如需强制重新训练，删除或重命名 transformer_model.pth 后再次运行。

## 📅 数据说明

- **训练数据**：2023-04-01 至 2024-07-01
- **测试数据**：2024-07-01 至 2024-07-08

## 📈 输出结果

- 预测结果图保存为：`Transformer.png`
- 模型评价指标（MSE、MAE、MAPE、R²）将在终端输出。
![Transformer.png](Transformer.png)

## 🚀 后续计划

- 加入学习率调度（LR scheduler）与早停机制（Early Stopping）
- 拆分验证集、支持多步（Multi-step）预测
- 融入外部特征（周几、节假日、天气等）
- 使用 TensorBoard 或 Weights & Biases 监控训练过程


