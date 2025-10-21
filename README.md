# 🚀 Simple Jenkins Pipeline for CI/CD 🚀

## Objective
Set up a basic Jenkins pipeline to automate the process of building and deploying an application.

## Tools Used
- Jenkins
- Docker

---

## 🚀 Project Overview
This project demonstrates how to create a simple Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins and Docker. The pipeline automates the building, testing, and deployment stages of an application.

---

## Steps to Implement the Pipeline

1. **Install Jenkins**  
   Set up Jenkins on my local machine .

   ![Jenkins Setup](https://www.jenkins.io/doc/book/resources/img/jenkins-dashboard.png)  
   *Jenkins Dashboard*

2. **Create a Jenkinsfile**  
   Add a 'Jenkinsfile' to my project repository with the pipeline script defining stages such as `build`, `test`, and `deploy`.

3. **Configure Jenkins**  
   - Create a Jenkins pipeline job linked to my project repository.  
   - Enable **Poll SCM** or set up webhooks to trigger the pipeline on each code commit.

4. **Pipeline Stages**  
   The Jenkins pipeline should include the following stages:  
   - **Build:** Build the Docker image for the app.  
   - **Test:** Run tests to validate the build (optional, based on your app).  
   - **Deploy:** Deploy the built Docker container to the desired environment.
     <img width="1920" height="1080" alt="task2 final" src="https://github.com/user-attachments/assets/feecd67d-2cda-40a7-94dc-f575e9425314" />


5. **Test the Pipeline**  
   Push changes to your repository and verify the pipeline execution on the Jenkins dashboard.

<img width="1920" height="1080" alt="task2 4 (2)" src="https://github.com/user-attachments/assets/acc09b24-6ca6-4630-b4df-63e332ee0088" />

<img width="1920" height="1080" alt="task2 4" src="https://github.com/user-attachments/assets/fa926ecc-bceb-4e27-b3ad-4c0c71a987c0" />

<img width="1920" height="1080" alt="task2 1" src="https://github.com/user-attachments/assets/2ac4ef11-aaf4-4779-9b34-246098ad2b19" />



---
