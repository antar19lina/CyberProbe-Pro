# Cloud-Enabled-Penetration-Testing-Tool-Prototype
Built a modular Python-based penetration testing framework to automate reconnaissance, vulnerability scanning, and reporting using Dockerized micro-tools.

pentest-framework/
│
├── core/
│   ├── runner.py        # Main controller (orchestrates scans, handles AWS uploads)
│   ├── config.py        # Config for scans and AWS settings
│
├── modules/
│   ├── port_scan.py     # Port scanning
│   ├── web_check.py     # Web security headers
│   ├── dir_enum.py      # Directory enumeration
│   ├── vuln_check.py    # Basic vuln flagging (new, inspired by Nettacker)
│
├── reports/
│   └── report.json      # JSON report (uploadable to S3)
│
├── logs/
│   └── runtime.log      # Logs for debugging
│
├── tests/
│   ├── test_port_scan.py # Basic unit test
│
├── aws/
│   ├── deploy_ec2.sh    # Script to launch EC2 with IAM role
│   ├── s3_upload.py     # Upload reports to S3
│   ├── iam_policy.json  # IAM policy for EC2/S3 access (least-privilege)
│
├── docker/
│   ├── Dockerfile.scanner # Docker build
│
├── requirements.txt     # Python deps
├── README.md            # Docs with AWS guide and disclaimer
└── LICENSE              # Simple MIT license
