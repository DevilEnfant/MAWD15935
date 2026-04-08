<p align="center">
  <img src="../figure/logo.png" alt="MAWD15935 Logo" width="100%">
</p>

# A Large-Scale Manchu Archives Word Dataset

[`中文`](./README-CN.md)｜ [`ENG`](../README.md)

## 🔍 介绍

**MAWD15935**是首个面向**满文档案单词识别**的大规模数据集，共包含**1,092,744**个单词图像样本，来源于**15,935**个满文单词，其中包括**975,301**个印刷体样本和**117,443**个手写体样本。该数据集主要基于《新满汉大词典》以及大连图书馆馆藏清代真实满文档案构建而成。特别地，所有手写体样本均采集自真实档案扫描图像，这使得该数据集在历史文档分析研究中具有很高的价值。凭借大规模的词汇覆盖、多样的书写风格以及真实的档案特性，MAWD15935为满文单词识别、历史文档理解以及濒危语言资源数字化研究提供了一个坚实的基准。

---

## 📙 论文补充材料

论文相关的补充材料可在 [`Supplementary Material.pdf`](../Supplementary%20Material.pdf) 中获取。

## 🧩 数据集结构

```text
MAWD15935
├── encoding_conversion_rules
│   ├── grapheme encoding.docx
│   ├── latin transliteration.docx
│   └── Table of Conversion Relations Between Latin Characters and Manchu Grapheme Encoding.pdf
├── extra_data
│   ├── Manchu Dataset of Real Handwritten Archives (2805)
│   │   ├── aba
│   │   │   ├── aba_0.png
│   │   │   └── aba_1.png
│   │   ├── abade
│   │   │   ├── abade_0.png
│   │   │   ├── abade_1.png
│   │   │   ├── abade_2.png
│   │   │   └── abade_3.png
│   │   ├── ......
│   └── extra_data_intro.pdf
├── main_data
│   ├── data_docx
│   │   ├── 1.docx
│   │   ├── 2.docx
│   │   ├── 3.docx
│   │   ├── 4.docx
│   │   ├── 5.docx
│   │   └── ...... (14270 more files)
│   └── data_docx_intro.pdf
└── main_data_anno
    ├── annotation.xlsx
    └── main_data_anno_intro.pdf
```

## 📂 数据集概览

发布的 **MAWD15935** 仓库主要由四个部分组成：**encoding_conversion_rules**、**extra_data**、**main_data** 和 **main_data_anno**。相关文件可以在数据集压缩包或[`这里`](../docs/)找到。

### 1. `encoding_conversion_rules`
该文件夹提供了与文字转换和标注解释相关的辅助材料，包括：

- `latin transliteration.docx`
- `grapheme encoding.docx`
- `Table of Conversion Relations Between Latin Characters and Manchu Grapheme Encoding.pdf`

这些文件描述了满文字元编码与拉丁转写之间的对应关系，旨在帮助用户理解 MAWD15935 所采用的标注体系。

### 2. `extra_data`
这一部分包含**真实手写档案满文单词数据**：

- `Manchu Dataset of Real Handwritten Archives (2805)`
- `extra_data_intro.pdf`

手写数据来源于**大连图书馆藏清代内务府档案**。  
该子集共包含 **2,805 类满文单词**和 **117,443 个样本**。

同一个单词的样本被存放在同一个文件夹中。  
每个文件夹以对应满文单词的**拉丁转写形式**命名，文件夹内的图像文件也遵循相同的命名方式。例如，`zhuwe` 文件夹中仅包含 *zhuwe* 这一单词的图像样本。在这 2,805 个手写类别中，有 **1,145 个单词**与《新满汉大词典》中的词条一致。

### 3. `main_data`
这一部分提供了**11 种字体的印刷体满文单词文档**：

- `data_docx`
- `data_docx_intro.pdf`

该部分数据来源于 `manchu_new_base_14536` 数据集。  
其中，单词编号和满文单词内容均与该数据集保持一致。文件以各满文单词的**编号**命名。

该部分共包含 **14,275 个满文单词**，每个单词均以 **11 种字体形式**呈现，分别为：

- ZhengBai
- WenJian
- YaBai
- GuFeng
- ZhengHei
- BiaoHei
- WenQin
- XingShu
- LiuYe
- YingBi
- ShuKai

这些字体文档构成了数据集中的印刷体部分，并为真实手写档案样本提供了重要补充。对应的 **11 个 TTF 字体文件**也可在仓库根目录下的 [`fonts`](./fonts) 文件夹中找到。

### 4. `main_data_anno`
这一部分包含满文单词的**标注信息表**：

- `annotation.xlsx`
- `main_data_anno_intro.pdf`

该标注文件记录了每个单词的关键元数据，包括：

- 单词编号
- 拉丁转写
- 汉语释义
- 备注信息
- 对应的 11 种字体形式

更具体地说：

