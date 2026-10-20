# brainai — Connect AI

Connect AI is an open-source Jupyter notebook project for giving a small open model long-term memory of a one-person company's own knowledge.

Using Unsloth, the notebook fine-tunes Qwen2.5-3B-Instruct with LoRA / SFT on a curated Q&A dataset of business knowledge (synced in this repo as `connect-ai/knowledge.json`, loaded at runtime from the maintainer's Hugging Face dataset), and exports both safetensors and GGUF builds so the resulting model can run locally inside an app.

## Contents
- `connect-ai/train-sft.ipynb` — the full training notebook: dataset formatting, response-only training, loss checks, model testing, and GGUF export. Runs on a free Colab T4 GPU.
- `connect-ai/knowledge.json` — the synced knowledge entries used to build the training data.

## Who this is for
Solo founders and non-ML practitioners who want an AI that knows their own business — a reproducible, low-cost, end-to-end fine-tuning recipe you can fork and rerun with your own knowledge and your own Hugging Face account.

## License
MIT — see `LICENSE`.
