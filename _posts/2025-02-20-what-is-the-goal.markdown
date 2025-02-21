---
layout: post
title:  "What is the goal for Delve?"
date:   2025-02-20 17:44:02 +0000
categories: information
---

**Delve** aims to be a unified platform for **Software Composition Analysis (SCA)** and streamlined **vulnerability management**, enabling faster remediation times through an intuitive interface.

### 🛠️ **Core Objective**  
To empower developers with an easy-to-use tool that simplifies the process of identifying and managing vulnerabilities in their software stack.

### 📂 **How It Works**  
Developers can upload any of the following:  
- 📁 **Raw Source Code**  
- 📦 **Dependency Artifacts**  
- 🐳 **Containers**

Delve will then:  
1. **Generate a Software Bill of Materials (SBOM)** using [**Syft**](https://github.com/anchore/syft) — a powerful tool for extracting accurate package data from code, artifacts, and containers.  
2. **Scan for vulnerabilities** using [**Grype**](https://github.com/anchore/grype), which cross-references known vulnerabilities against the SBOM.  
3. **Produce an actionable vulnerability report** that highlights security risks in a clear, developer-friendly format.  
4. **Integrate findings** into the **Vulnerability Management Interface** and store them in the platform’s database for ongoing tracking and remediation.

### 🚀 **Why Delve?**  
- ✅ **Automation-first** — Reduces manual overhead in vulnerability tracking.  
- ✅ **Clear Reporting** — Presents vulnerabilities in an easy-to-understand format.  
- ✅ **Unified Workflow** — From SBOM generation to remediation, all in one platform.

---

*Delve simplifies security so developers can focus on building, not fixing.*  
