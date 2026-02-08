# 🛡️ PolicyGuard — Local LLM Powered Policy Gap Analyzer  
### HackIITK 2k26 | Problem Statement 1

> **Offline Policy Gap Analysis and Improvement Module using a Local LLM**

---

## 📌 Problem Statement

Organizational cybersecurity policies are foundational governance documents. However, many real-world policies suffer from **incomplete coverage, vague controls, and missing alignment with industry standards** such as the **NIST Cybersecurity Framework**.

The objective of this project is to **analyze existing organizational policy documents**, identify gaps by benchmarking them against recognized frameworks, and **suggest improved policy revisions and a roadmap for enhancement** — all while operating **entirely offline using a lightweight local LLM**, as mandated by the problem statement.

---

## 🎯 Objective

- Identify **policy gaps and deficiencies**
- Benchmark policies against:
  - **CIS MS-ISAC NIST Cybersecurity Framework Policy Template Guide (2024)**
- Revise existing policies to:
  - Address identified gaps
  - Align with NIST Cybersecurity Framework
- Ensure **100% offline execution** using a **locally hosted lightweight LLM**

---

## 🔒 Key Constraints (Strictly Followed)

✅ Fully **offline execution**  
✅ **Local LLM only** (no cloud models)  
✅ **No external APIs**  
✅ **No internet dependency**  
✅ Lightweight and locally deployable architecture  

---

## 🧠 Solution Overview

**PolicyGuard** is a modular Python-based system that:

1. Accepts an organizational policy document as input
2. Parses and structures the policy text
3. Compares it against reference controls derived from the  
   **CIS MS-ISAC NIST Cybersecurity Framework Policy Template (2024)**
4. Identifies:
   - Missing sections
   - Incomplete controls
   - Weak or vague statements
5. Uses a **local LLM** to:
   - Suggest policy improvements
   - Rewrite deficient sections
   - Generate a **policy improvement roadmap**

All computation happens **locally**, ensuring data privacy and compliance.

---

## 🔄 High-Level Workflow

1. Policy Document  
2. Policy Reader  
3. Gap Detection Engine  
4. Local LLM Analysis  
5. Rewritten Policy + Improvement Roadmap  
6. Offline Output Reports  
---

## 📁 Project Structure

```text
PolicyGuard-PS1/
├── app.py              # Streamlit UI
├── main.py             # CLI execution logic
├── policy_reader.py    # Policy parsing
├── gap_detector.py     # Gap identification
├── llm_rewriter.py     # Local LLM rewriting
├── test_llm.py         # LLM testing
├── sample_policy.txt   # Test policy
├── outputs/            # Generated reports
├── assets/             # Screenshots
├── .gitignore
└── README.md
```
---

## 📊 Test Data (As Required)

Dummy organizational policies are created for validation across:

- Information Security Management System (ISMS)
- Data Privacy & Security
- Patch Management
- Risk Management

These policies simulate real-world incomplete policy documents and are used to evaluate the effectiveness of the gap analysis and revision process.

---

## 📚 Reference Framework

Gap analysis and alignment are based on:

**CIS MS-ISAC NIST Cybersecurity Framework  
Policy Template Guide (2024)**

This document serves as the **baseline reference** for identifying missing or weak policy controls.

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Rajpatel2924/PolicyGuard.git
cd PolicyGuard
```
### 2️⃣ Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows
```
### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
⚠️ Ensure the selected local LLM is properly installed and configured on the system.

### ▶️ How to Run
```bash
# Run Full Policy Analysis
python main.py --policy sample_policy.txt
```
## 📤 Output

The system generates the following artifacts:

- ⭐ **Identified policy gaps**
- ⭐ **Revised policy text**
- ⭐ **Improvement roadmap aligned with NIST CSF**
- ⭐ **Stored in the `outputs/` directory**

---

## 🧪 Testing

Validate LLM behavior and gap detection logic by running:

```bash
python test_llm.py

```
## 📦 Deliverables Mapping (PS Compliance)
| PS Requirement     | Implementation          |
| ------------------ | ----------------------- |
| Offline LLM        | ✅ Local lightweight LLM |
| No External APIs   | ✅ Zero API usage        |
| Gap Identification | ✅ `gap_detector.py`     |
| Policy Revision    | ✅ `llm_rewriter.py`     |
| Roadmap Generation | ✅ Included in outputs   |
| Documentation      | ✅ This README           |

## ⚠️ Limitations

- Quality of suggestions depends on the local LLM’s size and training

- Framework mapping is currently rule-guided + LLM-assisted

- PDF parsing of policy documents is limited (text-based input preferred)

## 🔮 Future Improvements

- Support for direct PDF ingestion

- Multi-framework comparison (ISO 27001, COBIT)

- Confidence scoring for policy completeness

- Interactive dashboard (still offline)

## 👥 Team & Hackathon
Built for HackIITK 2k26
Problem Statement 1 – Policy Gap Analysis using Local LLM

### THE MATRIX MINDS
- Raj Patel
- Raj Tiwari
- Rakshit Gupta 
- Sidak Sethi Singh 


## ⭐ Final Note

This project prioritizes privacy, offline security, and real-world applicability, making it suitable for organizations that cannot rely on cloud-based AI solutions for sensitive policy analysis.
