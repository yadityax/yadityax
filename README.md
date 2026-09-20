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

# ResearchCopilot: Retrieval-Augmented Research Assistant with Adaptive Memory

MLOps course project. [GitHub](https://github.com/yadityax/ResearchCopilot) | [Live Demo](https://huggingface.co/spaces/m25csa001/ResearchCopilot)

A FastAPI backend for retrieval-augmented Q&A over research papers, with a Gradio frontend deployed on Hugging Face Spaces.

## Features

- **Ingestion**: pulls papers from arXiv, Semantic Scholar and uploaded PDFs (PyMuPDF with a pdfplumber fallback, section and equation detection). Pretrained MiniLM-L6-v2 embeddings are stored in ChromaDB.
- **Generation**: answers are produced by Qwen 3.5 (35B) served locally through Ollama, with source citations.
- **Retrieval**: LLM query rewriting uses conversation history to resolve short follow-ups. Named papers missing from the store are auto-ingested, and paper-specific and general searches are merged. Long answers and reports are generated across multiple continuation passes.
- **Adaptive memory**: conversation history is stored in DynamoDB with a semantic copy in ChromaDB. Retrieval is re-ranked with exponential interest decay (lambda = 0.05, about a 14-day half-life), and an explicit "forget topic" endpoint deletes semantically matching memories.
- **MLOps**: GitHub Actions CI (flake8 and 61 pytest tests) and CD that builds a Docker image, pushes it to DockerHub and deploys to a Kubernetes cluster with a smoke test, behind an autoscaler running 2-10 pods. Monitoring via Prometheus, Grafana and MLflow.

**Tech Stack:** FastAPI, Ollama (Qwen 3.5), sentence-transformers, ChromaDB, DynamoDB, PyMuPDF, Docker, Kubernetes, GitHub Actions, Prometheus, Grafana, MLflow, Gradio, Hugging Face Spaces


---

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

### 🛡️ Agentic Code Security Reviewer: Autonomous PR Security Review with Verified Auto-Fix
**Personal Project** | [GitHub](https://github.com/yadityax/Agentic-Code-Security-Reviewer)

- Built an autonomous **GitHub pull-request security reviewer**: a **FastAPI** webhook feeds a **LangGraph** workflow that orchestrates **Semgrep, CodeQL, Gitleaks, Trivy and Syft** in network-isolated **Docker** containers. LLM agents reach the tools only through a least-privilege, audited **MCP** server.
- An **LLM analyst** triages correlated findings and must cite real line numbers as evidence. A discovery pass finds logic flaws that scanners cannot see, such as missing access checks and weak token randomness.
- Designed a **verified-remediation loop**: guardrailed patch, then build, the project's tests (sandboxed, no network), security rescan and up to 3 retries. It ends in a **human-approved** fix PR on a restricted branch and never merges automatically.
- Hardened and shipped it: secret redaction, HMAC-verified webhooks, an audit trail in **PostgreSQL**, a **React/TypeScript** dashboard, **Docker Compose** deployment, **Prometheus/Grafana/OpenTelemetry** config, and 130+ tests including sandbox-isolation tests.
- Built a **28-case benchmark** (12 held-out cases, independent repeats, hidden exploit tests as an oracle) comparing LLM-only, scanner-only and agentic systems.

**Results (held-out split, synthetic benchmark)**
- False alarms on safe code: **25% → 0%** after LLM triage, with no true findings lost
- F1 **0.86**, or **0.94** with LLM discovery, vs 0.75 scanner-only and 0.81 LLM-only
- **67%** of confirmed findings fixed and verified automatically, and a hidden exploit test confirmed 3 of the 4 fixes it could check
- About **20 s** and **$0.0001** per review

**Tech Stack:** Python, FastAPI, LangGraph, MCP, Semgrep, CodeQL, Gitleaks, Trivy, Syft, PostgreSQL, Redis, Docker, React, TypeScript, Tailwind, Prometheus, Grafana, OpenTelemetry, pytest, Groq (gpt-oss)

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
