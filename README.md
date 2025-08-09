# Reddit Mental Health NLP

A Natural Language Processing (NLP) pipeline for analyzing mental health-related posts from Reddit.

## Features
- Configurable Transformer fine-tuning (default: BERT)
- Text preprocessing: cleaning, tokenization
- Evaluation: Accuracy, Precision, Recall, F1
- Inference for single text or CSV batch

## Structure
```
configs/        # YAML configs
data/           # Raw and processed datasets
src/            # Scripts: train, evaluate, infer, data utils
outputs/        # Checkpoints, reports
requirements.txt
README.md
```

## Installation
```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
```

## Usage

### Train
```bash
python -m src.train --config configs/base.yaml
```

### Evaluate
```bash
python -m src.evaluate --config configs/base.yaml --checkpoint path/to/best.ckpt --split test
```

### Inference
```bash
python -m src.infer --checkpoint path/to/best.ckpt --text "I feel anxious."
```

## License
MIT License.
