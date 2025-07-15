# ✉️ AI Email Writer Assistant

An AI-powered tool that helps you automatically generate professional, smart email replies directly inside Gmail and Outlook.  
Powered by Java Spring Boot, React (optional), and a Chrome Extension. Deployed with Docker on Azure.

---

## 🚀 Features

✅ Generate context-aware replies to emails with one click  
✅ Choose tone: Professional, Casual, Friendly  
✅ Chrome Extension integrates into Gmail & Outlook, adds "AI Reply" button to your compose box  
✅ Spring Boot backend using Gemini (or other generative language models)  
✅ Deployed on Azure App Service via Docker, image hosted on Docker Hub

---

## 🖥️ Tech Stack

| Layer              | Technology                          |
|--------------------|------------------------------------|
| **Backend API**     | Java 21, Spring Boot 3, WebClient  |
| **Frontend UI**     | React + MUI (optional)             |
| **Browser Extension** | JavaScript (Manifest V3)         |
| **Containerization** | Docker, Docker Hub               |
| **Cloud**           | Azure App Service (Linux Container) |

---

## 🚀 Getting Started

## 🐳 Run backend locally via Docker
### 🐳 Pull the latest image from Docker Hub
`docker pull dasiladev/email-writer-app:latest`

### 🚀 Run the container on port 8080
`docker run -d -p 8080:8080 --name email-writer dasiladev/email-writer-app:latest`

### ✅ Check that the container is running
`docker ps`

### 📝 To see logs (check API startup & requests)
`docker logs -f email-writer`

## The API will be available at:


`http://localhost:8080/api/email/generate`

## ⚙️ Environment variables
Configure your backend with environment variables for security:
```
GEMINI_API_URL=https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
GEMINI_API_KEY=YOUR_API_KEY

```
✅ On Azure, add these as App Settings under your App Service Configuration.

---
# 🌐 Chrome Extension
The Chrome Extension injects an "AI Reply" button directly into Gmail & Outlook.
When clicked, it:

- Reads the email thread content

- Sends it to your backend

- Inserts the generated reply into the compose box

## 🔧 Set your backend URL
Inside your extension project, edit:


```const BACKEND_URL = "https://example-appp-123.centralindia-01.azurewebsites.net";```
