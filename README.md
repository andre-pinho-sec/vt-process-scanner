# 🛡️ VT Process Scanner

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)]()
[![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

A lightweight Windows process threat triage tool built in Python.

This tool enumerates running processes, detects suspicious behavior (such as spoofed system binaries), and integrates with VirusTotal to provide reputation-based analysis.

---

## 🎯 Purpose

Designed for:

* 🔍 Malware analysis practice
* 🛠️ Incident response triage
* 🧪 Security research and experimentation

---

## ✨ Features

* 🔍 Real-time process scanning using `psutil`
* 🔑 VirusTotal integration (`vt-py`)
* 🧠 Detection of spoofed system processes
* 📝 Persistent whitelist system (`whitelist.json`)
* 🎨 Color-coded CLI output:

  * 🟢 Safe
  * 🟡 Unknown
  * 🔴 Malicious
* 📊 Automatic CSV report generation
* ⚡ Interactive menu interface

---

## 🖥️ How It Works

1. Enumerates all running processes
2. Validates known system processes
3. Detects anomalies (e.g., fake `svchost.exe`)
4. Queries VirusTotal for unknown executables
5. Outputs results and saves a report

---

## 📦 Installation

```bash
git clone https://github.com/andre-pinho-sec/vt-process-scanner.git
cd vt-process-scanner
```

```bash
python -m venv venv
venv\Scripts\activate
```

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

```bash
python scanner.py
```

On first run, insert your VirusTotal API key.

---

## 📊 Example Output

```
[OK] System process: services.exe (PID 672)
[OK] Known app: chrome.exe (PID 2140)
[!!!] SPOOFED: svchost.exe (PID 3024) Path: C:\Users\...
[!!!] MALICIOUS: badprocess.exe (PID 5001)
```

---

## 📁 Project Structure

```
vt-process-scanner/
├── scanner.py
├── requirements.txt
├── whitelist.json
├── apikey.json
└── reports/
```

---

## ⚠️ Disclaimer

This tool is for educational and research purposes only.
Always verify VirusTotal results before taking action.

---

## 👨‍💻 Author

André – Cybersecurity Enthusiast
