# Azure Web Deployment Project

Capstone Project — Deploying Applications Across Various Service Models on Azure (IaaS & PaaS)

This project demonstrates deploying a simple web application using two different Azure cloud service models:

- **IaaS (Infrastructure as a Service)** → Azure Virtual Machine
- **PaaS (Platform as a Service)** → Azure App Service

---

## Project Overview

The objective of this project was to:

✅ Explore Azure deployment models (IaaS vs. PaaS)  
✅ Deploy and serve a sample web application using each model  
✅ Compare features, ease of use, and flexibility between the two approaches

---

## Files Included

### `index.html`

A simple HTML web page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Cloud App</title>
</head>
<body>
  <h1>Hello from Gbadeweb’s App Service on Azure!</h1>
</body>
</html>





### `server.js`

const express = require('express');
const app = express();

app.use(express.static(__dirname));

const port = process.env.PORT || 3000;
app.listen(port, () => {
  console.log(`Server listening on port ${port}`);
});




### `package.json`

{
  "name": "wwwroot",
  "version": "1.0.0",
  "description": "",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^5.1.0"
  }
}


**IaaS Deployment (Azure Virtual Machine)**
✅ Deployed on an Ubuntu VM using Nginx.

✅ **Steps performed:**
Created a VM in Azure
Installed Nginx

Deployed the HTML page at:
/var/www/html/index.html

✅ **VM Public IP:**
48.217.68.124

✅ Browser output:
Hello from Gbadeweb’s VM on Azure!

**PaaS Deployment (Azure App Service)**
✅ Deployed on Azure App Service running Node.js 20 LTS (Linux).
✅ Deployment steps:

**Created an App Service**
Uploaded index.html, server.js, and package.json

**Configured startup command:**
npm start

✅ **App Service URL:**
https://webjoeapp.azurewebsites.net

✅ **Browser output:**
**Hello from Gbadeweb’s App Service on Azure!**

Project Outcome
This project highlights:

**IaaS (VM):**
Total control of OS and environment
Requires manual server configuration (Nginx, file management)

**PaaS (App Service):**
Simplified deployment
Managed runtime
No server maintenance required

✅ Both models successfully served the same web app, demonstrating different levels of flexibility and complexity.
