# MAWD15935: A Large-Scale Manchu Archives Word Dataset

> Official repository for **MAWD15935: A Large-Scale Manchu Archives Word Dataset**

[![Project Page](https://img.shields.io/badge/Project-Website-blue)](https://github.com/your-org/MAWD15935)
[![Paper](https://img.shields.io/badge/Paper-ArXivorOpenReview-red)](PASTE_PAPER_LINK_HERE)
[![License](https://img.shields.io/badge/License-PASTE_LICENSE_NAME-green)](./LICENSE)

---

## Overview

**MAWD15935** is a large-scale Manchu archival word dataset for research on historical document analysis.

This repository serves as the **official dataset website**, providing:

- dataset overview
- access instructions
- license and terms of use
- data organization
- annotation protocol
- benchmark tasks
- evaluation protocol
- baseline resources
- supplementary materials
- ethics and responsible use statement

If you use **MAWD15935** in your research, please cite our paper.

---

## News

- **[2026-xx-xx]** Repository released.
- **[2026-xx-xx]** Dataset website is online.
- **[2026-xx-xx]** Benchmark code and evaluation protocol released.
- **[2026-xx-xx]** Supplementary materials released.

---

## Dataset at a Glance

- **Dataset name:** MAWD15935
- **Full title:** *MAWD15935: A Large-Scale Manchu Archives Word Dataset*
- **Domain:** historical document analysis
- **Language or script:** Manchu
- **Data granularity:** word-level
- **Number of samples:** 15,935
- **Source documents:** `PASTE_NUMBER_OR_DESCRIPTION_HERE`
- **Tasks supported:** `PASTE_TASKS_HERE`
- **Annotation type:** `PASTE_ANNOTATION_TYPE_HERE`
- **License:** `PASTE_LICENSE_NAME_HERE`

> Please replace the fields above with the final official statistics.

---

## Table of Contents

- [Overview](#overview)
- [News](#news)
- [Dataset at a Glance](#dataset-at-a-glance)
- [Project Page and Access](#project-page-and-access)
- [Download](#download)
- [Dataset Structure](#dataset-structure)
- [Data Splits](#data-splits)
- [Annotation Format](#annotation-format)
- [Collection and Annotation Protocol](#collection-and-annotation-protocol)
- [Dataset Statistics](#dataset-statistics)
- [Benchmark Tasks](#benchmark-tasks)
- [Evaluation Protocol](#evaluation-protocol)
- [Baselines and Resources](#baselines-and-resources)
- [Supplementary Materials](#supplementary-materials)
- [License and Terms of Use](#license-and-terms-of-use)
- [Ethics and Responsible Use](#ethics-and-responsible-use)
- [Citation](#citation)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

---

## Project Page and Access

**Official dataset website:**  
`https://github.com/your-org/MAWD15935`

This repository is the main public entry for **MAWD15935**.  
It contains dataset documentation, access instructions, benchmark details, and supplementary materials.

For stable access, we recommend providing **at least one international mirror** in addition to any mainland China mirror.

---

## Download

### Main Access

- **Project page:** `PASTE_PROJECT_PAGE_LINK_HERE`
- **International mirror:** `PASTE_HF_ZENODO_GDRIVE_OR_SERVER_LINK_HERE`
- **Mainland China mirror:** `PASTE_BAIDU_PAN_LINK_HERE`
- **Extraction code:** `PASTE_CODE_HERE`
- **Checksum file:** `PASTE_CHECKSUM_LINK_HERE`

### Notes

1. Please read the license and terms of use before downloading.
2. The dataset is intended for academic research purposes unless otherwise stated.
3. If access requires an application form or agreement, provide the instructions here.
4. If some files are updated after release, please check the checksum file before use.

### Recommended Download Statement

```text
The international mirror is recommended for reviewers and overseas users.
The mainland China mirror is provided as an additional convenience channel.
```

---

## Dataset Structure

```text
MAWD15935/
├── README.md
├── LICENSE
├── DATA_LICENSE.md
├── docs/
│   ├── supplementary.pdf
│   ├── annotation_guidelines.pdf
│   ├── benchmark_details.pdf
│   └── ethics_statement.pdf
├── images/
│   ├── train/
│   ├── val/
│   └── test/
├── annotations/
│   ├── train.json
│   ├── val.json
│   └── test.json
├── splits/
│   ├── train.txt
│   ├── val.txt
│   └── test.txt
├── evaluation/
│   ├── eval_protocol.md
│   └── metrics_description.md
└── checksums/
    └── sha256.txt
```

> Adjust this structure to match your actual release package.

---

## Data Splits

We recommend reporting results on the official split released with the dataset.

| Split | Number of samples | Description |
|---|---:|---|
| Train | `PASTE_NUMBER_HERE` | Training set |
| Val | `PASTE_NUMBER_HERE` | Validation set |
| Test | `PASTE_NUMBER_HERE` | Test set |
| Total | `15,935` | Full dataset |

### Split Policy

Please clearly state:

- whether the split is document-independent
- whether pages from the same archival source can appear across different subsets
- whether there are writer, page, or source overlaps
- whether any manually filtered subset exists for benchmarking

Suggested statement:

```text
The official train, val, and test split is fixed and should be used for all benchmark comparisons unless otherwise stated.
```

---

## Annotation Format

Please describe the exact annotation format here.

### Example

```json
{
  "image_id": "page_0001_word_00001",
  "file_name": "images/train/page_0001_word_00001.jpg",
  "transcription": "PASTE_SAMPLE_HERE",
  "bbox": [x_min, y_min, width, height],
  "source_page": "page_0001",
  "split": "train"
}
```

### Field Description

| Field | Type | Description |
|---|---|---|
| `image_id` | string | Unique sample identifier |
| `file_name` | string | Relative path to the image |
| `transcription` | string | Ground-truth word transcription |
| `bbox` | list | Bounding box if applicable |
| `source_page` | string | Original page identifier |
| `split` | string | Official split name |

> Delete fields that are not used in your final release.

---

## Collection and Annotation Protocol

### Data Source

Describe the source of the Manchu archival materials:

- institution or archive name
- digitization source
- acquisition process
- scanning or photography settings if relevant
- time period and document types if relevant

### Preprocessing

Describe:

- cropping or segmentation pipeline
- image cleaning or normalization
- duplicate removal
- low-quality filtering
- naming rules

### Annotation Procedure

Describe:

- who annotated the data
- annotation tools
- annotation stages
- quality control process
- dispute resolution strategy
- expert verification process

Suggested subsections:

#### Step 1. Source document acquisition  
`PASTE_DETAILS_HERE`

#### Step 2. Word region extraction  
`PASTE_DETAILS_HERE`

#### Step 3. Manual annotation and verification  
`PASTE_DETAILS_HERE`

#### Step 4. Final quality control  
`PASTE_DETAILS_HERE`

---

## Dataset Statistics

Please replace the following placeholders with final official numbers.

### Basic Statistics

| Item | Value |
|---|---:|
| Total word images | 15,935 |
| Total source pages | `PASTE_NUMBER_HERE` |
| Total archival documents | `PASTE_NUMBER_HERE` |
| Number of unique labels or vocabulary items | `PASTE_NUMBER_HERE` |
| Average image width | `PASTE_NUMBER_HERE` |
| Average image height | `PASTE_NUMBER_HERE` |

### Distribution Analysis

You may also report:

- word length distribution
- source archive distribution
- document type distribution
- image quality distribution
- frequency imbalance
- rare word statistics

Suggested text:

```text
MAWD15935 exhibits substantial variability in writing style, document condition, background noise, and word morphology, making it suitable for benchmarking robust historical document analysis methods.
```

---

## Benchmark Tasks

Please fill in the actual supported tasks.

Possible task descriptions:

### 1. Word Recognition

Given a cropped word image, predict the target transcription.

### 2. Word Retrieval or Spotting

Given a query, retrieve matching word instances from the dataset.

### 3. Historical Document Representation Learning

Use the dataset for pretraining, retrieval, or feature learning under historical document settings.

### 4. Other Tasks

`PASTE_ADDITIONAL_TASKS_HERE`

---

## Evaluation Protocol

Describe the official evaluation setup in a precise and reproducible way.

### Metrics

Please specify the exact metrics used in your benchmark, for example:

- Accuracy
- Character Error Rate
- Word Error Rate
- Mean Average Precision
- Precision at K
- Recall at K
- F1 score

### Reporting Rule

Suggested template:

```text
All methods should be trained on the official training split, optionally tuned on the validation split, and evaluated on the official test split. No external training data should be used unless explicitly stated.
```

### Example Benchmark Table

| Method | External Data | Metric 1 | Metric 2 | Metric 3 |
|---|---|---:|---:|---:|
| Baseline A | No | `xx.xx` | `xx.xx` | `xx.xx` |
| Baseline B | No | `xx.xx` | `xx.xx` | `xx.xx` |
| Your Method | No | `xx.xx` | `xx.xx` | `xx.xx` |

---

## Baselines and Resources

We recommend releasing at least the following resources:

- data loader
- preprocessing code
- split files
- evaluation script
- one or more baseline implementations
- training config
- inference example

### Resource Links

- **Baseline code:** `PASTE_CODE_LINK_HERE`
- **Evaluation script:** `PASTE_EVAL_LINK_HERE`
- **Training config:** `PASTE_CONFIG_LINK_HERE`
- **Model weights:** `PASTE_WEIGHT_LINK_HERE`

### Reproducibility Notes

Please specify:

- framework and version
- hardware setup
- training epochs
- batch size
- learning rate
- random seed
- preprocessing details

Suggested statement:

```text
We provide benchmark code, evaluation scripts, and split files to support reproducible research on MAWD15935.
```

---

## Supplementary Materials

All additional materials are collected here.

- **Supplementary PDF:** `./docs/supplementary.pdf`
- **Annotation guidelines:** `./docs/annotation_guidelines.pdf`
- **Benchmark details:** `./docs/benchmark_details.pdf`
- **Ethics statement:** `./docs/ethics_statement.pdf`

### Recommended Contents of the Supplementary PDF

- additional dataset statistics
- more visual examples
- annotation interface screenshots
- quality control details
- extended benchmark results
- failure cases
- ablation details
- archive source discussion
- additional implementation details

Suggested note:

```text
The supplementary materials provide extended documentation for data collection, annotation, quality control, benchmark setup, and additional qualitative examples.
```

---

## License and Terms of Use

### Dataset License

This dataset is released under: **`PASTE_LICENSE_NAME_HERE`**

Please include the full license text in `LICENSE` or `DATA_LICENSE.md`.

### Usage Terms

By downloading or using **MAWD15935**, you agree to the following terms:

1. The dataset is used only under the stated license.
2. Users must properly cite the dataset paper.
3. Users must not redistribute modified copies without permission unless explicitly allowed.
4. Users must not use the dataset for unlawful, harmful, or deceptive purposes.
5. Users must respect any archive-specific restrictions described here.

### Access Restriction Statement

Choose one version and keep only the correct one.

#### Option A: Open public access

```text
MAWD15935 is publicly accessible for research use under the license provided in this repository.
```

#### Option B: Access by request

```text
MAWD15935 is available for research use upon request. Please contact the corresponding authors and agree to the usage terms before access is granted.
```

---

## Ethics and Responsible Use

Please clearly describe any ethical or legal considerations.

Suggested topics:

- archival ownership and permissions
- cultural heritage sensitivity
- privacy risk assessment
- limitations for downstream deployment
- potential OCR or recognition bias
- responsible release considerations

Suggested statement:

```text
MAWD15935 is intended for academic research on historical document analysis and cultural heritage computing. Users should verify that any downstream use complies with archive policies, applicable laws, and institutional requirements.
```

### Limitations

Please consider adding a short limitations statement, for example:

```text
The dataset may not fully cover all writing styles, document conditions, archive sources, or historical periods of Manchu documents. Performance on this dataset should not be interpreted as universal performance across all Manchu archival materials.
```

---

## Citation

Please cite the dataset paper if you use **MAWD15935**.

```bibtex
@inproceedings{PASTE_CITATION_KEY_HERE,
  title     = {MAWD15935: A Large-Scale Manchu Archives Word Dataset},
  author    = {PASTE_AUTHORS_HERE},
  booktitle = {Proceedings of the ACM International Conference on Multimedia},
  year      = {2026},
  pages     = {PASTE_PAGES_HERE},
  doi       = {PASTE_DOI_HERE}
}
```

If the paper is not yet published, you may temporarily use:

```bibtex
@misc{PASTE_CITATION_KEY_HERE,
  title        = {MAWD15935: A Large-Scale Manchu Archives Word Dataset},
  author       = {PASTE_AUTHORS_HERE},
  year         = {2026},
  note         = {Under review},
  howpublished = {GitHub repository}
}
```

---

## Contact

For questions about the dataset, please contact:

- `PASTE_NAME_HERE` — `PASTE_EMAIL_HERE`
- `PASTE_NAME_HERE` — `PASTE_EMAIL_HERE`

You may also open an issue in this repository for bug reports or documentation problems.

---

## Acknowledgements

Please acknowledge:

- archive institutions
- funding support
- annotation team
- technical support
- collaborating labs or universities

Suggested template:

```text
We thank the archive institutions, annotators, and collaborators who supported the construction of MAWD15935.
```
