# comfyui-lsnet

### *「我这双眼睛，能将黑暗看得一清二楚」*

  —— 宇智波佐助

![阿吗特拉斯](https://github.com/user-attachments/assets/a9d16b72-b577-4458-bc10-604eb82fefea)

> “*Kaloscope*”（万花筒）致敬万花筒写轮眼，象征忍术(画风)复刻能力

## 核心能力

基于 *LSNet* 技术核心，本工具聚焦两大核心场景：

1. **画风分类**：精准识别单幅作品的风格属性（如动漫、写实、水彩、国风等），如同写轮眼一眼看穿事物本质，快速完成风格标签匹配；

2. **画风聚类**：自动对多组作品按风格特征进行归类聚合，筛选出风格相似的作品群体，实现批量风格整理与分析，提升处理效率

## 第一步：下载必要文件

前往 Hugging Face 仓库，下载两个核心文件：

* `best_checkpoint.pth`（*LSNet 模型权重文件*，决定画风分类与聚类的精度）

* `class_mapping.csv`（*风格类别映射配置文件*，适配不同画风标签的识别与归类）

仓库地址：[ht](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[tps:/](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[/hugg](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[ingfa](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[ce.co](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[/heat](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[hclif](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[f01/K](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[alosc](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[ope/t](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[ree/m](https://huggingface.co/heathcliff01/Kaloscope/tree/main)[ain](https://huggingface.co/heathcliff01/Kaloscope/tree/main)

## 第二步：文件放置与环境配置

### 1. 创建目录结构

在 ComfyUI 的`models`目录下，新建名为`lsnet`的文件夹（专门存放 LSNet 相关模型文件）；

进入`lsnet`文件夹后，可随意创建一个子文件夹（如 “checkpoints”“kaloscope” 等，名称无强制要求，用于归类核心文件）。

目录结构示例：



```
ComfyUI/

└── models/

       └── lsnet/

           └── 子文件夹名称/  # 例："sharingan" 或 “kaloscope”

               ├── best_checkpoint.pth

               └── class_mapping.csv
```

相关操作截图：

* 新建`lsnet`文件夹：

![新建lsnet文件夹](https://github.com/user-attachments/assets/d959be3c-156c-4c54-9076-f9f5a25000a9)

* 在`lsnet`内创建子文件夹：

![创建子文件夹](https://github.com/user-attachments/assets/f64d8e9c-8047-424b-b9b0-8a6ec1732ef0)

### 2. 安装依赖

将上述两个文件放入子文件夹后，执行以下命令安装 LSNet 运行所需依赖：


```
pip install -r requirements.txt
```

## 第三步：启动 ComfyUI 并使用

1. 按常规方式启动 ComfyUI

2. 在画风分析工作流中，调用 LSNet 相关节点，即可触发 “画风分类” 或 “画风聚类” 功能

### 使用示例

![基础推理界面（含LSNet核心节点）](https://github.com/user-attachments/assets/28cc2820-ff5d-4290-8ac2-339763947e91)

聚类暂时不作示例，内有其他节点供开发者使用
