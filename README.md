# Cloud-Enabled-Penetration-Testing-Tool-Prototype
Built a modular Python-based penetration testing framework to automate reconnaissance, vulnerability scanning, and reporting using Dockerized micro-tools.

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
