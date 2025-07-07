# 🧠 Conversational Agent App

A practical LLM-based conversational agent pipeline designed to demonstrate fine-tuning and real-time streaming inference using [Ludwig](https://ludwig.ai/), HuggingFace Transformers, and custom training data.

This repository includes Jupyter notebooks to:

* Fine-tune a base language model on your own conversational dataset.
* Deploy and run **streaming inference** for real-time agent responses.

---

## 📁 Repository Structure

| File/Notebook                                                                                                      | Description                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`SVCEAI Fine tuning - Inference Code.ipynb`](./SVCEAI%20Fine%20tuning%20-%20Inference%20Code.ipynb)               | This notebook handles **fine-tuning** a Hugging Face LLM (like `meta-llama/Llama-2-7b-hf`) using **Ludwig**. It defines a YAML config for model training and shows how to run predictions on custom input after training. |
| [`SVCEAI Streaming Response - Inference Code.ipynb`](./SVCEAI%20Streaming%20Response%20-%20Inference%20Code.ipynb) | This notebook sets up **token-wise streaming response generation** using the fine-tuned model. It leverages `AutoModelForCausalLM` and `generate()` with `stopping_criteria` to simulate chatbot-like interaction.        |

---

## 🛠️ Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/AishwaryaSubash/Conversational-Agent-App.git
   cd Conversational-Agent-App
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Install optional packages if needed:**

   ```bash
   pip install ludwig
   pip install transformers datasets
   ```

---

## 🚀 How to Use

### 1. Fine-Tune a Base Model

Open the notebook `SVCEAI Fine tuning - Inference Code.ipynb`:

* Define the **Ludwig config** for input/output features.
* Train on your custom data (structured in JSON/CSV with prompt-response pairs).
* Save and optionally evaluate your model.

### 2. Stream Responses from Fine-Tuned Model

Open `SVCEAI Streaming Response - Inference Code.ipynb`:

* Load your fine-tuned model checkpoint.
* Use token-wise generation with stopping criteria.
* Simulate live interaction with your conversational agent.

---

## 📊 Example Use Cases

* Building domain-specific chatbots
* Interactive academic tutors
* Real-time customer service agents

---

## 📌 Notes

* Uses **causal language modeling (CLM)** for training and inference.
* Fine-tuning can be done on local GPU or integrated with platforms like Colab or SageMaker.
* Works with models like **LLaMA**, **Mistral**, or other HuggingFace-compatible LLMs.

---

## 📃 License

MIT License — see [`LICENSE`](LICENSE) for details.
