# Null-Shot Prompting: Rethinking Prompting Large Language Models With Hallucination

This repository contains the data and analysis for the paper "Null-Shot Prompting: Rethinking Prompting Large Language Models With Hallucination" accepted at [EMNLP 2024 (Main, long)](https://2024.emnlp.org/program/accepted_main_conference/).

For the main experiment code, please refer to the [code repository](https://github.com/Pittawat2542/null-shot-prompting/tree/main).

## Authors
Pittawat Taveekitworachai, Febri Abdullah, and Ruck Thawonmas

## Abstract

This paper investigates an interesting phenomenon where we observe performance increases in large language models (LLMs) when providing a prompt that causes and exploits hallucination. We propose null-shot prompting, a counter-intuitive approach where we deliberately instruct LLMs to reference a null, non-existent, section. We evaluate null-shot prompting across a variety of tasks, including arithmetic reasoning, commonsense reasoning, and reading comprehension. Notably, we observe a substantial increase in performance in arithmetic reasoning tasks for various models, with up to a 44.62% increase compared to a baseline in one model. Additional experiments on more complex mathematical problem-solving and hallucination detection benchmarks also reveal similar benefits from this approach. Furthermore, we explore the effects of combining reasoning, which typically mitigates hallucination, with hallucination within the prompt and find several cases of performance improvements. We hope this paper stimulates further interest, investigation, and discussion on how hallucination in prompts may not only affect LLMs but, in certain cases, enhance their performance.

## File structure
```
.
├── .gitignore # Git ignore file
├── analysis_code # Code used for analysis
│   ├── 1_result_compilation.ipynb
│   ├── 2_scaling_analysis.ipynb
│   ├── 3_1_ratio_analysis.ipynb
│   ├── 3_2_error_analysis.ipynb
│   ├── 3_3_non-hallucinated-examples.ipynb
│   ├── 4_stat_test.ipynb
│   ├── 5_hallucination_count.ipynb
│   └── utilities # Utility functions
├── analysis_results # Aggregated results obtained from the analysis code
├── logs # Logs from the experiments
└── zipped_files # Zipped results from the experiments, should be unzipped and renamed to `results` folder before running the analysis code
```

## Installation and Usage
0. Create a virtual environment (if needed):
```bash
conda create -n null-shot python=3.12
```
and activate it:
```bash
conda activate null-shot
```
1. For each Jupyter notebook in the `analysis_code` folder, run the code cells to reproduce the results.
