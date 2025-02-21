---
layout: page
title: Resources
permalink: /resources/
---

Welcome to the **Resources** page! 🚀  
This section is dedicated to providing you with the tools, materials, and insights I've developed and curated throughout the journey of creating **Delve**.

---

## 🔧 **About Delve: SBOM & Vulnerability Management Suite**

**Delve** is an integrated platform designed for **Software Composition Analysis (SCA)** and **vulnerability management**. It streamlines the process of scanning and analyzing software dependencies, containers, and source code, helping developers identify outdated and vulnerable components in their applications.

---

### 📄 **Project Resources**

- **[Delve GitHub Repository](https://github.com/DylBP/SBOM-FYP)**  
  The complete source code for the Delve project, including documentation, setup instructions, and configuration details. Check out the repository for in-depth information on how Delve works, the technologies used, and future updates.

- **[Semester 1 Report]({{ 'assets/docs/Dylan Butler Parry - 20099082 - FPY Semester 1 Report.pdf' | relative_url }})**  
  A deep dive into the architecture, challenges, and future roadmap of the Delve project.

- **[Delve Documentation (WIP)](#)**  
  Comprehensive guides to help you get started with **Delve**. This includes setup guides, configuration details, and step-by-step instructions on how to use the platform for Software Composition Analysis (SCA) and vulnerability management.

- **[Delve API Documentation (WIP)](#)**  
  All the details you need to integrate with the Delve API for vulnerability scanning, SBOM generation, and more. This includes API endpoints, authentication requirements, and usage examples.

---

## 💻 **Technologies Behind Delve**

Delve is built on a stack of powerful tools and technologies, each of which plays a key role in ensuring the system operates efficiently and securely.

- **[Syft](https://github.com/anchore/syft)**  
  Syft is a tool used to generate Software Bill of Materials (SBOMs) from source code, container images, and artifacts. This allows Delve to map out exactly which components are used in a given project, helping to pinpoint vulnerable dependencies.

- **[Grype](https://github.com/anchore/grype)**  
  Grype is a vulnerability scanner that works seamlessly with Syft’s SBOMs. Delve uses Grype to scan for known vulnerabilities in the components used within a software package, offering a clear report of potential security risks.

- **[AWS (EC2, S3, DynamoDB, Cognito)](https://aws.amazon.com/)**  
  Delve leverages AWS for scalable cloud infrastructure:
  - **EC2**: Virtual servers for hosting applications.
  - **S3**: Storage for managing large datasets and SBOM files.
  - **DynamoDB**: NoSQL database for storing metadata and component data.
  - **Cognito**: User authentication and management for secure access to the platform.

- **[Node.js](https://nodejs.org/)**  
  Node.js is used to build the backend of Delve, providing a fast and efficient runtime for server-side applications and APIs.

- **[Express](https://expressjs.com/)**  
  Express is a web framework for Node.js, simplifying the process of building robust RESTful APIs to interact with Delve's components and services.

- **[React](https://reactjs.org/)**  
  React is employed to create dynamic and responsive frontend interfaces for Delve, ensuring a smooth and user-friendly experience for interacting with the platform.

---

## 📚 **Learning Resources & Inspiration**

Throughout the development of **Delve**, I’ve relied on a variety of sources and inspiration from the tech community. These resources have shaped the direction of the project and influenced the technologies I’ve implemented:

- **[OWASP](https://owasp.org/)** — A key organization in web application security, offering invaluable resources, including vulnerability scanning techniques and secure development practices.

- **[Hack The Box](https://www.hackthebox.eu/)** — A platform for improving penetration testing and cybersecurity skills. The hands-on experience gained here has greatly contributed to the development of Delve's vulnerability management capabilities.

- **[TryHackMe](https://tryhackme.com/)** — Another great resource for anyone looking to improve their cybersecurity knowledge through practical labs and tutorials.

---

## 🚀 **What’s Next for Delve?**

As Delve continues to evolve, I am focused on adding the following features:

- **Real-time vulnerability scanning** for faster vulnerability detection.
- **Enhanced SBOM parsing** with deeper insights into software components.
- **User authentication** to ensure secure access to processed files.

Stay tuned for future updates and releases!

---

Feel free to check out the resources linked above or reach out if you have any questions about **Delve** or my development process. I’m always open to feedback and collaboration opportunities!

---

*Stay connected and follow the progress of Delve on my [GitHub](https://github.com/DylBP)!*
