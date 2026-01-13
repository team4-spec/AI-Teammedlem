# EcoTrace AI: Technical Strategist Jo

## Project Overview

EcoTrace AI is a strategic platform designed to win the AI Awards 2026 by addressing environmental challenges through multimodal AI and gamification. This repository contains the implementation of **Jo**, a professional AI project assistant configured for technical strategy and project management.

---

## Installation

### 1. Environment Setup

Execute the following in the project root:

```powershell
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt

```

### 2. Network Requirements

**Critical:** Do not use school or restricted institutional networks for installation or execution. These environments often block required SSL certificates and API endpoints. Use a mobile hotspot or unrestricted private network.

---

## External Dependencies

Due to file size limits, AI models must be downloaded manually and placed in the `./models/` directory.

### ASR: Speech Recognition (SenseVoice)

* **Download:** [SenseVoice Model](https://github.com/k2-fsa/sherpa-onnx/releases/download/asr-models/sherpa-onnx-sense-voice-zh-en-ja-ko-yue-2024-07-17.tar.bz2)
* **Extraction Path:** `./models/sherpa-onnx-sense-voice-zh-en-ja-ko-yue-2024-07-17/`

### TTS: Speech Synthesis (Ryan Male Voice)

* **Download:** [Ryan TTS Model](https://www.google.com/search?q=https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-en_US-ryan-medium.tar.bz2)
* **Extraction Path:** `./models/vits-piper-en_US-ryan-medium/`

---

## Configuration

1. Rename `conf.yaml.example` to `conf.yaml`.
2. Insert a valid Gemini API key into the `llm_api_key` field under `gemini_llm`.
3. Verify the following file paths:
* **Live2D Registry:** `model_dict.json` must point to `/live2d-models/chitose/runtime/chitose.model3.json`.
* **Voice Assets:** `conf.yaml` must point to `./models/vits-piper-en_US-ryan-medium/en_US-ryan-medium.onnx`.



---

## Execution

Start the backend server:

```powershell
python run_server.py

```

Access the interface via web browser at `http://localhost:12393`.

---

**Would you like me to generate a clean `conf.yaml.example` that includes only the necessary sections for the jury to minimize configuration errors?**
