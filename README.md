
# EduGenAI: Text In. Learning Out. 📚🎬🧠 
# by Team Idea_2_Implement

Welcome to **EduGenAI**, an open-source AI-powered virtual tutor that transforms **textual learning material** into **personalized, engaging video lessons**, complete with **voiceovers**, **visual animations**, and **multilingual subtitles**!

---

## 🚀 What is EduGenAI?

**EduGenAI** is a modular, open-source platform designed to revolutionize education using the power of Generative AI. From generating study content to producing video explanations with human-like narration in multiple languages — **EduGenAI automates the full educational content pipeline**.

---

## 🧩 Key Modules & Their Purpose

### 1. Web Tutor Interface (Frontend)
**Location**: `/index.html + JavaScript`  
**Purpose**:  
- User selects **topic**, **difficulty level**, and describes **prior knowledge**
- Generates a **customized study guide** using Gemini LLM
- User-friendly form-based interface

**Tech Used**:  
- HTML + JS (vanilla)
- Backend integrated with a Flask/Streamlit app (via `/generate-study-guide`)

---

### 2. AI-Powered Script Solver (Backend: Streamlit App)
**Location**: `streamlit_math_solver.py`  
**Purpose**:  
- Uses **Gemini Pro** LLM to generate step-by-step solutions for user-provided **math problems**
- Outputs a clear, human-readable solution with explanations

**Tech Used**:  
- Streamlit UI
- Google Gemini API
- Python + dotenv for secure keys

---

### 3. Text-to-Video Generator
**Location**: `video_generation_pipeline.py`  
**Purpose**:  
- Converts long-form educational **text content** (e.g., a concept explanation) into a **30-second video**
- Steps:
  - **Script segmentation** (30 segments using NLTK)
  - **Video frames** generated using **Stable Diffusion text-to-video**
  - **Voiceover** using **Coqui TTS**
  - **Subtitles** generated via **Whisper ASR** & translated via **Bhashini**
  - **Final video** rendered with **FFmpeg**

**Tech Used**:  
- Hugging Face Diffusers (Text-to-Video)
- Coqui TTS
- Whisper (OpenAI) for speech & subtitle generation
- FFmpeg for video rendering
- Torch, NLTK, and more

---

## 🌍 Multilingual Magic

Thanks to **Bhashini (Indian Lang Translation API)** + **Whisper**, EduGenAI supports:
- 🎤 Hindi voiceover generation
- 📝 Accurate Devanagari subtitles
- 🌐 Easy extension to **regional Indian languages**

---

## 💡 Use Cases

- 📘 School/College Tutors
- 🧑‍🏫 Personalized Learning Assistants
- 🧠 Inclusive Learning for Multilingual Users
- 🎓 NGOs & EdTechs promoting scalable, localized learning

---

## ⚙️ How to Run Locally

```bash
# 1. Install requirements
pip install -r requirements.txt

# 2. Run Streamlit App for Tutor Interface & Math Solver
streamlit run streamlit_math_solver.py

# 3. Run Video Generator Script
python video_generation_pipeline.py
