# Cloud Squad — AWS Exam Readiness Checker

A clean, serverless web application that helps AWS exam candidates quickly determine their readiness based on a practice test score.  
Built using modern **AWS serverless architecture** and deployed with **GitHub-integrated CI/CD**.

---

## Live Demo
**Frontend (AWS Amplify):**  
https://main.dgqde671qhhxp.amplifyapp.com

---

## Features
- Enter a **User ID** and **score (0–100)**
- Instantly receive **Ready / Not Ready** result
- Results are **stored in DynamoDB**
- Fully **serverless architecture**
- Automatic **CI/CD deployment via GitHub → AWS Amplify**

---

## Architecture Overview

```mermaid
flowchart LR
  A[User Browser] --> B[AWS Amplify Hosting]
  B --> C[API Gateway HTTP API /check]
  C --> D[AWS Lambda checkExamReadiness]
  D --> E[DynamoDB ExamResults Table]
