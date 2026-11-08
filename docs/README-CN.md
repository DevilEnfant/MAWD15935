**论文正式链接：** [MAWD15935: A Large-Scale Manchu Archives Word Dataset](https://doi.org/10.1145/3767308.3838655)

<p align="center">
  <img src="../figure/logo.png" alt="MAWD15935 项目标识" width="100%">
</p>

<h1 align="center">MAWD15935</h1>
<p align="center"><strong>大规模满文档案单词数据集</strong></p>
<p align="center"><strong>已被 ACM Multimedia 2026（ACM MM '26）数据集赛道录用</strong></p>
<p align="center">
  <a href="https://doi.org/10.1145/3767308.3838655">正式论文</a> ·
  <a href="../Supplementary%20Material.pdf">补充材料</a> ·
  <a href="#data-access">申请数据</a> ·
  <a href="#citation">BibTeX</a> ·
  <a href="../README.md">English</a>
</p>

<p align="center">
  Jianjun He · Yucheng Wang · Fengzhi Bao · Yu Zhou · Zhengxu Jin · Ruirui Zheng
</p>
<p align="center"><em>大连民族大学 信息与通信工程学院</em></p>

## 项目简介

**MAWD15935** 是面向**满文档案单词识别**与历史文档分析构建的大规模单词级图像数据集，共包含 **1,092,744 张单词图像**，覆盖 **15,935 个不同的满文单词**。数据集将具有较广词汇覆盖范围的印刷体数据与从真实清代档案中提取的手写体单词图像相结合。

印刷体部分主要依据《新满汉大词典》词条及多种字体制作；手写体部分来源于**大连图书馆馆藏清代内务府档案**。MAWD15935 可用于低资源文字识别（OCR）、历史文档理解、文字结构感知识别及数字人文与文化遗产保护等研究。

### 核心数据指标

| 指标 | MAWD15935 |
|:--|--:|
| **单词图像总数** | **1,092,744** |
| **不同满文单词数** | **15,935** |
| 印刷体图像数 | 975,301 |
| 真实档案手写体图像数 | 117,443 |
| 印刷体单词类别数 | 14,275 |
| 手写体单词类别数 | 2,805 |
| 两个子集共有单词数 | 1,145 |
| 印刷体文档制作所用字体数 | 11 |

**为什么同时采用印刷体与手写体？** 印刷体子集用于扩大词汇覆盖，手写体子集则体现真实历史档案在笔迹、纸张外观及文档保存状态等方面的复杂性。**117,443 张手写体图像全部来自真实档案扫描件**；印刷体子集并不等同于原始档案手稿。

## 数据集组成

### 印刷体单词图像

印刷体部分包含 **975,301 张图像**、**14,275 个单词类别**，词汇主要从《新满汉大词典》中整理而来。除词典扫描材料外，数据集还包含使用以下 11 种满文字体制作的单词文档：

`ZhengBai` · `WenJian` · `YaBai` · `GuFeng` · `ZhengHei` · `BiaoHei` · `WenQin` · `XingShu` · `LiuYe` · `YingBi` · `ShuKai`

### 真实档案手写体单词图像

手写体部分包含 **117,443 张图像**、**2,805 个单词类别**，由大连图书馆馆藏的真实清代满文档案扫描件裁切、整理和标注获得。样本按照对应单词的拉丁转写进行分类，例如 `zhuwe/zhuwe_0.png`。其中有 **1,145 个单词**与印刷体子集的词汇重合。

### 标注与文字表示

MAWD15935 提供两类互补的文字表示：**满文拉丁转写**与**满文字元编码**。后者对 **35 个满文字母**的书写变体进行编码，归纳为 **112 种字元形式**，采用 `M002` 等标识符。配套的转换规则文档给出了拉丁字母、满文字形与字元编码之间的对应关系。

## 数据组织形式

以下目录树展示了研究人员在申请获取数据集后收到的**数据包组织结构**，并不表示完整数据可直接从本 GitHub 仓库下载。

```text
MAWD15935/
├── encoding_conversion_rules/
│   ├── grapheme encoding.docx
│   ├── latin transliteration.docx
│   └── Table of Conversion Relations Between Latin Characters and Manchu Grapheme Encoding.pdf
├── extra_data/
│   ├── Manchu Dataset of Real Handwritten Archives (2805)/
│   │   ├── aba/
│   │   │   ├── aba_0.png
│   │   │   └── aba_1.png
│   │   ├── abade/
│   │   │   ├── abade_0.png
│   │   │   └── ...
│   │   └── ...
│   └── extra_data_intro.pdf
├── main_data/
│   ├── data_docx/
│   │   ├── 1.docx
│   │   ├── 2.docx
│   │   └── ...
│   └── data_docx_intro.pdf
└── main_data_anno/
    ├── annotation.xlsx
    └── main_data_anno_intro.pdf
```

| 目录 | 内容说明 |
|:--|:--|
| `encoding_conversion_rules/` | 满文拉丁转写及字元编码转换规则文档。 |
| `extra_data/` | 按单词拉丁转写归类的真实档案手写体图像及说明文件。 |
| `main_data/` | 使用 11 种字体制作、按编号命名的印刷体满文单词文档及说明文件。 |
| `main_data_anno/` | 单词标注电子表格及说明文件。 |

其中，`main_data_anno/annotation.xlsx` 的 **A–E 列**分别记录单词编号、拉丁转写、汉语释义、备注及重复编号，**F–P 列**记录对应的 11 种字体形式。原始标注表中标记的错误词条已在数据集构建过程中剔除。

## 基准评测协议

[ACM MM '26 正式论文](https://doi.org/10.1145/3767308.3838655) 使用八种识别方法，并设计了互补的评测设置：

- **按样本划分：** 随机采用 **80% 训练 / 20% 测试**，训练集与测试集可以包含相同的单词类别，用于衡量模型对已见词汇不同视觉样本的识别能力。
- **按单词类别划分：** 采用**词汇不重合的 80% / 20% 划分**，训练集与测试集不共享单词类别，用于评估模型对未见单词的泛化能力。
- **手写体数据比例实验：** 结合印刷体数据，改变真实档案手写体训练样本的比例，研究模型在档案场景下的识别表现。

以上为**论文报告的评测协议**，不代表本仓库已经提供预生成的数据划分文件。实验设置与基准结果请以正式论文为准。

<a id="data-access"></a>
## 数据集申请与获取

**MAWD15935 采用联系作者申请获取的方式提供数据。** 如需使用完整数据集，请以 **`MAWD15935 Dataset Access Request`** 为邮件主题，联系以下**任意一位**负责人：

| 联系人 | 职责 | 电子邮箱 |
|:--|:--|:--|
| **郑蕊蕊（Ruirui Zheng）** | 通讯作者 | [zrr@dlnu.edu.cn](mailto:zrr@dlnu.edu.cn) |
| **王宇骋（Yucheng Wang）** | GitHub 仓库所有者与维护者 | [wyc_24kbaekhyun@163.com](mailto:wyc_24kbaekhyun@163.com) |
| **贺建军（Jianjun He）** | 第一作者 | [jianjunhe@live.com](mailto:jianjunhe@live.com) |

**请在申请邮件中提供以下信息：**

1. **所属机构：** 学校、研究机构或其他组织的名称。
2. **联系邮箱：** 便于后续联系和接收数据获取说明的邮箱地址。
3. **使用意图：** 简要介绍研究或教学项目，以及计划如何使用 MAWD15935 数据集。

作者团队将在核对申请信息后，根据适用的数据使用条款向科研申请者**提供数据集及获取说明**。本项目页面**不提供完整数据集的公开直链下载**。

## 适用范围与使用条款

MAWD15935 旨在支持历史满文档案文字识别研究。解读实验结果时需要注意两点：一是印刷体图像并非原始档案手稿；二是手写体数据集中来源于特定馆藏，跨档案来源、跨书写风格的泛化能力仍需进一步验证。

- **仓库代码：** 本仓库原创代码和脚本（如有，且未另行声明）采用 **MIT License**。
- **数据集资料：** 单词图像、标注及其他数据资产仅供**非商业学术研究与教学**。商业用途及原始数据集的再分发须事先取得相关权利人的许可；使用者应保留署名和来源信息，并遵守档案材料及第三方资源的适用限制。
- **正式论文：** ACM 发表的论文采用 **CC BY 4.0** 许可。该论文的开放许可**并不自动适用于**数据集图像、档案原始资料或第三方字体文件。

使用 MAWD15935 开展研究并发表成果时，请规范引用正式论文。涉及授权或使用许可的问题，请联系[数据集申请与获取](#data-access)部分列出的负责人。

<a id="citation"></a>
## 论文引用

如 MAWD15935 对您的研究有所帮助，请引用 **ACM MM 2026 正式发表论文**：

```bibtex
@inproceedings{he2026mawd15935,
  author    = {Jianjun He and Yucheng Wang and Fengzhi Bao and Yu Zhou and Zhengxu Jin and Ruirui Zheng},
  title     = {MAWD15935: A Large-Scale Manchu Archives Word Dataset},
  booktitle = {Proceedings of the 34th ACM International Conference on Multimedia},
  year      = {2026},
  publisher = {Association for Computing Machinery},
  doi       = {10.1145/3767308.3838655},
  url       = {https://doi.org/10.1145/3767308.3838655}
}
```

**论文补充材料：** [`Supplementary Material.pdf`](../Supplementary%20Material.pdf) 提供部分特殊字元情况的解释及字元频次统计分析。

## 问题反馈与项目维护

如需申请数据、咨询标注或授权、开展合作，请通过上述联系方式与作者团队联系。仓库文档勘误与项目问题也可通过 [GitHub Issues](https://github.com/DevilEnfant/MAWD15935/issues) 反馈。
