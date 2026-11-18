# Project 1 运行说明

本项目使用 NumPy 实现 OpenCLIP ViT-B-32 图像编码器。将完成的 `image_encoder.py` 放回课程提供的 `project1-numpy-student` 目录，在该目录打开终端。使用 Python 3.9 或更新版本。

```powershell
python -m pip install -r requirements.txt
python check.py --stage all
python run.py --output output_tokens.npz
```

`check.py` 会逐阶段与课程参考结果比较。`run.py` 默认处理课程提供的 10 张图片，将结果保存到 `output_tokens.npz`。其中 `ids` 记录图片顺序，`output_tokens` 是形状为 `(10, 512)` 的 `float32` 数组，每行对应一张图。

也可以处理自己的图片：

```powershell
python run.py --images "photo.jpg" --output my_tokens.npz
```
