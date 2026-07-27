# benchmarking-mllm-prompts-asd

**Benchmarking Prompting Strategies for General-Purpose multi-modal Language Models in Autism-Related Behavioral Feature Extraction**

This repository contains the evaluation framework, prompt templates, and results for assessing how different prompting strategies influence the ability of general-purpose vision-language models (VLMs) to detect and temporally localize autism-related self-stimulatory behaviors in naturalistic videos. 

It provides the data and methodology used to evaluate three state-of-the-art models (Qwen 3.7-Plus, Gemini 3.1 Pro, and Claude Opus 4.8) across three distinct prompting strategies:
1. **Baseline**: Standard instruction for detection and localization.
2. **Long**: Expanded instructions with detailed clinical definitions of the target behaviors.
3. **Chain-of-Thought (CoT)**: Structured reasoning prompts requiring step-by-step verification before final prediction.

## Repository Structure

* `prompts/`: Contains the exact text files for the Baseline, Long, and CoT prompts used to query the models.
* `results/`: Contains the comprehensive evaluation data in CSV format (`ssbd_results.csv` and `ssbd_plus_results.csv`), including video-level presence metrics (Precision, Recall, F1) and temporal localization metrics (Ground Truth Coverage, Predicted Purity).
* `figures/`: Contains the precision and recall scatterplots for both presence detection and temporal localization across the evaluated behaviors.

## Datasets

The evaluation uses two publicly available naturalistic video datasets:
* **SSBD** (Self-Stimulatory Behaviours in the Wild)
* **SSBD+** (Self-Stimulatory Behaviors Dataset Plus)

The models were evaluated on their ability to identify and temporally localize three specific behaviors: arm flapping, head banging, and spinning.

## Methods

See study workflow illustrating datasets, prompting strategies, multi-modal language models, and evaluation procedures below. 

<img width="1536" height="1024" alt="MethodsFig" src="https://github.com/user-attachments/assets/181cec68-4800-4cca-80cf-b7a5920da76f" />


## Usage 

The prompt templates in the `prompts/` directory can be used to replicate the evaluation or applied to new video datasets. The results data can be loaded using standard data analysis libraries (e.g., pandas) to reproduce the figures and statistical analyses discussed in the paper.

## Citation

*(need to add)*
