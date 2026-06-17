# 📄 Contract Risk Analyzer

An AI-powered legal intelligence tool that helps freelancers, startups, and small businesses understand contract risks without requiring legal expertise.

🔗 **Live Demo:** https://clause-risk-analyser.streamlit.app

---

## Overview

Contract Risk Analyzer automatically reviews uploaded PDF contracts, extracts legal clauses, identifies potential risks, and explains them in plain English.

Instead of manually reading lengthy agreements, users receive a structured risk assessment dashboard within minutes.

---

## Key Features

1. Upload legal agreements directly through a simple web interface.

2. Automatically identifies and extracts individual legal clauses from the contract.

3. Classifies clauses into High Risk , Medium Risk , Low Risk or Informational

4. Transforms legal jargon into concise, easy-to-understand summaries.

5. Visualizes contract risks through metrics, tables, and detailed clause analysis.

6. Export analyzed results as a CSV report for future review.

---

## Architecture

```text
PDF Contract
      │
      ▼
PyMuPDF Text Extraction
      │
      ▼
Gemini 2.5 Flash
Clause Extraction
      │
      ▼
Gemini 2.5 Flash
Risk Analysis
      │
      ▼
Risk Dashboard
(Streamlit)
```

---

## Tech Stack

| Component      | Technology                |
| -------------- | ------------------------- |
| Frontend       | Streamlit                 |
| Language       | Python                    |
| PDF Processing | PyMuPDF                   |
| Data Handling  | Pandas                    |
| AI Model       | Gemini 2.5 Flash          |
| Deployment     | Streamlit Community Cloud |

---

## Target Users

* Freelancers
* Startups
* Small & Medium Businesses (SMEs)
* Procurement Teams
* Non-Legal Professionals

---

## Local Setup

Clone the repository:

```bash
git clone https://github.com/vaish9825/contract_risk_analyser.git
cd contract_risk_analyser
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create:

```text
.streamlit/secrets.toml
```

Add your Gemini API key:

```toml
GOOGLE_API_KEY="YOUR_API_KEY"
```

Run locally:

```bash
streamlit run app.py
```

---
## Future Improvements

* OCR support for scanned contracts
* Contract-level risk scoring
* PDF report generation
* Multi-language support
* Fine-tuned legal language models
