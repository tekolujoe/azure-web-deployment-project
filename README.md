# azure-web-deployment-project
Capstone Project - Deploying Applications Across Various Service Models on Azure (IaaS &amp; PaaS)
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
