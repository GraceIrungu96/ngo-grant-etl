# NGO Grant Compliance & Risk Audit Pipeline

##  Project Overview
This ETL (Extract, Transform, Load) pipeline was engineered to solve a specific legal bottleneck for small-to-medium NGOs. It automates the auditing of Grant MOUs by programmatically scanning agreement transcripts for critical indemnity clauses—specifically the **No-Liability Clause**.

In high-urgency environments, manual oversight of legal notes can lead to significant financial exposure. This tool provides an automated "Safety Gate" by flagging high-risk partnerships before they reach the finance department.

##  Tech Stack
- **Language:** Python 3.10+
- **Data Engine:** Pandas (Vectorized logic for high-performance auditing)
- **Database:** PostgreSQL (Relational storage for audit persistence)
- **Connectivity:** SQLAlchemy (Object Relational Mapping)
- **Environment:** Linux/Ubuntu, Dotenv (Secure credential management)

##  Architectural Workflow
1. **Extraction**: Ingests raw partner data and MOU transcripts.
2. **Transformation**: Executes a risk-assessment algorithm that categorizes records into `SECURE` or `HIGH RISK` based on legal keyword presence.
3. **Loading**: Transmits audited records to a PostgreSQL production database.
4. **Security**: Zero-Trust architecture utilizing `.env` masking to prevent credential leakage.

## Key Features
- **Automated Risk Flagging**: Real-time categorization of grant status.
- **Production-Ready**: Scripted for headless execution via Cron jobs.
- **Audit Trail**: Every transformation is logged and stored in a permanent SQL table for historical compliance reviews.

##  Project Structure
- `ngo_grant_audit_pipeline.ipynb`: Core logic and development environment.
- `.env`: (Local only) Secure database configuration.
- `.gitignore`: Prevents sensitive data and bulky virtual environments from being committed.

## ⚖️ License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
