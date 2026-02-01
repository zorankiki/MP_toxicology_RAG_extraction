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

Below are side-by-side, full instructions for **Windows** (left column) and **Ubuntu 22.04** (right column). Pick the column that matches your OS.

<table>
  <tr>
    <td valign="top" width="50%">

### 🪟 Windows Users

#### Requirements
- **Python version:** **Python 3.10.12**

---

#### Step 1: Install Python 3.10.12
- Download **Python 3.10.12** from the official Python for Windows website. Choose the 64-bit installer.
- During installation **check** **“Add python.exe to PATH”** and click **Install Now**.

---

#### Step 2: Create a Virtual Environment
Open **Command Prompt** or **PowerShell** and run:
```powershell
cd C:\Users\YourUsername\Desktop\MyProject
py -3.10 -m venv venv_3_10_12
```

---

#### Step 3: Activate the Virtual Environment
```powershell
venv_3_10_12\Scripts\activate
```

---

#### Step 4: Install Dependencies
```powershell
pip install openai faiss-cpu jsonschema pandas tqdm scipdf textacy
```

---

#### Step 5: Install Jupyter & Register Kernel
```powershell
pip install jupyter ipykernel
python -m ipykernel install --user --name=venv_3_10_12 --display-name="Python (venv_3_10_12)"
```

---

#### Step 6: Launch Jupyter Notebook
```powershell
jupyter notebook
```

---

#### Step 7: Deactivate the Environment
```powershell
deactivate
```

---

## 🐳 Running GROBID (Docker – Windows)

To run **GROBID 0.6.2** on **Windows**, using **Docker Desktop** is the most reliable approach.

**Step 1: Install Docker Desktop on Windows**
- Download and run **Docker Desktop Installer.exe**.
- During setup, select **“Use WSL 2 instead of Hyper-V”**.
- Restart if prompted and launch Docker Desktop.

**Step 2: Pull and Run GROBID 0.6.2**
```powershell
docker run -t --rm --init -p 8070:8070 -p 8071:8071 grobid/grobid:0.6.2
```

**Access the Service**
- **Main Interface:** http://localhost:8070  
- **Health Check:** http://localhost:8071

**Windows WSL Tip:** If `localhost` does not work, run:
```powershell
wsl hostname -I
```
Use the returned IP address instead of `localhost`.

    </td>
    <td valign="top" width="50%">

### 🐧 Ubuntu 22.04 Users

#### Requirements
- **OS:** Ubuntu **22.04 LTS** (tested)
- **Python version:** **Python 3.10.12** (or system Python 3.x)

---

#### Step 1: Install Python 3.10.12 (if not present)
Ubuntu 22.04 ships with Python 3.10; to ensure you have 3.10.12 you can use the deadsnakes PPA or install from source. Quick install using apt (system python):
```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip
```
If you need exactly **3.10.12** and it is not in your distro packages, consider using **pyenv** or building from source.

---

#### Step 2: Create a Virtual Environment
```bash
cd ~/projects/myproject
python3 -m venv venv_3_10_12
```

---

#### Step 3: Activate the Virtual Environment
```bash
source venv_3_10_12/bin/activate
```

---

#### Step 4: Install Dependencies
```bash
pip install --upgrade pip
pip install openai faiss-cpu jsonschema pandas tqdm scipdf textacy
```

> Note: `faiss-cpu` on Linux may require additional system packages (build tools). If `pip` install fails, refer to FAISS installation docs or install via conda.

---

#### Step 5: Install Jupyter & Register Kernel
```bash
pip install jupyter ipykernel
python -m ipykernel install --user --name=venv_3_10_12 --display-name="Python (venv_3_10_12)"
```

---

#### Step 6: Launch Jupyter Notebook
```bash
jupyter notebook --no-browser --ip=0.0.0.0
# open the provided URL in your local browser or use SSH port forwarding if remote
```

---

#### Step 7: Deactivate the Environment
```bash
deactivate
```

---

## 🐳 Running GROBID (Docker – Ubuntu 22.04)

To run **GROBID 0.6.2** on **Ubuntu 22.04**, install Docker Engine (instructions below) and run the official container.

**Install Docker (Ubuntu 22.04)**:
```bash
sudo apt update
sudo apt install -y ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
# (Optional) Add your user to the docker group:
sudo usermod -aG docker $USER
# log out / log in again for group changes to apply
```

**Pull and Run GROBID 0.6.2**:
```bash
docker run -t --rm --init -p 8070:8070 -p 8071:8071 grobid/grobid:0.6.2
```

**Access the Service**
- **Main Interface:** http://localhost:8070  
- **Health Check:** http://localhost:8071

**Ubuntu Tip:** If running on a remote server, ensure firewall allows incoming traffic on ports **8070** and **8071** (e.g., `ufw allow 8070` `ufw allow 8071`).

    </td>
  </tr>
</table>

---

## 📎 Notes

- This repository is a **demo / proof-of-concept** and **not production-ready**.  
- If you make changes to environment commands, please test them on the target OS/version before committing.
- For exact Python patch-level installs consider using **pyenv** or containerized environments.

---

## 📄 License

*(Not specified)*
