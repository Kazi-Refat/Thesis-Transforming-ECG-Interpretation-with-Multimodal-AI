# Transforming ECG Interpretation with Multimodal AI[cite: 1]

## Overview[cite: 1]
This repository contains the codebase and methodology for my undergraduate thesis, which introduces a novel multimodal vision-language framework designed to automate clinical report generation.[cite: 1] By integrating 12-lead ECG images with structured patient metadata, this system translates complex cardiological visual data into accurate, readable diagnostic text.[cite: 1]

---

### 📌 Note on Viewing the Notebooks
Sometimes GitHub fails to render Jupyter Notebook (`.ipynb`) files properly due to metadata issues, showing an "Invalid Notebook" error. However, the code and all cell outputs are completely intact. 

**How to view the code and outputs:**
* **Download:** You can download the `.ipynb` file and open it locally using Jupyter Notebook, VS Code, or upload it to Google Colab.
* **View Online:** Alternatively, you can copy the URL of the notebook and paste it into [nbviewer](https://nbviewer.jupyter.org/) to view the fully rendered code and graphs directly in your browser.

---

## Core Innovations[cite: 1]
* **Stochastic Lead Masking:** Implemented a custom training strategy that drops 4 to 6 text fields at a 94% probability.[cite: 1] This forces the model to visually ground its predictions on the actual waveform morphology rather than relying on shortcut textual learning.[cite: 1]
* **Zero-Cheating Evaluation:** System performance is rigorously benchmarked under strict, blank-lead testing configurations to ensure genuine visual understanding.[cite: 1]

## Model Architecture & Implementation[cite: 1]
* **MedGemma-4b-it Integration:** The initial pipeline was built and fine-tuned using MedGemma-4b-it.[cite: 1] Training was carefully optimized for Kaggle T4 GPUs by utilizing fp16 precision alongside 4-bit NF4 QLoRA, ensuring stable memory management and preventing hardware-specific implementation bottlenecks.[cite: 1]
* **Llama-3.2-11B-Vision Scaling:** The architecture was successfully scaled to Meta's Llama-3.2-11B-Vision-Instruct utilizing 16-bit LoRA and the Unsloth library on NVIDIA A100 infrastructure.[cite: 1]
* **Robust Inference Pipelines:** Engineered data processing loops that strictly handle 12-lead ECG inputs as PIL Image objects, preventing type-mismatch errors and ensuring highly stable, continuous model inference.[cite: 1]

## Performance Metrics[cite: 1]
Under rigorous, zero-cheating evaluation, the final architecture achieved:[cite: 1]
* **76.88%** TF-IDF Cosine Similarity index.[cite: 1]
* **54.79%** ROUGE-L F1 score.[cite: 1]

## Tech Stack[cite: 1]
* **Frameworks & Libraries:** PyTorch, Hugging Face Ecosystem, Unsloth.[cite: 1]
* **Core Domains:** Vision-Language Models (VLMs), Parameter-Efficient Fine-Tuning (PEFT), Multimodal AI.[cite: 1]
