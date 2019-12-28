<a href="https://explosion.ai"><img src="https://explosion.ai/assets/img/logo.svg" width="125" height="125" align="right" /></a>

# Machine learning dataset loaders

Loaders for various machine learning datasets for testing and example scripts.
Previously in `thinc.extra.datasets`.

[![Current Release Version](https://img.shields.io/github/release/explosion/ml_datasets.svg?style=flat-square&logo=github)](https://github.com/explosion/ml_datasets/releases)
[![PyPi Version](https://img.shields.io/pypi/v/ml-datasets.svg?style=flat-square&logo=pypi&logoColor=white)](https://pypi.python.org/pypi/ml-datasets)

## Setup and installation

The package can be installed via pip:

```bash
pip install ml-datasets
```

## Loaders

Loaders can be imported directly or used via their string name (which is useful if they're set via command line arguments). Some loaders may take arguments – see the source of details.

```python
# Import directly
from ml_datasets import imdb
train_data, dev_data = imdb()
```

```python
# Load via registry
from ml_datasets import loaders
imdb_loader = loaders.get("imdb")
train_data, dev_data = imdb_loader()
```

### Available loaders

| ID / Function        | Description                                                 | From URL |
| -------------------- | ----------------------------------------------------------- | :------: |
| `imdb`               | IMDB sentiment dataset.                                     |    ✓     |
| `mnist`              | MNIST data.                                                 |    ✓     |
| `quora`              | Quora question answer dataset.                              |    ✓     |
| `reuters`            | Reuters dataset.                                            |    ✓     |
| `snli`               | Stanford Natural Language Inference corpus.                 |    ✓     |
| `stack_exchange`     | Stack Exchange dataset.                                     |          |
| `ud_ancora_pos_tags` | Universal Dependencies Spanish AnCora corpus (POS tagging). |    ✓     |
| `ud_ewtb_pos_tags`   | Universal Dependencies English EWT corpus (POS tagging).    |    ✓     |
| `wikiner`            | WikiNER data.                                               |          |