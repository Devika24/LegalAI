# 🧠 LegalAI: Multi-Agent Legal Document Generation System

This project implements an **AI-powered multi-agent legal document generation system** using **CrewAI**, **OpenAI GPT-4**, and **Google Gemini**.  
Each agent in the system plays a specialized legal role — drafting, reviewing, and validating the generated documents — ensuring compliance, accuracy, and minimal hallucinations.

---

## ⚖️ Project Overview

`Final_legalAI.ipynb` automates the creation of legally sound documents (like service agreements, NDAs, contracts) through the collaboration of multiple expert agents.

### 🔍 Core Objectives
- Generate professional, complete legal documents automatically.  
- Ensure compliance with laws and data privacy frameworks (GDPR, CCPA, etc.).  
- Detect and minimize hallucinations using GPT-4 verification.  
- Provide traceable, structured outputs using `pydantic` models.

---

## 🧩 Multi-Agent Architecture

| Agent | Role | Purpose |
|--------|------|----------|
| **Legal Expert** | Senior Legal Counsel | Drafts comprehensive legal documents using best practices. |
| **Compliance Officer** | Regulation Specialist | Reviews drafts for adherence to industry standards and data protection laws. |
| **Risk Analyst** | Contract Risk Expert | Identifies ambiguities, liabilities, or high-risk clauses. |
| **Quality Assurance** | Fact-Checker | Detects hallucinations and ensures factual and logical consistency. |

Each agent is powered by **CrewAI** and orchestrated in a **sequential process**, simulating a coordinated legal review team.

---

## ⚙️ Workflow Pipeline

```mermaid
flowchart TD
A[User Inputs Requirements] --> B[Legal Expert Drafts Document]
B --> C[Compliance Officer Reviews Regulations]
C --> D[Risk Analyst Identifies Liabilities]
D --> E[Quality Assurance Checks Accuracy]
E --> F[Gemini Generates Final Document]
F --> G[GPT-4 Hallucination Detector]
G --> H[Final Legal Document + Metadata]

