# Locate Anything Server

Python FastAPI backend that runs the LocateAnything vision-language model on a local GPU and returns bounding boxes or points for a natural-language prompt.

## Stack

- **Backend:** Python 3.12+, FastAPI, Uvicorn
- **Model:** nvidia/LocateAnything-3B (Hugging Face)
- **Runtime:** PyTorch CUDA

## Features

- Natural-language object localization API
- GPU worker process for model inference
- Automatic model download on first request

## Requirements

- NVIDIA GPU with roughly 8 GB+ VRAM
- CUDA 12.x driver
- ~7 GB disk for model weights

## Quick start

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000
```

API docs: http://localhost:8000/docs

## Author

Pooja Sharma — [Pooja101117](https://github.com/Pooja101117)
