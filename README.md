# dsc180a-Checkpoint
# DSC 180A Q1 Capstone - AI in Drug Discovery

**Student:** Taranvir Chima  
**Email:** tchima@ucsd.edu  
**Mentor:** Murali Krishnam (Solix Technologies)  
**Domain:** AI Applications in Drug Discovery (B23)

## Project Overview

This project explores AI applications in drug discovery through hands-on analysis of medical dialogues and biomedical literature. We investigate how large language models can extract structured information from unstructured medical text and identify potential drug repurposing candidates.

## Repository Structure
```
.
├── week2_medical_dialogue.py    # Medical dialogue analysis with semlib
├── week3_pubmed_fetching.py     # PubMed literature mining
├── week2_semlib_results.csv     # Week 2 output
├── alzheimers_repurposing_abstracts.csv  # Week 3 output
└── README.md
```

## Week 2: Medical Dialogue Analysis

Analyzes patient-doctor conversations from the MTS-Dialog dataset to extract:
- Chief complaints
- Medications mentioned
- Diabetes mentions
- Lifestyle/diet/exercise discussions

**Research Question:** Do diabetes conversations mention diet, exercise, or lifestyle changes? What proportion discuss medication vs. lifestyle management?

### Setup

**Dependencies:**
```bash
py -m pip install pandas semlib
```

**Set API Key:**
```cmd
# Windows Command Prompt
set OPENAI_API_KEY=your-api-key-here

# Windows PowerShell
$env:OPENAI_API_KEY="your-api-key-here"

# Mac/Linux
export OPENAI_API_KEY="your-api-key-here"
```

**Run:**
```bash
py week2_medical_dialogue.py
```

**Note:** This code uses the OpenAI API via semlib. Running the full analysis (1201 conversations) costs approximately $5-6.

### Data

Download the MTS-Dialog dataset:
- Source: https://github.com/abachaa/MTS-Dialog
- File: `MTS-Dialog-TrainingSet.csv`
- Place in same directory as script

---

## Week 3: PubMed Literature Mining

Queries PubMed for abstracts related to Alzheimer's disease and drug repurposing using the NCBI E-utilities API.

### Setup

**Dependencies:**
```bash
py -m pip install biopython pandas
```

**Run:**
```bash
py week3_pubmed_fetching.py
```

**Note:** Update the email address in the script (line 13) to your own email before running.

### Output

Generates `alzheimers_repurposing_abstracts.csv` containing:
- PubMed IDs
- Article titles
- Abstracts
- Publication years

---

## Results Summary

### Week 2 Findings
- **Top 5 Medications:** [Will be filled after running]
- **Diabetes Conversations:** [Will be filled after running]
- **Lifestyle vs. Medication:** [Will be filled after running]

### Week 3 Findings
- Retrieved 50+ abstracts on Alzheimer's drug repurposing
- Prepared dataset for LLM-based analysis in future work

---

## Future Work

- Integrate semlib with PubMed abstracts for drug candidate extraction
- Validate findings against DrugBank database
- Explore ontology-grounded approaches for improved predictions

---

## References

- MTS-Dialog Dataset: https://github.com/abachaa/MTS-Dialog
- PubMed API: https://www.ncbi.nlm.nih.gov/home/develop/api/
- Semlib Documentation: https://semlib.anish.io/
