# TruthfulVQA

This dataset is designed to evaluate the truthfulness and honesty of vision-language models.

## Usage

```python
from datasets import load_dataset

# Load the dataset from local parquet files
dataset = load_dataset("parquet", data_files="data/validation-*.parquet", split="validation")
```

## Description

TruthfulVQA contains the following categories of truthfulness challenges:

### 1. Information Hiding
- Visual Information Distortion
- Blurring / Low-Resolution Processing
- Concealed Features and Information Masking

### 2. Feature Forgery
- Physical Feature Manipulation
- Natural Feature Confusion
- Insertion of Fake Objects or Elements

### 3. Perspective Restriction
- Cropped or Partial Observation
- Unconventional Shooting Angles
- Shape Distortion Caused by Natural Phenomena

### 4. Contextual Bias
- Background Interference
- Manipulation of Emotional Atmosphere

### 5. Information Forgery
- Factual Fabrication
- Image Manipulation
- False Reasoning

### 6. Fictional Information
- Fabricated Flags and Maps
- Imaginary Species

### 7. Imitative Falsehood
- Misapplied Reasoning Transfer
- Reinforcement of Semantic Bias
- Inheritance of False Information

### 8. Eye Illusion
- Perceptual Multiplicity
- Optical Illusions

## Features

- question_id: Unique identifier for each question
- question: The question text
- image: The associated image
- options: Multiple-choice options
- answer: The correct answer for the multiple-choice question
- category: Main category of the truthfulness challenge
- subcategory: Specific type of truthfulness challenge
- level: Difficulty level of the question