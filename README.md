# 🦉 TruthfulVQA

> **A Large-Scale Multimodal Truthfulness Benchmark**

---

## 📢 Introduction

TruthfulVQA is the first large-scale multimodal truthfulness benchmark built with rigorous human-in-the-loop verification. We collected over 5,000 visually misleading images, annotated by 50 professional annotators, and—critically—each sample was independently reviewed by five professionals to ensure robust and reliable evaluation.

We propose a three-tier human-written prompt system that systematically probes models across increasing levels of reasoning complexity, enabling fine-grained diagnosis of hallucination and misinformation vulnerabilities in MLLMs.

---

## 🚀 Quick Start

```python
from datasets import load_dataset

# Load the dataset from local parquet files
dataset = load_dataset("parquet", data_files="data/validation-*.parquet", split="validation")
```

---

## 🧩 Dataset Structure

TruthfulVQA covers the following categories of truthfulness challenges:

<details>
<summary>1️⃣ Information Hiding</summary>

- 🖼️ Visual information distortion
- 🔍 Blurring / low-resolution processing
- 🕵️‍♂️ Feature concealment and information masking
</details>

<details>
<summary>2️⃣ Feature Forgery</summary>

- 🧑‍🎨 Physical feature manipulation
- 🦄 Natural feature confusion
- 🏗️ Insertion of fake objects or elements
</details>

<details>
<summary>3️⃣ Perspective Restriction</summary>

- ✂️ Cropped or partial observation
- 📐 Unconventional shooting angles
- 🌪️ Shape distortion caused by natural phenomena
</details>

<details>
<summary>4️⃣ Contextual Bias</summary>

- 🏞️ Background interference
- 🎭 Manipulation of emotional atmosphere
</details>

<details>
<summary>5️⃣ Information Forgery</summary>

- 📰 Factual fabrication
- 🖌️ Image manipulation
- 🧠 False reasoning
</details>

<details>
<summary>6️⃣ Fictional Information</summary>

- 🚩 Fabricated flags and maps
- 🐉 Imaginary species
</details>

<details>
<summary>7️⃣ Imitative Falsehood</summary>

- 🔄 Misapplied reasoning transfer
- 🧩 Reinforcement of semantic bias
- 🧬 Inheritance of false information
</details>

<details>
<summary>8️⃣ Eye Illusion</summary>

- 👀 Perceptual multiplicity
- 🌀 Optical illusions
</details>

---

## 📝 Data Fields

| Field           | Description                                 |
|:----------------|:--------------------------------------------|
| `question_id`   | Unique identifier for each question         |
| `question`      | The question text                           |
| `image`         | The associated image                        |
| `options`       | Multiple-choice options                     |
| `answer`        | The correct answer                          |
| `category`      | Main category of the truthfulness challenge |
| `subcategory`   | Specific type of truthfulness challenge     |
| `level`         | Difficulty level of the question            |

---

## 🌟 Highlights

- 🧑‍⚖️ Rigorous human review for high-quality data
- 🏆 Multi-level reasoning probes for fine-grained model diagnosis
- 🖼️ Rich real-world scenarios of visual misinformation

---

> 📬 For collaboration or questions, contact: truthfulvqa@163.com
