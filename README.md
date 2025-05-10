# LLM Text Summarization Comparison

This repository contains a comparative study on abstractive text summarization using Large Language Models (LLMs). The project explores the performance of different LLMs and text generation (decoding) strategies on a standard summarization dataset, evaluated using common metrics.

## Project Goal

The main objective is to experiment with various LLMs and decoding methods for text summarization and analyze their impact on the quality of generated summaries.

## Dataset

The project utilizes the **CNN / DailyMail dataset** for abstractive summarization.
[Dataset Link on Hugging Face](https://huggingface.co/datasets/abisee/cnn_dailymail)

## Models Explored

The following pre-trained Large Language Models are used:

- **BART Large CNN** (`facebook/bart-large-cnn`): A sequence-to-sequence model fine-tuned for summarization.
- **T5 Small** (`t5-small`): A smaller, general-purpose text-to-text transformer model.

## Decoding Strategies

Different text generation (decoding) approaches are compared:

- **Greedy Search:** Selects the token with the highest probability at each step.
- **Beam Search:** Explores multiple likely sequences (`num_beams=4` used).
- **Sampling:** Introduces randomness (`top_k=50`, `temperature=0.7` used).

## Evaluation Metrics

The quality of generated summaries is evaluated quantitatively using standard metrics:

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):** ROUGE-1 (unigrams), ROUGE-2 (bigrams), and ROUGE-L (longest common subsequence) F1 scores.
- **BLEU (Bilingual Evaluation Understudy):** Measures n-gram precision (corpus BLEU score calculated on a single example for comparison).

## Code

The experiments and analysis are documented in a Jupyter notebook/Colab notebook.

- `summarization_experiment.ipynb` (or similar name, corresponding to your Colab file)

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YourUsername/llm-text-summarization-comparison.git
    cd llm-text-summarization-comparison
    ```
2.  **Install dependencies:** Make sure you have Python installed. Install the required libraries using pip:
    ```bash
    pip install -q transformers datasets rouge_score sacrebleu torch pandas
    ```
3.  **Open and run the notebook:** Open the `summarization_experiment.ipynb` file in Google Colab or a local Jupyter environment. Run the cells sequentially to load the data, models, generate summaries, compute metrics, and view the results.

## Results (Example Run on One Article)

Below is the results table generated from running the notebook on a single example article from the test set. Note that a full evaluation would typically run on a larger subset of the dataset.

Yunus Emre Gültepe
