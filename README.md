# task8_hello_java_maven
# Jenkins Setup using Docker

## 🧩 Overview
This project demonstrates how to run Jenkins in a Docker container, install plugins, and access the Jenkins dashboard for CI/CD automation.

---

## ⚙️ Prerequisites
- Docker Desktop installed and running  
- Internet connection  
- Browser (Chrome or Edge)

---

## 🚀 Steps to Run Jenkins

### 1. Pull Jenkins Image
```bash
docker pull jenkins/jenkins:lts
2. Run Jenkins Container
bash
Copy code
docker run -d --name jenkins -p 9090:8080 jenkins/jenkins:lts
3. Get Jenkins Admin Password
bash
Copy code
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword
Copy the displayed password.

🌐 Access Jenkins
Open your browser and go to:
👉 http://localhost:9090

Paste the admin password when prompted.

🧩 Plugin Installation
When asked:

Click “Install suggested plugins”

If some plugins fail, click “Retry” or continue without them.

👤 Create Admin User
Fill in:

Username

Password

Full Name

Email

Then click Save and Continue.

✅ Jenkins Dashboard
You’ll now see the Jenkins home page.
From here, you can:

Create new pipelines

Connect with GitHub

Automate builds and tests

🛑 Common Issues
If Docker shows 500 Internal Server Error → Restart Docker Desktop.

If port 8080 is busy → Use a different port like -p 9090:8080.

To remove old container:

bash
Copy code
docker rm -f jenkins
