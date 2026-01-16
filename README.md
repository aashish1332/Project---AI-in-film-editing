AI in film editing
# 🎬 AI-Based Automated Film Editing for Social Media Reels

This project implements an **AI-assisted automated video editing pipeline** that converts raw video footage into **social media–ready short reels**.  
It focuses on **motion-based highlight detection** and automated post-processing such as transitions, aspect ratio adjustment, stabilization, and audio mixing.

The system is implemented as a **Python Jupyter Notebook pipeline**, designed for reliability, reproducibility, and easy debugging.

---

## 📌 Problem Overview

Creating short-form content for platforms like **Instagram Reels, YouTube Shorts, and TikTok** requires manually reviewing long videos, selecting highlights, applying transitions, and formatting videos for different aspect ratios.  
This process is **time-consuming and repetitive**.

This project aims to **automate these tasks** using computer vision techniques, reducing manual editing effort.

---

## 🎯 Project Objectives

- Automatically detect highlight segments from raw videos  
- Apply social media–specific video enhancements  
- Generate short, ready-to-upload reels  
- Reduce manual post-production time  

---

## 🧠 Approach & System Design

The project follows a **modular video-processing pipeline**:

1. **Video Input**  
   - User-provided video files (`.mp4`, `.mov`)

2. **Motion Analysis (OpenCV)**  
   - Frame extraction  
   - Grayscale conversion  
   - Gaussian blur  
   - Frame-to-frame difference calculation  
   - Motion score computation

3. **Highlight Selection**  
   - High-motion segments selected as highlights  
   - Fallback to random selection if needed

4. **Video Processing (MoviePy)**  
   - Clip extraction and concatenation  
   - Crossfade transitions  
   - Aspect ratio conversion (9:16, 16:9, 1:1)  
   - Color grading

5. **Optional Enhancements**
   - Video stabilization using VidStab  
   - Audio mixing (original audio + optional background music)

6. **Final Export**
   - Social media–ready video reel

---

## 🛠️ Tools & Technologies Used

- **Python**
- **Jupyter Notebook**
- **MoviePy** – video editing and audio handling  
- **OpenCV (cv2)** – motion detection and frame analysis  
- **VidStab** – video stabilization  

---

## 📊 Evaluation

The system is evaluated using **qualitative metrics**, as video quality is subjective.

**Evaluation Criteria:**
- Visual appeal  
- Highlight accuracy  
- Transition smoothness  
- Audio quality  

The generated reels are visually engaging and suitable for social media platforms, especially for videos with noticeable motion.

---

## ⚠️ Limitations

- Motion does not always represent contextual importance  
- No semantic understanding (speech, objects, or events)  
- Performance depends on input video quality  
- Notebook-based implementation (no web/app interface)

---

## 📚 Challenges & Learnings

- Multiple AI tools were tested, but none generated a fully working solution end-to-end  
- Frequent runtime and dependency issues occurred, especially in Google Colab  
- The project required creating **7–8 notebook versions** due to instability  
- Significant time was spent debugging AI-generated code  
- Initial plan for a web/app-based solution was reduced to a stable notebook pipeline  

**Key Learning:**  
AI tools are **assistive**, not autonomous. Strong debugging and modular design are essential for real-world AI systems.

---

## 🔮 Future Improvements

- Speech-to-text subtitles  
- Object and scene detection  
- Beat-synchronized editing  
- Web or GUI-based interface  
- GPU acceleration for faster processing  

---

## 🤖 AI Usage Disclosure

AI tools such as **ChatGPT** and **Gemini** were used for:
- Code suggestions  
- Debugging assistance  
- Documentation support  

All final code was **manually tested, debugged, and modified**.

---

## 📂 How to Run

1. Clone the repository  
2. Install required dependencies  
3. Open the Jupyter Notebook  
4. Run cells **top-to-bottom**  
5. Provide a video file path as input  

---

## 👤 Author

**Aashish Kumar**

---

## 📄 License

This project is for **academic and educational purposes only**.
