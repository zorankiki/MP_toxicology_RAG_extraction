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

**Important installation options:**
- ✅ Check **“Add python.exe to PATH”**
- Click **“Install Now”**
- Wait until installation completes

---

### Step 2: Create a Virtual Environment

1. Open **Command Prompt (CMD)** or **PowerShell**
2. Navigate to your project directory:
   ```bash
   cd C:\Users\YourUsername\Desktop\MyProject
   ```

3. (Optional) Verify available Python versions:
   ```bash
   py -0
   ```

4. Create the virtual environment:
   ```bash
   py -3.10 -m venv venv_3_10_12
   ```

---

### Step 3: Activate the Virtual Environment

```bash
venv_3_10_12\Scripts\activate
```

**Verification:**
- Your terminal prompt should now show:
  ```
  (venv_3_10_12)
  ```

This confirms the environment is active and isolated.

---

### Step 4: Install Dependencies

```bash
pip install openai faiss-cpu jsonschema pandas tqdm scipdf textacy
```

---

### Step 5: Install Jupyter & Register Kernel

1. Install Jupyter and ipykernel:
   ```bash
   pip install jupyter ipykernel
   ```

2. Register the environment as a Jupyter kernel:
   ```bash
   python -m ipykernel install --user --name=venv_3_10_12 --display-name="Python (venv_3_10_12)"
   ```

---

### Step 6: Launch Jupyter Notebook

```bash
jupyter notebook
```

**Inside Jupyter:**
- Create or open a notebook
- Navigate to **Kernel → Change kernel**
- Select **Python (venv_3_10_12)**

---

### Step 7: Verify Kernel Registration (Optional)

```bash
jupyter kernelspec list
```

Your new kernel should appear in the list.

---

### Step 8: Deactivate the Environment

When finished:

```bash
deactivate
```

---

## 🐧 Ubuntu / Linux Users

> ⚠️ Setup instructions are currently **incomplete**.

---

## 📎 Notes

- This repository is **not production-ready**
- Intended for **experimentation and demos**
- Dependencies and workflows may change

---

## 📄 License

*(Not specified)*
