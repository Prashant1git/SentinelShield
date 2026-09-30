# SentinelShield 
* A middleware filter
# 🛡️ SentinelShield: Automated BOLA Assessment & Hot-Patching Engine

**Project Framework for Smart India Hackathon 2026**  
**Problem Statement Track:** World Monitor Application Security Assessment  
**Technical Focus:** API Security, Broken Object Level Authorization (BOLA), Automated Remediation Middleware  

---

## 🚀 Overview

SentinelShield is an advanced, lightweight security orchestration framework designed to protect enterprise real-time dashboards (such as **World Monitor**) from high-stakes authorization loop holes. 

Traditional vulnerability assessment systems flag errors but leave systems exposed until manual developers patch the codebase. SentinelShield introduces a dual-engine paradigm:
1. **The Assessment Engine (`exploit.py`):** Automatically tests API paths for parameter-tampering structural anomalies (**CWE-285**) and evaluates risk metrics utilizing the **CVSS v3.1 standard**.
2. **The Remediation Engine (`patch.py`):** Dynamically injects an isolated validation middleware wrapper into the runtime application loop to neutralize the attack vector with **Zero System Downtime**.

---

## ⚙️ Core Architecture & Feasibility Features

* **Zero-Downtime Hot-Swapping:** Implements dynamic runtime configuration toggles, allowing applications to be protected instantly without requiring server reboots.
* **Microsecond Latency Interception:** Uses lightweight, memory-efficient lookahead parameter cross-referencing to ensure zero data pipeline lagging.
* **Plug-and-Play Framework Interoperability:** Written in pure, modular Python handlers, making it seamlessly adaptable to frameworks like FastAPI, Flask, Django, or Node.js routing.
* **Cloud-Native & Low Resource Cost:** Validated inside version-controlled **GitHub Codespaces** containers with virtually zero CPU/RAM operational overhead.

---

## 📦 Directory Structure

```text
SentinelShield/
├── app.py          # Simulated World Monitor Backend API (Vulnerable / Patched states)
├── exploit.py      # SentinelShield Automated Vulnerability Assessment Suite
├── patch.py        # Hot-Patching Middleware Deployment Trigger
└── README.md       # Technical Repository Documentation
```

---

## 🛠️ Step-by-Step Execution Guide

To simulate the complete detection, hot-patching, and automated mitigation cycle inside your environment, leverage a split-terminal layout:

### Step 1: Initialize the Application Server
Launch the primary target mock system inside your first terminal panel:
```bash
python app.py
```
*Output: `🚀 World Monitor Mock Application Running on http://localhost:8080...`*

### Step 2: Execute Vulnerability Assessment (Verify the Flaw)
Open a parallel terminal panel and trigger the test suite to scan for access control vulnerabilities:
```bash
python exploit.py
```
*Result: The system successfully exploits a **BOLA loophole**, bypassing low-tier employee token constraints to exfiltrate the Administrator's raw **Top Secret Data Matrix**. The engine logs a critical evaluation rating of **CVSS 9.8**.*

### Step 3: Deploy Runtime Remediation Block
Inside your testing terminal, deploy the live hot-patch:
```bash
python patch.py
```
*Result: Updates the backend routing parameters instantaneously, reinforcing the runtime layer without service degradation.*

### Step 4: Re-Verify Application Security Posture
Run the vulnerability evaluation module one final time to check system defenses:
```bash
python exploit.py
```
*Result: The attack vector is completely neutralized. The application intercepts the token-mismatch payload and safely blocks access with an explicit **HTTP Error 403: Forbidden** response.*

---

## 📚 Standard Reference Implementations

* **OWASP API Security Top 10 Framework:** API1:2023 - Broken Object Level Authorization
* **MITRE Common Weakness Enumeration:** CWE-285: Improper Authorization
* **FIRST CVSS v3.1 Specification Guidelines:** Common Vulnerability Scoring Matrix Standards
