# MP_toxicology_RAG_extraction

**MP_toxicology_RAG_extraction** is a demo project for **RAG-based (Retrieval-Augmented Generation) information extraction** from **scientific studies on microplastics**, with a focus on toxicology-related content.

---

## 📌 Project Overview

- **Domain:** Scientific literature / Toxicology / Microplastics  
- **Goal:** Demonstrate information extraction using **RAG pipelines**  
- **Status:** Demo / Experimental  

> ⚠️ This repository is intended as a **proof-of-concept** and may contain incomplete or evolving components.

---

## 🚀 How to Run the Demo

### Requirements

- **Python version:** **Python 3.10.12**

---

## 🪟 Windows Users

### Step 1: Install Python 3.10.12

- Download **Python 3.10.12** from the official Python for Windows website
- Select the appropriate installer (64-bit recommended)
- Ensure **“Add python.exe to PATH”** is checked

---

### Step 2: Create a Virtual Environment

```bash
cd C:\Users\YourUsername\Desktop\MyProject
py -3.10 -m venv venv_3_10_12
```

---

### Step 3: Activate the Virtual Environment

```bash
venv_3_10_12\Scripts\activate
```

---

### Step 4: Install Dependencies

```bash
pip install openai faiss-cpu jsonschema pandas tqdm scipdf textacy
```

---

### Step 5: Install Jupyter & Register Kernel

```bash
pip install jupyter ipykernel
python -m ipykernel install --user --name=venv_3_10_12 --display-name="Python (venv_3_10_12)"
```

---

### Step 6: Launch Jupyter Notebook

```bash
jupyter notebook
```

---

### Step 7: Deactivate the Environment

```bash
deactivate
```

---

## 🐧 Ubuntu / Linux Users

> ⚠️ Setup instructions are currently **incomplete**.

---

## 📎 Notes

- Demo / proof-of-concept repository
- Not production-ready

---

## 🐳 Running GROBID (Docker – Windows)

To run **GROBID 0.6.2** on **Windows**, using **Docker Desktop** is the most reliable approach, as it provides the required Linux-native environment.

---

### Step 1: Install Docker Desktop on Windows

- Download and run **Docker Desktop Installer.exe**
- During setup, select **“Use WSL 2 instead of Hyper-V”**
- Restart if prompted and launch Docker Desktop

---

### Step 2: Pull and Run GROBID 0.6.2

```powershell
docker run -t --rm --init -p 8070:8070 -p 8071:8071 grobid/grobid:0.6.2
```

**Command breakdown:**

- `-t` — Allocates a pseudo-terminal  
- `--rm` — Removes the container after stopping  
- `--init` — Handles system signals correctly  
- `-p 8070:8070` — Main service port  
- `-p 8071:8071` — Admin / health-check port  

---

### Step 3: Access the Service

- **Main Interface:** http://localhost:8070  
- **Health Check:** http://localhost:8071  

---

### 🪟 Windows-Specific Tip

If `localhost` does not work due to WSL networking:

```powershell
wsl hostname -I
```

Use the returned IP address instead of `localhost`.
