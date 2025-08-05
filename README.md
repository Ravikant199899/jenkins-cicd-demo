# Jenkins CI/CD Pipeline Demo

## Overview
This project demonstrates a simple **Jenkins + Docker CI/CD pipeline** integrated with **GitHub** and deployed on an **AWS EC2 Ubuntu instance**. The pipeline automates building, testing, and deploying a sample application whenever code changes are pushed to GitHub.

---

## Prerequisites
Before you start, ensure you have the following:
- An **AWS account** with an Ubuntu EC2 instance running.
- Jenkins installed on the EC2 instance.
- Docker installed on the EC2 instance.
- A **GitHub repository** containing your application code and Jenkinsfile.
- Basic knowledge of Git, Jenkins, and Docker.

---

## Setup Steps
Follow these steps to set up the CI/CD pipeline:

1. **Launch an Ubuntu EC2 instance on AWS.**  
   ![AWS EC2 Instance Setup](screenshots/instance.png)  
   *(Screenshot of AWS EC2 instance running)*

2. **SSH into your EC2 instance.**  
   ![SSH Access](screenshots/SSH-access.png)  
   *(Terminal showing successful SSH connection)*

3. **Install Jenkins on the EC2 instance.**  
   - Added Jenkins repository key.  
   - Installed and started Jenkins service.  
   ![Jenkins Installation Step 1](screenshots/Jenkins-Installation-stp_l.png)  
   ![Jenkins Installation Step 2](screenshots/Jenkins-installation-stp_2.png)  
   ![Jenkins Installation Step 3](screenshots/Jenkins-Installation-stp_3.png)  
   ![Jenkins Installation Step 4](screenshots/Jenkins-Installation-stp_4.png)  
   ![Jenkins Installation Step 5](screenshots/Jenkins-Installation-stp_5.png)  

4. **Install Docker and enable Jenkins to use Docker.**

5. **Create a GitHub repository** containing your `app.py` and `Jenkinsfile`.  
   ![GitHub Repo Page](screenshots/Repo-Page.png)

6. **Create a new Pipeline job in Jenkins, and configure it to use your GitHub repo.**  
   ![Create Jenkins New Item](screenshots/Create_Jenkin-Newltem.png)  
   ![Pipeline Config Step 1](screenshots/Pipeline-Config-Stp_I.png)  
   ![Pipeline Config Step 2](screenshots/Pipeline-Config-Stp_2.png)

7. **Configure GitHub webhook for automatic build triggers.**

8. **Verify the Jenkins Dashboard showing your job is ready.**  
   ![Jenkins Dashboard](screenshots/Jenkins-Dashboard.png)  
   ![Jenkins Job](screenshots/Jenkins-Job.png)

9. **Trigger the pipeline manually or by pushing code and verify the build success.**  
   ![Build Successful](screenshots/Build-Sucessful.png)

---

## Pipeline Stages

- **Build:** Builds the application or Docker image.  
- **Test:** Runs tests on the built application/image.  
- **Deploy:** Deploys the application (e.g., runs the Docker container).

Each stage is automated by the Jenkins pipeline defined in the `Jenkinsfile`.

---

## How to Reproduce

1. Launch an AWS EC2 Ubuntu instance and SSH into it.
2. Install Jenkins and Docker.
3. Setup your GitHub repo with application code and a `Jenkinsfile`.
4. Create a Jenkins Pipeline job linked to your GitHub repo.
5. Configure webhook on GitHub to trigger Jenkins on commits.
6. Push code changes and observe Jenkins build and deploy automatically.

---

## Screenshots

| Step                  | Screenshot                                  |
|-----------------------|---------------------------------------------|
| EC2 Instance Running  | ![Instance](screenshots/instance.png)      |
| SSH Access            | ![SSH](screenshots/SSH-access.png)         |
| Jenkins Installation  | ![Step 1](screenshots/Jenkins-Installation-stp_l.png) <br> ![Step 2](screenshots/Jenkins-installation-stp_2.png) <br> ![Step 3](screenshots/Jenkins-Installation-stp_3.png) <br> ![Step 4](screenshots/Jenkins-Installation-stp_4.png) <br> ![Step 5](screenshots/Jenkins-Installation-stp_5.png) |
| GitHub Repo           | ![Repo Page](screenshots/Repo-Page.png)    |
| Jenkins Job Creation  | ![New Item](screenshots/Create_Jenkin-Newltem.png) <br> ![Config Step 1](screenshots/Pipeline-Config-Stp_I.png) <br> ![Config Step 2](screenshots/Pipeline-Config-Stp_2.png) |
| Jenkins Dashboard     | ![Dashboard](screenshots/Jenkins-Dashboard.png) <br> ![Job](screenshots/Jenkins-Job.png)     |
| Successful Build      | ![Build Success](screenshots/Build-Sucessful.png)        |

---

Thank you for exploring this Jenkins CI/CD pipeline demo!  
Feel free to reach out if you want to expand or customize this setup.

