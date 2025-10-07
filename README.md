## TruthfulVQA

> A Large-Scale Multimodal Truthfulness Benchmark

---

### Overview

TruthfulVQA is a large-scale multimodal truthfulness benchmark built with rigorous human-in-the-loop verification. It contains 5,000+ visually misleading images annotated by 50 professional annotators. Each sample is independently reviewed by five professionals to ensure robust and reliable evaluation.

We introduce a three-tier, human-authored prompt design that systematically probes models across increasing levels of reasoning complexity, enabling fine-grained diagnosis of hallucination and misinformation vulnerabilities in MLLMs.

---

### Table of Contents
- **Overview**
- **Quick Start**
- **Dataset Structure**
- **Data Fields**
- **Key Features**
- **Citation**

---

## Quick Start

```python
from datasets import load_dataset

# Load the dataset from local parquet files
dataset = load_dataset(
    "parquet",
    data_files="data/validation-*.parquet",
    split="validation",
)

# Peek a sample
sample = dataset[0]
print(sample["question"], sample["options"], sample["answer"])
```

---

## Dataset Structure

TruthfulVQA covers the following 8 categories and 21 subcategories of truthfulness challenges:

### Information Hiding
- Visual information distortion
- Blurring and low-resolution processing
- Feature concealment and information masking

### Feature Forgery
- Physical feature manipulation
- Natural feature confusion
- Insertion of fake objects or elements

### Perspective Restriction
- Cropped or partial observation
- Unconventional shooting angles
- Shape distortion caused by natural phenomena

### Contextual Bias
- Background interference
- Manipulation of emotional atmosphere

### Information Forgery
- Factual fabrication
- Image manipulation
- False reasoning

### Fictional Information
- Fabricated flags and maps
- Imaginary species

### Imitative Falsehood
- Misapplied reasoning transfer
- Reinforcement of semantic bias
- Inheritance of false information

### Eye Illusion
- Perceptual multiplicity
- Optical illusions

---

## Data Fields

| Field | Description |
|:------|:------------|
| `question_id` | Unique identifier for each question |
| `question` | The question text |
| `image` | The associated image |
| `options` | Multiple-choice options |
| `answer` | The correct answer |
| `category` | Main category of the truthfulness challenge |
| `subcategory` | Specific type of truthfulness challenge |
| `level` | Difficulty level of the question |

---

## Key Features

- **Rigorous Human Review**: High-quality data validated by professional annotators.
- **Multi-Level Reasoning**: Fine-grained model diagnosis across complexity tiers.
- **Real-World Scenarios**: Rich examples of visual misinformation.
