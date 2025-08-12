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
```
/vlm-playground
├── app.py               # Gradio UI
├── vlm_utils.py         # BLIP & GIT models + classification logic
├── test_images/         # Sample images
├── vlm_results_ui.txt   # Log for single image mode
├── sample_results.csv   # Example batch output
└── README.md            # Project documentation
```

---

## ⚡ Quick Start (Google Colab)

1. **Open in Colab**  
  

2. **Install dependencies**:
```python
%pip install gradio pandas transformers torchvision timm accelerate Pillow
```

3. **Run the app**:
```python
import gradio as gr
# paste the app.py code here
```

4. **Click the public link** shown in Colab to access the app.

---

## 💻 Running Locally
```bash
git clone https://github.com/YOUR_USERNAME/vlm-playground.git
cd vlm-playground
pip install -r requirements.txt
python app.py
```
Open `http://127.0.0.1:7860` in your browser.

---

## 📊 Sample Output

| Image Name           | Caption                                      | Category | Agent Trace                          |
|----------------------|----------------------------------------------|----------|---------------------------------------|
| banana.jpg           | a photo of two bananas                       | Fruit    | BLIP > Classified: Fruit              |
| papaya.jpg           | a slice of papaya                            | Fruit    | BLIP > Classified: Fruit              |
| broccoli.jpg         | a photo of chopped broccoli                  | Vegetable| BLIP retry > Classified: Vegetable    |
| cinnamon.jpg         | a photo of cinnamon sticks and powder        | Spice    | BLIP > Classified: Spice              |

---
---

## 📌 Future Improvements
- Better classification with fuzzy matching for typos.
- Integration with other VLMs (SmolVLM, NanoVLM).
- Deployment on Jetson Nano for real-time camera captioning.

---

## 📜 License
MIT License. Author - Eby J Kavungal





