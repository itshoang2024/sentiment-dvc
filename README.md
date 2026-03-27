<div align="center">

  # Tutorial: Data Version Control with DVC

  <img src="https://img.shields.io/badge/DVC-13ADC7?style=for-the-badge&logo=dvc&logoColor=white" />
  <img src="https://img.shields.io/badge/DagsHub-6B4FBB?style=for-the-badge&logo=dagshub&logoColor=white" />
</div>

---

## Overview

This project demonstrates how to use **[DVC (Data Version Control)](https://dvc.org/)** to manage data versioning in Machine Learning / NLP projects. The exercise covers:

- Initializing DVC in a Git repository
- Tracking datasets with DVC
- Configuring remote storage on **[DagsHub](https://dagshub.com/)**
- Pushing and pulling data between local and remote

## Getting Started

### Prerequisites

- Python ≥ 3.8
- [Git](https://git-scm.com/)
- [DVC](https://dvc.org/doc/install)

### 1. Clone the repository

```bash
git clone https://github.com/itshoang2024/sentiment-dvc-code.git
cd sentiment-dvc-code
```

### 2. Install DVC

```bash
pip install dvc
```

### 3. Pull data from remote

```bash
dvc pull
```

> Data is stored on DagsHub at:  
> `https://dagshub.com/itshoang2024/sentiment-dvc-data.dvc`

### 4. Common DVC Commands

| Command             | Description                              |
| ------------------- | ---------------------------------------- |
| `dvc init`          | Initialize DVC in the repo               |
| `dvc add <file>`    | Start tracking a file with DVC           |
| `dvc push`          | Push data to remote storage              |
| `dvc pull`          | Pull data from remote storage            |
| `dvc status`        | Check data change status                 |
| `dvc remote list`   | List configured remotes                  |

## 🔗 Links

| Resource              | URL                                                        |
| --------------------- | ---------------------------------------------------------- |
| Source Code (GitHub)   | https://github.com/itshoang2024/sentiment-dvc-code        |
| Data Storage (DagsHub) | https://dagshub.com/itshoang2024/sentiment-dvc-data       |
| DVC Documentation      | https://dvc.org/doc                                       |

## 📝 Notes

- `sentiment.csv` is tracked by DVC, so it is **not** stored directly in Git. Instead, Git only stores the `.dvc` metafile containing metadata (hash, size).
- Run `dvc pull` after cloning the repo to download the actual data files.
