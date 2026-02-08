# cloud-pentesting-automation
Python-based cloud-deployed security automation tool for reconnaissance, basic vulnerability analysis, and structured reporting in authorized environments.
## 📂 Project Structure

```text
pentest-framework/
│
├── core/
│   ├── runner.py        # Main controller (orchestrates scans, AWS uploads)
│   ├── config.py        # Scan configuration & AWS settings
│
├── modules/
│   ├── port_scan.py     # TCP port scanning
│   ├── web_check.py     # Web security headers analysis
│   ├── dir_enum.py      # Directory enumeration
│   ├── vuln_check.py    # Basic vulnerability flagging (rule-based)
│
├── reports/
│   └── report.json      # Structured JSON scan report
│
├── logs/
│   └── runtime.log      # Runtime logs for debugging & auditing
│
├── tests/
│   └── test_port_scan.py # Basic unit test (pytest)
│
├── aws/
│   ├── deploy_ec2.sh    # EC2 deployment script (with IAM role)
│   ├── s3_upload.py     # Upload reports to Amazon S3
│   ├── iam_policy.json  # Least-privilege IAM policy
│
├── docker/
│   └── Dockerfile.scanner # Dockerized scanner environment
│
├── requirements.txt     # Python dependencies
├── README.md            # Project documentation
└── LICENSE              # MIT License
```

Skills Demonstrated
Python: Functions, imports, error handling, JSON manipulation, logging.
Docker: Containerization for portability (build/run images).
AWS EC2: Cloud VM deployment for secure scans.
AWS S3: Object storage for reports (upload/download).
AWS IAM: Policies for access control (e.g., secure S3 perms).
Cloud Computing: Scalable, ethical deployment in the cloud.
Other: Ethical hacking basics (OWASP headers), CLI automation, modular design, testing (unit tests).

# Cloud Pentesting Automation (Educational)

# Overview
This project is a Python-based cloud-deployed security automation tool designed
to assist in reconnaissance, basic vulnerability analysis, and structured
reporting for **authorized security testing environments**.

The focus of this project is **analysis and reporting**, not exploitation.

---

## Security Problem Addressed
Manual reconnaissance and initial security assessments are time-consuming and
error-prone when repeated across multiple targets.

Security analysts require:
- Consistent data collection
- Structured findings
- Clear logs for review and escalation

---

# What This Tool Does
- Performs automated reconnaissance (ports, headers, directories)
- Applies rule-based vulnerability checks (OWASP-aligned)
- Generates structured JSON reports for analysis
- Logs all scan activity for traceability
- Uploads reports securely to AWS S3 using least-privilege IAM roles

---

# How Analysis Works
- Port scan results identify exposed services
- HTTP response headers are checked for security misconfigurations
- Directory enumeration highlights potential attack surfaces
- Findings are classified by **severity and category**
- Results are consolidated into a machine-readable report for review

---

# Analyst-Relevant Output
- Target scanned
- Issue identified
- Severity level
- Evidence (response headers / endpoint)
- Timestamped logs for audit purposes

Example:
```json
{
  "target": "example.com",
  "issue": "Missing Security Headers",
  "severity": "Medium"
}
