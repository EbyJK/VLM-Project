# 📷 Vision-Language Model Playground

An **interactive Vision-Language Model (VLM) playground** that:
- Generates captions for images using **BLIP** with a **GIT-VLM fallback**.
- Automatically classifies captions into categories (**Fruit**, **Vegetable**, **Spice**, **Dry Fruit**, **Pulse**, or **Unknown**).
- Works in **Single Image Mode** (real-time) and **Batch Mode** (ZIP → CSV).
- Shows the **Agentic AI flow trace** for transparency.

---

## 🚀 Features
- **Single Image Mode**: Upload one image → Get caption + category + agent trace instantly.
- **Batch Mode**: Upload a ZIP of images → Download a CSV with captions & categories.
- **Fallback Logic**: If BLIP outputs repetitive words or unclear captions, retry with better prompts or use GIT-VLM.
- **Simple Classification**: Keyword-based rules for assigning categories.
- **Agent Trace**: Shows which agent handled each step.

---

## 📂 Project Structure
/vlm-playground
├── app.py # Gradio UI
├── vlm_utils.py # BLIP & GIT models + classification logic
├── test_images/ # Sample images
├── vlm_results_ui.txt # Log for single image mode
├── sample_results.csv # Example batch output
└── README.md # Project documentation

## ⚡ Quick Start (Google Colab)

1. **Open in Colab**  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK)

2. **Install dependencies**:
```python
%pip install gradio pandas transformers torchvision timm accelerate Pillow

3. **Run the app**:

import gradio as gr


4. **Click the public link shown in Colab to access the app.**

## 💻 Running Locally

git clone https://github.com/YOUR_USERNAME/vlm-playground.git
cd vlm-playground
pip install -r requirements.txt
python app.py



