# HLS-Repair-Dataset

本数据集面向 **高层次综合（High-Level Synthesis, HLS）程序自动修复**任务，包含 **6182** 条 C/C++ 代码修复样本对。每条样本由一段不可综合的 HLS C 源代码及其对应的可综合修复版本构成，可用于大语言模型微调、检索增强生成（RAG）以及自动程序修复相关研究。


## 使用方式

```python
import csv

with open("hls_repair_dataset.csv", "r", encoding="utf-8") as f:
    reader = csv.DictReader(f)
    for row in reader:
        error_type = row["0"]
        buggy = row["1"]
        fixed = row["2"]
        # 用于模型训练、RAG检索等下游任务
```

## 不可综合类型

0：指针  
1：动态数组  
2：递归  
3：布尔运算  
4：异常处理  

## 引用

如使用本数据集，请引用：

> 基于参数高效微调和 RAG 的 HLS 程序自动修复研究

## 许可证

本数据集仅供学术研究使用。
