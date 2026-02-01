# MP_toxicology_RAG_extraction

**Two-column README: Windows vs Ubuntu/Linux**

> Note: GitHub Flavored Markdown supports inline HTML. Below are two options for a two-column layout.
> - **HTML table approach:** simple and broadly supported
> - **Side-by-side divs (requires GitHub to allow inline styles):** may not render identically across viewers

---

## Option 1 — HTML Table (recommended)

<table>
  <tr>
    <td valign="top" width="50%">

### 🪟 Windows Users (summary)

**Install Python 3.10.12** and create a virtual environment:

```bash
cd C:\\Users\\YourUsername\\Desktop\\MyProject
py -3.10 -m venv venv_3_10_12
venv_3_10_12\\Scripts\\activate
pip install openai faiss-cpu jsonschema pandas tqdm scipdf textacy
pip install jupyter ipykernel
python -m ipykernel install --user --name=venv_3_10_12 --display-name="Python (venv_3_10_12)"
jupyter notebook
```

- Use `deactivate` to leave the venv.

    </td>
    <td valign="top" width="50%">

### 🐧 Ubuntu / Linux Users (summary)

**Install Docker & run GROBID** (example):

```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
sudo usermod -aG docker $USER
docker run -t --rm --init -p 8070:8070 -p 8071:8071 grobid/grobid:0.6.2
```

- If needed, use `wsl hostname -I` on Windows to get WSL IP for `localhost` replacement.

    </td>
  </tr>
</table>

---

## Option 2 — Side-by-side divs (may be blocked by some renderers)

<div style="display:flex; gap:2rem; align-items:flex-start;">
  <div style="flex:1; min-width:280px;">
  ### 🪟 Windows Users
  - Steps: install python, create venv, activate, install deps, run jupyter.
  </div>
  <div style="flex:1; min-width:280px;">
  ### 🐧 Ubuntu / Linux Users
  - Steps: install docker, (optional) add user to docker group, run grobid container.
  </div>
</div>

---

### Which option to use?
- Use **Option 1 (HTML table)** for the best cross-viewer compatibility (works on GitHub web UI and many other renderers).
- Use **Option 2** only if you want a more responsive layout and are OK with slight rendering differences.

---

## Final notes

You can copy the relevant Windows / Ubuntu sections from the main README into either column layout.
