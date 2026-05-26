# DeepStudy - 深度学习视觉项目工具库

这是一个针对计算机视觉任务（特别是 RoboMaster 视觉识别相关）的深度学习项目工具库。本项目涵盖了从数据采集、预处理、标签转换、模型训练到推理部署的全流程脚本。

## 📁 目录结构

- **[01_data_preprocessing](file:///c:/Users/30855/Desktop/DeepStudy/01_data_preprocessing)**: 数据预处理工具，包括视频抽帧、数据集划分、数据增强（背景分离、装甲板提取等）。
- **[02_label_processing](file:///c:/Users/30855/Desktop/DeepStudy/02_label_processing)**: 标签格式转换工具，支持 XML、JSON、TXT (YOLO) 等多种格式互转及标注优化。
- **[03_dataset_management](file:///c:/Users/30855/Desktop/DeepStudy/03_dataset_management)**: 数据集管理工具，用于数据清洗、批量重命名及类别提取。
- **[04_yolo_training](file:///c:/Users/30855/Desktop/DeepStudy/04_yolo_training)**: YOLO 系列模型训练与评估脚本。
- **[05_model_conversion](file:///c:/Users/30855/Desktop/DeepStudy/05_model_conversion)**: 模型转换工具，支持将 `.pt` 导出为 ONNX、OpenVINO 等部署格式。
- **[06_model_inference](file:///c:/Users/30855/Desktop/DeepStudy/06_model_inference)**: 模型推理脚本，包含视频/图片检测及不同平台的验证代码。
- **[07_classifier_training](file:///c:/Users/30855/Desktop/DeepStudy/07_classifier_training)**: 基础分类器（MLP, LeNet）的训练与部署脚本。
- **[08_utils](file:///c:/Users/30855/Desktop/DeepStudy/08_utils)**: 通用工具类，涵盖图像处理、文件操作等辅助功能。
- **[09_documentation](file:///c:/Users/30855/Desktop/DeepStudy/09_documentation)**: 项目相关技术文档与操作指南。

## ✨ 主要功能

- **全流程覆盖**: 从原始视频抽帧到最终模型部署的一站式解决方案。
- **多格式支持**: 兼容 YOLOv5、YOLOv8 等主流目标检测框架，支持多种标注格式转换。
- **自动化工具**: 提供大量批处理脚本，极大提高数据集准备和模型验证的效率。
- **部署优化**: 包含针对 OpenVINO 和 ONNX Runtime 的模型导出与量化检查。

## 🚀 快速开始

### 1. 环境准备
项目依赖可以通过 `environment.yml` 进行配置：
```bash
conda env create -f environment.yml
conda activate DeepStudy
```

### 2. 数据准备
使用 `01_data_preprocessing` 下的脚本进行视频抽帧：
```bash
python 01_data_preprocessing/01_video_frame_extraction.py
```

### 3. 模型训练
进入 `04_yolo_training` 目录开始训练：
```bash
python 04_yolo_training/01_train_yolo_model.py
```

### 4. 模型部署
将训练好的模型转换为 ONNX 格式：
```bash
python 05_model_conversion/01_pt_to_onnx_openvino.py
```

## 🛠️ 技术细节

- **检测框架**: YOLOv5, YOLOv8
- **分类网络**: MLP, LeNet
- **推理引擎**: ONNX Runtime, OpenVINO
- **数据处理**: OpenCV, NumPy, PIL

---
*本项目主要用于深度学习视觉算法的学习与实践，欢迎参考与改进。*
