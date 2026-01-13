---

# EcoTrace AI: Technical Strategist Jo

## Project Overview

EcoTrace AI is a strategic platform designed to address environmental challenges through multimodal AI and gamification. This repository contains the implementation of **Jo**, a professional AI project assistant configured for technical strategy and project management.

---

## 1. Prerequisites

Ensure the following base software is installed before proceeding:

* **Python 3.11+**: [Download Python](https://www.python.org/downloads/) (Ensure "Add Python to PATH" is checked during installation).
* **Git**: [Download Git](https://www.google.com/search?q=https://git-scm.com/downloads) (Required to clone the repository).
* **Google API Key**: Obtain from [Google AI Studio](https://aistudio.google.com/).

---

## 2. Installation and Environment

### Environment Setup

Execute the following in the project root to install all Python dependencies:

```powershell
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt

```

### Network Requirements

**Critical:** Do not use school, corporate, or restricted institutional networks for installation. These environments often block required SSL certificates and API endpoints. Use a mobile hotspot or unrestricted private network.

---

## 3. External AI Models

Download the following models and place them in the `./models/` directory.

### ASR: Speech Recognition (SenseVoice)

* **Download:** [SenseVoice Model Archive](https://github.com/k2-fsa/sherpa-onnx/releases/download/asr-models/sherpa-onnx-sense-voice-zh-en-ja-ko-yue-2024-07-17.tar.bz2)
* **Extraction Path:** `./models/sherpa-onnx-sense-voice-zh-en-ja-ko-yue-2024-07-17/`

### TTS: Speech Synthesis (Ryan Male Voice)

* **Download:** [Ryan TTS Model Archive](https://www.google.com/search?q=https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-en_US-ryan-medium.tar.bz2)
* **Extraction Path:** `./models/vits-piper-en_US-ryan-medium/`

---

## 4. Configuration

1. Rename `conf.yaml.example` to `conf.yaml`.
2. Insert a valid Gemini API key into the `llm_api_key` field under `gemini_llm`.
3. Verify file paths:
* **Live2D Registry:** `model_dict.json` must point to `/live2d-models/chitose/runtime/chitose.model3.json`.
* **Voice Assets:** `conf.yaml` must point to `./models/vits-piper-en_US-ryan-medium/en_US-ryan-medium.onnx`.



---

## 5. Execution

Start the backend server:

```powershell
python run_server.py

```

Access the interface via web browser at `http://localhost:12393`.
