---
layout: post
title:  "Serving an API - Phase 1"
date:   2025-02-21 13:07:02 +0000
categories: progress
---

### 🔧 **Phase 1: Setting Up the AWS Infrastructure**  
For the initial testing phase of my project, I focused on setting up the necessary **AWS infrastructure** to process and parse application source code, while serving the results over an API.

I started by testing the infrastructure with **Flask** to ensure proper configuration, but have since migrated to a **Node.js API** for scalability and flexibility.

### 🖥️ **Server Setup**  
The EC2 instance, which acts as both the **Processing** and **API Server**, has the following binaries installed:

- 🔐 **Syft** — For generating SBOMs from source code, artifacts, and containers.  
- ⚠️ **Grype** — For scanning SBOMs for known vulnerabilities.  
- 🚀 **Delve** — My custom vulnerability management interface.  
- 🌐 **Node.js & NPM**  
  - 🛠️ **pm2** — Process manager to keep the Node.js API running smoothly.  
  - ⚡ **Express** — Web framework to handle API requests.  
  - 🔒 **dotenv** — Securely managing environment variables.  
  - 📂 **path** — Path utilities for file handling.

### 🚀 **Initial Testing & Results**  
During this phase, I was able to successfully:
1. **Communicate** with the API hosted on AWS from my local machine.
2. **Upload** source code or dependencies for processing.
3. **Retrieve the results** from the API, including SBOMs and vulnerability reports.

This was a promising start, demonstrating that the infrastructure was working as expected and the API was responding correctly.

### 🔐 **Next Steps: Adding Authentication**  
While the testing phase has been successful, the next step is to introduce **authentication** to the API. Specifically, each user should only be able to access and interact with the files they have personally processed.

My plan for this phase:
- **Implement user authentication** using **AWS Cognito** and JWT Bearer Tokens.
- **Ensure file access control**, allowing users to only retrieve files they uploaded or processed.

This will significantly enhance the security and usability of the API, allowing for safe, personalized access to the data.

### 💻 **Early Implementation of the API**

Below is an early implementation of the **Node.js API** for serving uploaded files:

```javascript
const express = require("express");
const path = require("path");
const dotenv = require("dotenv");

dotenv.config();

const app = express();
const port = process.env.PORT || 3000;

// Directory for stored files
const FILES_DIR = path.join(__dirname, "files");

// Serve static files
app.use("/files", express.static(FILES_DIR));

// API to download a file
app.get("/download/:filename", (req, res) => {
    const filePath = path.join(FILES_DIR, req.params.filename);
    res.download(filePath, (err) => {
        if (err) {
            res.status(404).json({ error: "File not found" });
        }
    });
});

// Start the server
app.listen(port, () => {
    console.log(`File API running on port ${port}`);
});
```

---

*For the next update, I'll dive deeper into the authentication process and how I plan to enforce these security measures.*
