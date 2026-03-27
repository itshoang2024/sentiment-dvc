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
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/12bdeS_ZGzyAGwp3vUrLptK8_-I68MJtb?usp=sharing)

### Prerequisites

- Python ≥ 3.8
- [Git](https://git-scm.com/)
- [DVC](https://dvc.org/doc/install)

### 1. Clone the repository

```bash
git clone https://github.com/itshoang2024/sentiment-dvc.git
cd sentiment-dvc
```

### 2. Install DVC

```bash
pip install dvc
```

### 3. Setup Dagshub credentials

```bash
dvc remote modify dagshub --local user {DASHUB_USER}
dvc remote modify dagshub --local password {DAGSHUB_TOKEN}
```

### 4. Pull data from remote

```bash
dvc pull
```

> Data is stored on DagsHub at:  
> `https://dagshub.com/itshoang2024/sentiment-dvc.dvc`

### 4. Common DVC Commands

| Command             | Description                              |
| ------------------- | ---------------------------------------- |
| `dvc init`          | Initialize DVC in the repo               |
| `dvc add <file>`    | Start tracking a file with DVC           |
| `dvc push`          | Push data to remote storage              |
| `dvc pull`          | Pull data from remote storage            |
| `dvc status`        | Check data change status                 |
| `dvc remote list`   | List configured remotes                  |

## Links

| Resource              | URL                                                        |
| --------------------- | ---------------------------------------------------------- |
| Source Code (GitHub)   | https://github.com/itshoang2024/sentiment-dvc        |
| Data Storage (DagsHub) | https://dagshub.com/itshoang2024/sentiment-dvc       |
| DVC Documentation      | https://dvc.org/doc                                       |

## Notes

- `sentiment.csv` is tracked by DVC, so it is **not** stored directly in Git. Instead, Git only stores the `.dvc` metafile containing metadata (hash, size).
- Run `dvc pull` after cloning the repo to download the actual data files.
