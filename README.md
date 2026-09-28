# BERT-Based Semantic Role Labeling

This repository contains a PyTorch and BERT implementation of PropBank-style semantic role labeling as a token-level BIO sequence-labeling task.

## Repository contents

```text
notebooks/semantic-role-labeling-bert.ipynb  Main experiment notebook
data/                                        Local-only data directory
src/                                         Space for reusable model/data modules
tests/                                       Space for unit tests
results/                                     Space for metrics and figures
reports/                                     Space for research notes
```

## Setup

```bash
python -m venv .venv
source .venv/bin/activate       # macOS/Linux
# .venv\Scripts\activate        # Windows
pip install -r requirements.txt
```

The notebook expects a GPU-enabled PyTorch environment for fine-tuning BERT. It was originally written for Python 3.7 and may require small compatibility updates with current versions of PyTorch and Transformers.

## Dataset

The notebook uses OntoNotes 5.0 / PropBank-style annotations. The dataset is not included in this repository because the notebook states that it is provided for COMS 4705 use only and may be subject to LDC licensing restrictions.

See [`data/README.md`](data/README.md) for local setup instructions. Do not commit the dataset, downloaded archive, or generated annotation files.

## Notebook

Open `notebooks/semantic-role-labeling-bert.ipynb` after placing authorized local copies of the required data files in the notebook working directory.

## Academic and licensing note

This work originated as a course assignment. Keep the repository private unless you have confirmed that publication is allowed by the course policy and dataset license. Before public release, remove assignment instructions and any completed answer content, and rewrite the notebook as an independent project report.
