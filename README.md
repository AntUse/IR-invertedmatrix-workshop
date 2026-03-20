# 🛠️ IR Inverted Matrix Workshop
### PROG8245 — Information Retrieval | Active Learning Workshop

> **Course:** PROG8245 &nbsp;|&nbsp; **Submission subject:** `PROG8245 - Inverted Matrix Workshop, Team #_____`

---

## 👥 Team Members

| Name | GitHub |
|------|--------|
| Team Member 1 | ANTHONY IZEVBOKUN |
| Team Member 2 | PREEJA ANILAL |
| Team Member 3 | MINH THUAN TROUNG |

> Replace the placeholders above with your actual names and GitHub usernames before submitting.

---

## 📄 Dataset Description

**Source:** Python Software Foundation (PSF) Blog — Public RSS Feed  
**Format:** Plain text (`.txt`), one file per blog post, auto-saved to `sample_docs/`  
**Collection method:** Fetched programmatically using the `feedparser` library from the PSF's public RSS endpoint  
**Corpus size:** 20 documents  
**Vocabulary:** 2,000+ unique tokens after tokenisation and normalisation  

### Content Overview

The corpus consists of official blog posts published by the Python Software Foundation, covering:

- Python version releases and security patch announcements
- PSF governance updates, grants, and community programs
- PyCon event announcements and recaps
- Open source funding and sponsorship news
- Developer community initiatives

Each document is stored as a `.txt` file with the post title on the first line followed by the post summary body. The full NLP pipeline applied to each document is:

1. **Tokenisation** — lowercase conversion + regex-based punctuation removal
2. **Normalisation** — NLTK English stop-word removal + Porter Stemming
3. **Inverted Index** — term → set of doc IDs
4. **Positional Index** — term → {doc_id → [positions]} (standard + memory-optimised)
5. **TF & IDF scoring** — raw Term Frequency and log-weighted Inverse Document Frequency

---

## 🔗 Dataset Link & License

| Field | Details |
|-------|---------|
| **RSS Feed** | https://pyfound.blogspot.com/feeds/posts/default?alt=rss |
| **Blog** | https://pyfound.blogspot.com |
| **Publisher** | Python Software Foundation (PSF) |
| **License** | [Creative Commons Attribution 4.0 International — CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| **Access** | Publicly available — no authentication required |

> Attribution must be given to the **Python Software Foundation** when reproducing or distributing content derived from this corpus.

---

## 🗂️ Repository Structure

```
IR-invertedmatrix-workshop/
│
├── IR_InvertedMatrix_Workshop.ipynb   # Main notebook — all tasks, solutions & challenges
├── README.md                          # This file
├── requirements.txt                   # Python dependencies
└── sample_docs/                       # Auto-generated at runtime by the first notebook cell
    ├── blog_1.txt
    ├── blog_2.txt
    └── ...
```

---

## ⚙️ Setup — Virtual Environment & Dependencies

Follow these steps to run the notebook locally in VS Code with a clean, isolated Python environment.

### 1. Clone the Repository

```bash
git clone https://github.com/AntUse/IR-invertedmatrix-workshop.git
cd IR-invertedmatrix-workshop
```

### 2. Create a Virtual Environment

**macOS / Linux:**
```bash
python3 -m venv .venv
```

**Windows (Command Prompt):**
```cmd
python -m venv .venv
```

### 3. Activate the Virtual Environment

**macOS / Linux:**
```bash
source .venv/bin/activate
```

**Windows (Command Prompt):**
```cmd
.venv\Scripts\activate
```

**Windows (PowerShell):**
```powershell
.venv\Scripts\Activate.ps1
```

> You should see `(.venv)` appear at the start of your terminal prompt once activated.

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install feedparser nltk requests
```

### 5. Download NLTK Data

Run this once in a Python shell or at the top of the notebook:

```python
import nltk
nltk.download('stopwords')
```

### 6. Open the Notebook in VS Code

1. Open VS Code in the project folder:
   ```bash
   code .
   ```
2. Open `IR_InvertedMatrix_Workshop.ipynb`
3. In the top-right kernel selector, click **Select Kernel → Python Environments → `.venv`**
4. Run all cells from top to bottom (**Run All** or `Shift+Enter` per cell)

> The `sample_docs/` folder will be created automatically by the first code cell.

### Deactivate the Virtual Environment (when done)

```bash
deactivate
```

---

---

## ✅ Workshop Tasks Completed

| # | Task | Status |
|---|------|--------|
| 1 | Document Collection — 20 PSF blog posts via RSS | ✅ |
| 2 | Tokenizer — lowercase + regex punctuation removal | ✅ |
| 3 | Normalisation Pipeline — NLTK stop-words + Porter Stemming | ✅ |
| 4 | Inverted Index construction | ✅ |
| — | Phrase Queries — 2 queries using positional merge algorithm | ✅ |
| C1 | Positional Index + TF/IDF comparison table + bigram talking point | ✅ |
| C2 | Memory-optimised Positional Index using `array.array` | ✅ |
| C3 | IDF implementation with top-10 rarest terms display | ✅ |
| C4 | TF implementation + full TF-IDF scoring table | ✅ |

---

## 📬 Submission

Email the instructor with:
- **Subject:** `PROG8245 - Inverted Matrix Workshop, Team #_____`
- **Body:** `.git` links to every team member's GitHub repo (one email per team)
