<h1 align="center">Hi 👋, I'm Aditya Yadav</h1>

<h3 align="center">
M.Tech in AI @ IIT Jodhpur |
Computer Vision • Visual SLAM • MLDL Ops • Deep Learning
</h3>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=0E75B6&center=true&vCenter=true&width=435&lines=M.Tech+AI+@+IIT+Jodhpur;Computer+Vision;Visual+SLAM;Deep+Learning" alt="Typing SVG" />
</p>

<p align="center"> 
  <img src="https://komarev.com/ghpvc/?username=yadityax&label=Profile%20views&color=FF5733&style=for-the-badge" alt="yadityax" /> 
</p>

---

## 🚀 About Me

- 🎓 M.Tech in Artificial Intelligence at IIT Jodhpur
- 🔬 Researching Computer Vision, Visual SLAM and 3D Scene Understanding
- 📚 Interested in Deep Learning, Representation Learning and Computer Vision
- 💻 Strong in Python, C++, PyTorch and OpenCV
- 🌱 Currently learning:
  - MASt3R-SLAM
  - VGGT
  - Foundation Models for Vision
  - 3D Gaussian Splatting
- 🧩 Solving Data Structures & Algorithms problems on LeetCode
- 🤝 Looking to collaborate on Computer Vision and AI projects
- 📫 How to reach me: **yaditya20x@gmail.com** or **m25csa001@iitj.ac.in**

---
### 🛠️ Languages and Tools

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,cpp,c,pytorch,tensorflow,sklearn,opencv,numpy,pandas,matplotlib,git,github,linux,docker,vscode,postgres,mysql,cmake&perline=9" />
  </a>
</p>

![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![W&B](https://img.shields.io/badge/W%26B-FFBE00?style=for-the-badge&logo=weightsandbiases&logoColor=black)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Eigen](https://img.shields.io/badge/Eigen-1F4E79?style=for-the-badge)

---

### 🔥 My GitHub Stats

<p align="center">
  <img src="https://streak-stats.demolab.com?user=yadityax&theme=radical&hide_border=true" alt="GitHub Streak" />
</p>

---

## 💻 Personal Projects

### 🖼️ Deep Image Matting with Searched Lightweight Backbones
**Computer Vision Course Project** | [GitHub](https://github.com/yadityax/Deep-Image-Matting-using-NAS) | [Live Demo](https://huggingface.co/spaces/m25csa001/matting-demo)

- Reimplemented **Deep Image Matting** (Xu et al., CVPR 2017) in **PyTorch**: a **VGG-16** encoder-decoder with max-pool unpooling plus a refinement network, trained on the real-image **AM-2k** dataset. The result was checked against the published baseline (SAD 6.4–6.5 vs 6.82).
- Replaced the VGG-16 encoder with lightweight backbones (**MobileNetV2/V3-Small, EfficientNet-B0, ShuffleNetV2**) using a **U-Net-style decoder**. Candidates were ranked by a fast **proxy-training search** on a holdout set, and the top two were fully trained.
- Built the full evaluation stack: **SAD, MSE, MAD, Gradient and Connectivity** errors following GCA-Matting, **FLOPs/params/latency** benchmarking, a **Pareto** analysis, and paired **bootstrap** confidence intervals.
- Exported the model to **ONNX** and deployed a serverless, in-browser demo with **ONNX Runtime Web** on **Hugging Face Spaces**. Images never leave the browser.

**Results (AM-2k test set, 200 images, native resolution)**
- EfficientNet-B0: **SAD 5.76**, 11.8% lower than the VGG-16 baseline (6.53)
- **30× fewer parameters** (4.3M vs 130.5M) and **23× fewer FLOPs** (8.0 vs 181.5 GFLOPs at 512×512)
- **6× lower CPU latency** on 2 threads (198 ms vs 1261 ms)
- MobileNetV2: SAD 6.17 with only 2.5M parameters and 7.5 GFLOPs

**Tech Stack:** PyTorch, torchvision, OpenCV, NumPy, SciPy, ONNX, ONNX Runtime Web, Gradio, Hugging Face Spaces, fvcore, Matplotlib

---

### 🚀 ResearchCopilot – Production-Grade AI Research Assistant
**MLOps Course Project** 

- Built a production-ready **Retrieval-Augmented Generation (RAG)** research assistant supporting **arXiv** and **Semantic Scholar** paper discovery.
- Developed a **FastAPI** backend with a **Streamlit** frontend and **ChromaDB** vector database, powered by **Qwen 3.5 (Ollama)** for local LLM inference.
- Implemented an end-to-end MLOps pipeline with **Docker Compose**, **MLflow** experiment tracking, **GitHub Actions** CI/CD, and **Kubernetes** manifests for scalable deployment.

**Tech Stack:** FastAPI, Streamlit, ChromaDB, PyTorch, Ollama, MLflow, Docker, GitHub Actions, Kubernetes, DVC

---
### 🛒 Market Basket Analysis
**ML Course Project**
- Built a recommendation system using **Apriori** and **FP-Growth** algorithms to discover association rules from retail transactions.
- Developed an interactive **Streamlit** dashboard for product recommendation and analysis.

**Tech Stack:** Python, Pandas, mlxtend, Streamlit

---

### ✍️ Handwriting Analysis for Personality Trait Detection
**BE Project** 

- Developed an automated handwriting analysis system that predicts personality traits using **machine learning** and **image processing** techniques.
- Extracted handwriting features including **pressure, zones, top margin, and letter size** using **OpenCV**.
- Built and optimized multiple ML models, with **Support Vector Machine (SVM)** achieving the best performance.

**Results**
- Pressure: **98%**
- Zones: **98%**
- Top Margin: **98%**
- Letter Size: **99%**

**Tech Stack:** Python, OpenCV, NumPy, Pandas, Scikit-learn

---

### 👤 Face Recognition System
**Internship Project**

- Developed a real-time face recognition system for secure access control and employee identification in control room environments.
- Conducted literature review, model development, and implementation using **CNN-based face recognition** techniques.
- Leveraged **MTCNN** for face detection and **FaceNet** embeddings for accurate recognition.

**Tech Stack:** TensorFlow, Keras, FaceNet, MTCNN, OpenCV, NumPy, Scikit-learn




### 🤝 Connect with me
<p align="center">
<a href="https://www.linkedin.com/in/aditya-yadav-646891215/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="Aditya Yadav LinkedIn" height="40" width="50" /></a>
<a href="https://leetcode.com/u/Anonymous_Light/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/leet-code.svg" alt="LeetCode" height="40" width="50" /></a>
</p>

---

<h3 align="center"></h3>

<p align="center">
  <i>"Turning ideas into intelligent systems through research and code."</i>
</p>
