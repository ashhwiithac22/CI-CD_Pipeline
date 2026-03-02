# 📱 Android CI/CD Pipeline using Jenkins
## 🚀 Project Overview

This project demonstrates how to build a **Continuous Integration and Continuous Delivery (CI/CD)** pipeline for an Android application using **Jenkins**, **Git**, and **Gradle**.

The pipeline automatically:

- Pulls source code from GitHub  
- Builds the Android application  
- Runs tests  
- Generates APK  
- Archives the APK as a Jenkins artifact  

This reduces manual work and ensures reliable builds.

---

## 🎯 Objectives

- Install and configure Jenkins on Linux  
- Set up Android development environment  
- Integrate GitHub with Jenkins  
- Create Jenkins pipeline using Jenkinsfile  
- Automate APK generation  
- Demonstrate CI/CD workflow for Android  

---

## 🧰 Tech Stack

- Java (JDK 11)  
- Android Studio  
- Android SDK  
- Gradle  
- Git & GitHub  
- Jenkins  
- Ubuntu  

---

## ✅ Prerequisites

Ensure the following are installed:

- Java JDK 11  
- Android Studio  
- Android SDK & Build Tools  
- Git  
- Jenkins Server  
- Gradle Wrapper  

### 🔍 Verify Installation

```bash
java -version
adb version
sdkmanager --list
git --version
```
--- 
### ⚙️ Jenkins Setup
1️⃣ Install Jenkins
```
sudo apt update
sudo apt install jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

Access Jenkins:
```
http://localhost:8080
```
Unlock Jenkins:
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

2️⃣ Required Jenkins Plugins
- Install from Manage Jenkins → Plugins:
- Git Plugin
- Pipeline Plugin
- Gradle Plugin
- Email Extension Plugin

### 🔗 GitHub Integration
- git init
- git add .
- git commit -m "Added Jenkinsfile"
- git remote add origin https://github.com/ashhwiithac22/CI-CD_Pipeline.git
- git branch -M main
- git push -u origin main
- 

### 🔄 Poll SCM Configuration

Enable automatic builds:

- Build Triggers → Poll SCM
- H/2 * * * *

Meaning:

- Jenkins checks repository approximately every 2 minutes
- If new commit found → build triggers automatically
  
--- 

### 📦 Build Output
APK Location: 
- app/build/outputs/apk/debug/app-debug.apk
  
### 📥 Download Steps

- Open Jenkins Dashboard
- Select Pipeline Job
- Open successful build
- Click Artifacts
- Download APK

### 🚀 Build Execution Flow

- Jenkins pulls latest code
- Environment variables set
- Gradle build runs
- Tests executed
- APK generated
- Artifact archived
- Build marked SUCCESS

--- 
### ⭐ Key Benefits

- Automated Android builds
- Faster feedback cycle
- Reduced manual errors
- Consistent build environment
- Easy artifact management

--- 
### 📌 Conclusion

This project successfully demonstrates the implementation of a CI/CD pipeline for an Android application using Jenkins. The automated workflow ensures reliable builds, faster development cycles, and efficient artifact management.

--- 