- A 列：单词编号
- B 列：拉丁转写
- C 列：汉语释义
- D 列：备注信息
- E 列：重复编号
- F 到 P 列：该满文单词对应的 11 种字体形式

原始标注表中以红色标出的词条表示错误满文单词，需要删除。这些错误词条已经在最终构建的数据集中被移除。

## 📊 数据集统计

MAWD15935 共包含 **1,092,744** 个单词图像样本，来源于 **15,935** 个不同的满文单词。

### 基本统计数据

| 项目 | 数值 |
|---|---:|
| 总样本数 | 1,092,744 |
| 满文单词总数 | 15,935 |
| 印刷体样本数 | 975,301 |
| 手写体样本数 | 117,443 |
| 印刷体单词类别数 | 14,275 |
| 手写体单词类别数 | 2,805 |
| 印刷体与手写体重合单词数 | 1,145 |
| 印刷体字体种类数 | 11 |

### 子集组成

该数据集由两个相互补充的部分组成，即大规模印刷体子集和真实手写档案子集。

**印刷体子集**包含 **975,301** 个样本，覆盖 **14,275** 个满文单词。每个单词均以 **11 种字体形式**呈现，这些字体为数据集提供了较丰富的印刷体外观变化，并增强了其视觉多样性。

**手写体子集**包含 **117,443** 个样本，覆盖 **2,805** 个满文单词。这些样本来源于真实的清代档案文献，能够反映历史满文档案中的真实手写风格。

印刷体子集与手写体子集中共有 **1,145** 个重合单词。在将这两个部分合并并按词汇层面去重后，最终数据集共包含 **15,935** 个不同的满文单词。

### 分布特征

该数据集同时具备较广的词汇覆盖范围和较强的样本多样性。

对于手写体子集，超过 **90%** 的满文单词拥有 **20 个以上样本**。  
对于印刷体子集，超过 **95%** 的满文单词拥有 **30 到 100 个样本**。

总体而言，MAWD15935 兼具大规模词汇覆盖、丰富的印刷体风格变化以及真实的手写档案样本，因此可为满文档案单词识别和历史文档分析研究提供有价值的数据资源。

## ⏬ 下载

| 资源 | 链接 | 密码 |
|---|---|---|
| 百度网盘 | [百度网盘](https://pan.baidu.com/s/1HYC6KksEineLi56Jh4t3rQ) | `MAWD` |
| 谷歌云盘 | [谷歌云盘](https://pan.baidu.com/s/1HYC6KksEineLi56Jh4t3rQ) | none |

## 🔗 引用

如果要在您的研究中使用 **MAWD15935**，请使用以下的临时引用:

```bibtex
@misc{mawd15935,
  title               = {MAWD15935: A Large-Scale Manchu Archives Word Dataset},
  author           = {Jianjun He and Yucheng Wang and Fengzhi Bao and Yu Zhou and Zhengxu Jin and Ruirui Zheng},
  year              = {2026},
  note              = {Under review},
  howpublished = {GitHub repository}
}
```

## ⭕️ 许可和使用条款

### 代码许可

除非另有说明，本仓库中的代码与脚本部分采用 **MIT License** 发布。

### 数据许可

**MAWD15935** 数据集，包括单词图像、标注文件、文档及补充材料，仅供**非商业科研与教学用途**使用。

访问、下载或使用本数据集即视为用户同意以下条款：

1. 本数据集仅可用于学术研究、教学和教育相关用途。
2. 未经版权所有者事先书面许可，不得将本数据集用于商业用途，不得为商业目的进行再分发，也不得将其整合进商业产品或服务中。
3. 凡使用本数据集或基于本数据集开展研究并形成论文、报告或其他衍生成果者，必须规范引用MAWD15935论文及本仓库。
4. 未经许可，用户不得向第三方重新分发完整原始数据集。
5. 用户可以出于科研目的生成处理结果，但不得删除原始署名、版权声明或来源信息。
6. 用户还应遵守与原始档案来源及第三方材料相关的其他适用要求。
7. 本数据集按“现状”提供，不对其完整性、准确性或特定用途适用性作任何形式的担保。

### 第三方材料

本仓库中的部分材料，例如字体文件或与档案来源相关的内容，可能受到额外的第三方权利或使用限制约束。用户在使用相关材料时，应自行遵守对应条款。

### 联系

如有许可、授权或商业使用相关问题，请联系【联系我们】章节中列出的作者。

## 📮 联系我们

如对数据集、标注信息及相关研究内容有任何问题，可联系以下人员：

- **Ruirui Zheng** (zrr@dlnu.edu.cn) — 通讯作者
- **Yucheng Wang** (wyc_24kbaekhyun@163.com) — 本GitHub仓库拥有者及维护者
- **Jianjun He** (jianjunhe@live.com) — 第一作者及本文主要写作者

如果是仓库使用、文档更新或资料说明等相关问题，也可以直接在本GitHub仓库中提交issue。