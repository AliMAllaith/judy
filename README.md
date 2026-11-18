# JUDY — Debate Evaluation & Analysis Dashboard

An interactive dashboard for exploring and evaluating AI-generated judgments of competitive debates. The project compares model predictions against human-provided ground truth and provides access to debate transcripts, model outputs, and experimental results.

## Overview

JUDY is designed to support the analysis of AI systems in debate evaluation. It brings together debate data, ground-truth decisions, and model-generated verdicts in one place.

The dashboard allows users to:

- Compare model predictions with ground-truth debate winners.
- Explore model performance across different experimental configurations.
- Examine verdicts, confidence scores, margins, and justifications.
- Inspect detailed ground-truth records.
- Browse debate transcripts and source JSON files.
- Compare the outputs of different language models.

## Dashboard

The project includes an interactive web dashboard that can be hosted using GitHub Pages.

**Live dashboard:**  
https://alimallaith.github.io/judy/

## Repository Structure

```text
judy/
│
├── index.html
├── README.md
├── detailed_ground_truth.csv
├── ground_truth.json
│
├── debates/
│   └── Debate transcript JSON files
│
├── outputs/
│   └── Model evaluation outputs
│
├── outputs_zeroshot/
│   └── Zero-shot experiment results
│
├── outputs_rag/
│   └── Retrieval-Augmented Generation results
│
├── outputs_pipeline/
│   └── Pipeline experiment results
│
└── outputs_length/
    └── Length-related experiment results
```

## Dataset

The repository contains debate data and ground-truth annotations.

### 1. Ground Truth JSON

`ground_truth.json` contains the reference debate outcomes used for evaluating model predictions.

### 2. Detailed Ground Truth CSV

`detailed_ground_truth.csv` provides additional information for 20 debates, including:

| Column | Description |
|---|---|
| # | Record number |
| YouTube URL | Link to the original debate video |
| البطولة | Tournament name |
| مستوى المناظرة | Debate stage or level |
| الموالاة | Proposition team |
| المعارصة | Opposition team |
| الفريق الفائز | Winning team |
| ID | Unique debate identifier |

The CSV preserves the original Arabic team names and tournament information.

### 3. Debate Transcripts

The `debates/` directory contains the debate transcript files used in the evaluation experiments.

## Experimental Configurations

The repository includes several experimental output directories:

| Directory | Description |
|---|---|
| `outputs/` | Main experiment outputs |
| `outputs_zeroshot/` | Zero-shot evaluation |
| `outputs_rag/` | Retrieval-Augmented Generation evaluation |
| `outputs_pipeline/` | Pipeline-based evaluation |
| `outputs_length/` | Length-related experiment outputs |

The experiment directories include results from different language models, such as:

- DeepSeek
- Gemma
- GPT-OSS
- Llama
- Qwen

Individual verdict files contain model-generated evaluation results, including predicted winners, confidence, margins, and justifications where available.

## Dashboard Features

### Performance Overview
- Overall evaluation metrics.
- Model accuracy comparisons.
- Winner distribution.
- Performance across experimental configurations.

### Ground Truth vs. Model Decisions
- Compare predicted winners against reference winners.
- Identify correct and incorrect predictions.
- Expand and collapse model justification snippets.

### Explore Source Data
- Browse ground-truth records.
- View detailed ground-truth CSV data.
- Inspect debate transcripts.
- Explore model-generated JSON outputs.

### Interface
- Dark and light themes.
- Interactive tables and charts.
- Search and filtering.
- JSON inspection and copying.

## Hosting with GitHub Pages

The dashboard is hosted using GitHub Pages.

To enable or update hosting:

1. Open the repository's **Settings**.
2. Navigate to **Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch.
5. Select the `/ (root)` directory.
6. Click **Save**.

The dashboard is available at:

https://alimallaith.github.io/judy/

## Updating the Dataset

To update the project:

1. Add or replace the relevant debate transcript files in `debates/`.
2. Update `ground_truth.json` when reference outcomes change.
3. Update `detailed_ground_truth.csv` when detailed annotations change.
4. Add new experiment results to the corresponding output directories.
5. Commit and push the changes to GitHub.

**Important:** The dashboard's data-loading implementation must reference the repository's current file paths. If new files or directories are added, ensure they are included in the dashboard's data index or loading logic.

## Purpose

The project aims to facilitate systematic evaluation of AI-based debate judgment by comparing model-generated decisions with reference outcomes and examining the reasoning provided by different language models.

It provides a structured environment for analyzing model performance, identifying disagreements, and exploring the relationship between debate content and automated judging decisions.

---

## License and Usage

Please refer to the repository's license and data-source permissions before redistributing the dataset, transcripts, or other materials.

