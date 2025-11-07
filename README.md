# 🏥 Healthcare Analytics Case Study – SJGHC Hospital Episode Analysis

## 📌 Overview
This case study analyzes de-identified hospital episode data from St John of God Health Care (SJGHC), focusing on operational efficiency, financial risk, and referral optimization. The dataset follows the Hospital Casemix Protocol (HCP), capturing clinical, demographic, and billing details across 30,000+ episodes.

The goal: uncover actionable insights that improve patient care, streamline resource allocation, and support cost containment strategies for both hospitals and insurers.

## 🧠 Executive Summary
- **Same-day episodes dominate** (78.45%), suggesting opportunities to optimize short-stay throughput and discharge protocols.
- **Peak admission time** is 7:30 AM on Wednesdays — critical for staffing and scheduling.
- **Top 10 episodes** exceed $4.8M in charges, with outliers reaching $6.9M — potential audit targets for billing anomalies.
- **External medical practitioners** drive 91% of referrals, yet emergency referrals show higher cost per episode — a referral strategy review is warranted.
- **Postcode-level cost variation** reveals geographic hotspots for high-cost care, informing regional planning and insurer negotiations.

## 💡 Stakeholder Actions
| Role | Action | Impact |
|------|--------|--------|
| **Finance Lead** | Audit top episodes for prosthesis/theatre billing | Recover $X in overcharges |
| **Operations Manager** | Staff peak hours and days | Improve throughput and reduce delays |
| **Clinical Director** | Review discharge coding and urgency flags | Enhance compliance and care transitions |
| **Strategy Lead** | Engage high-referral GPs and optimize pathways | Reduce avoidable admissions |

## 🛠️ Technologies Used
- Python (pandas, numpy)
- Power BI
- Jupyter Notebook

## 📁 Project Structure & Reproducibility

This project uses a modular, versioned workflow to support reproducible analytics across devices and sessions.

### Folder Structure
data/ ├── raw/               # Original Excel dataset (dummy data) ├── staging/           # Intermediate pickle files for fast reloads ├── cleansed/          # Cleaned dataset with normalized dates and numeric fields ├── transformed/       # Final dataset with engineered features notebooks/ └── sjghc_analysis.ipynb  # Main analysis notebook

### Versioned Data Loading
The notebook includes a reusable function to load data based on version checkpoints:

```python
df = load_or_create_df(version="raw", excel_path="...")

## 👤 Author
Kevin Wang – Data Analyst | Healthcare Insights | Workflow Automation
