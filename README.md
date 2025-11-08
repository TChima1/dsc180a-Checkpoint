# DSC 180A Capstone - AI in Drug Discovery

This project explores AI applications in drug discovery through analysis of medical dialogues and biomedical literature using large language models.
 
**Mentor:** Murali Krishnam, Dr. Justin Eldridge , Murali Krishnam

---


- `week2_medical_dialogue.py` - Analyzes patient-doctor conversations from MTS-Dialog
- `week3_pubmed_repurposing.py` - Extracts drug repurposing candidates from PubMed abstracts

---

## Setup

### 1. Clone repository
```bash
git clone https://github.com/TChima1/dsc180a-Checkpoint.git
cd dsc180a-Checkpoint
```

### 2. Install dependencies
```bash
py -m pip install pandas semlib biopython
```

**What each package does:**
- `pandas` - Data manipulation and CSV handling
- `semlib` - LLM-based semantic extraction framework
- `biopython` - PubMed API access

### 3. Set environment variables

**Windows Command Prompt:**
```cmd
set OPENAI_API_KEY=your-api-key-here
```

**Windows PowerShell:**
```powershell
$env:OPENAI_API_KEY="your-api-key-here"
```

**Mac/Linux:**
```bash
export OPENAI_API_KEY="your-api-key-here"
```

---



### Medical Dialogue Analysis

Analyzes 1,201 patient-doctor conversations from the MTS-Dialog dataset.

**Data Source:** Downloads automatically from https://github.com/abachaa/MTS-Dialog  
(Or manually download `MTS-Dialog-TrainingSet.csv` and place in project directory)

**Run:**
```bash
py week2_medical_dialogue.py
```



---

### PubMed Literature Mining

Retrieves 50 PubMed abstracts on Alzheimer's drug repurposing.

**Before running:** Update `Entrez.email` in script (line 18) to your email address:
```python
Entrez.email = "youremail@ucsd.edu"  # Required by NCBI
```

**Run:**
```bash
py week3_pubmed_repurposing.py
```



## Reproducibility

To reproduce results:

1. **Clone repository**
```bash
   git clone https://github.com/TChima1/dsc180a-Checkpoint.git
   cd dsc180a-Checkpoint
```

2. **Install dependencies**
```bash
   py -m pip install pandas semlib biopython
```

3. **Set API key**
```bash
   set OPENAI_API_KEY=your-api-key-here
```

4. **Update email in Week 3** (line 18)
```python
   Entrez.email = "youremail@ucsd.edu"
```

5. **Run scripts**
```bash
   py week2_medical_dialogue.py
   py week3_pubmed_repurposing.py
```

---

