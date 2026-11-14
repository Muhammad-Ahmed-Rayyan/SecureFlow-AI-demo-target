<div align="center">

# 🎯 secureflow-demo-target

*Intentionally vulnerable codebase for AI-driven security remediation demos*

![Last Commit](https://img.shields.io/github/last-commit/Um-Ul-Baneen/secureflow-demo-target)
![Python](https://img.shields.io/badge/Python-100%25-blue?logo=python)
![languages](https://img.shields.io/github/languages/count/Um-Ul-Baneen/secureflow-demo-target)

<br>

Built with the tools and technologies:  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)

</div>

---

> ⚠️ **THIS REPOSITORY IS INTENTIONALLY VULNERABLE — FOR DEMO PURPOSES ONLY** 
>
> Do **not** deploy any code from this repository in a production environment.
> Every vulnerability present here is deliberate and serves as a target for
> automated AI-driven remediation tooling.

---

## 🧠 Project Summary

**Secureflow-demo-target** is a synthetic "customer" codebase used to demonstrate an **AI security-remediation pipeline**. Its files mirror **8 records** of a synthetic vulnerability scan dataset, with one deliberate vulnerability per module.

All secrets, tokens, credentials, and data in this repository are **synthetic and non-functional**. They exist solely to demonstrate vulnerability patterns.

---

## 🚀 Features

- 🐛 **Deliberate Vulnerabilities:** Eight modules, each containing exactly one known vulnerability pattern mapped to a scan record.
- 🏢 **Multi-Service Layout:** Code is organized into realistic microservice-style directories (`payment-api`, `admin-dashboard`, `data-pipeline`, etc.).
- ✅ **Functional Tests:** Verify normal behavior and are expected to **pass** on the vulnerable code.
- 💥 **Exploit Tests:** Verify each vulnerability is exploitable and are expected to **fail** on vulnerable code and **pass** once a fix is applied.
- 🤖 **Remediation Target:** Designed as the input for automated AI-driven fix generation and validation.

---

## 🛡️ Vulnerability Map

| # | File | Vulnerability |
|---|------|---------------|
| 1 | `notification-svc/src/main/service/File2.py` | SQL Injection (f-string query) |
| 2 | `data-pipeline/src/main/service/File4.py` | Insecure Deserialization (pickle) |
| 3 | `analytics-engine/src/main/controller/File16.py` | Insecure TLS (`verify=False`) |
| 4 | `search-indexer/src/main/service/File43.py` | Hardcoded Secret (API token) |
| 5 | `admin-dashboard/src/main/controller/File47.py` | Cross-Site Scripting (XSS) |
| 6 | `data-pipeline/src/main/config/File20.py` | Open Redirect |
| 7 | `admin-dashboard/src/main/util/File36.py` | Path Traversal |
| 8 | `payment-api/src/main/service/File34.py` | SQL Injection (LIKE clause) |

---

## 🗃️ Project Structure

```bash
secureflow-demo-target
├── notification-svc
│   └── src/main/service
│       └── File2.py               # SQL Injection (f-string query)
├── data-pipeline
│   └── src/main
│       ├── service
│       │   └── File4.py           # Insecure Deserialization (pickle)
│       └── config
│           └── File20.py          # Open Redirect
├── analytics-engine
│   └── src/main/controller
│       └── File16.py              # Insecure TLS (verify=False)
├── search-indexer
│   └── src/main/service
│       └── File43.py              # Hardcoded Secret (API token)
├── admin-dashboard
│   └── src/main
│       ├── controller
│       │   └── File47.py          # Cross-Site Scripting (XSS)
│       └── util
│           └── File36.py          # Path Traversal
├── payment-api
│   └── src/main/service
│       └── File34.py              # SQL Injection (LIKE clause)
├── tests                          # Functional and exploit tests
└── requirements.txt               # Project dependencies
```

---

## 🔧 Setup & Installation

> Make sure Python 3.8+ is installed.

```bash
# Clone the repo
git clone https://github.com/Um-Ul-Baneen/secureflow-demo-target.git
cd secureflow-demo-target

# (Optional) Create a virtual environment
python -m venv venv

# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

# Install required libraries
pip install -r requirements.txt
```

---

## 🧪 Running Tests

```bash
# Functional tests only (all should pass on vulnerable code)
pytest -q -m "not exploit"

# Exploit tests (all should FAIL on vulnerable code, pass after a fix)
pytest -q -m exploit
```

---

<div align="center">

⭐ Like what you see? Don't forget to hit that star on GitHub!

</div>
