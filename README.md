# Python App Deployment using Jenkins Pipeline (2-Server Architecture)
# Project Overview
This project demonstrates CI/CD automation by deploying a Python application using Jenkins Pipeline on a remote server using SSH credentials.

# Architecture:
- Server 1: Jenkins Server (CI/CD)
- Server 2: Python Application Server (Deployment Target)

<img width="1262" height="749" alt="image" src="https://github.com/user-attachments/assets/0d151ba8-ce89-4c98-985f-1fdff683591e" />

# Tech Stack
- Jenkins (Pipeline)
- Git & GitHub
- Python 3
- SSH (Private Key Authentication)
- Linux (Ubuntu Server)
- CI/CD Pipeline
#  Pipeline Stages
1. Checkout Code from GitHub
2. Clone Repository
3. Deploy to Remote Python Server (via SSH)
4. Install Dependencies
5. Run Python Application

# Credentials Used
- Jenkins Credentials ID: `node-app-key`
- Type: SSH Username with Private Key
- Used for secure deployment to remote server

Create a credentials in jenkins using python server ip and Private key
<img width="1642" height="768" alt="image" src="https://github.com/user-attachments/assets/07e45340-f6da-46d0-999f-39d870dc451e" />
<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/310e6f0e-270a-4b5b-b48b-76e650882239" />


# Jenkins Pipeline Configuration

pipeline {
    agent any

    environment {
        SSH_CRED = 'node-app-key'
        SERVER_IP = '13.48.24.75'
        REMOTE_USER = 'ubuntu'
        APP_DIR = '/home/ubuntu/pythonapp'
    }

    
# agent any

This tells Jenkins to run the pipeline on any available Jenkins agent (node).
It means the job is not restricted to a specific server.

# environment { }

The environment block is used to define global variables that are reused across all pipeline stages.
SSH_CRED: Jenkins stored credential ID (SSH private key) used for secure server access
SERVER_IP: Remote Python server IP address where the app will be deployed
REMOTE_USER: Username of the target server (Ubuntu in this case)
APP_DIR: Directory path on the remote server where the application will be stored

# This makes the pipeline more secure, reusable, and easy to maintain.

# Key Learning Outcomes

- CI/CD Pipeline Implementation
- GitHub Integration with Jenkins
- SSH-based Secure Deployment
- Multi-stage Pipeline Execution
- Real-world DevOps workflow

# Sucessfully build and deploy
<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/8ad14d7f-da31-42aa-b5a1-9d6e50f80330" />
<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/f92ccf44-ad74-4589-afc7-c2615fe03fa2" />
# Hit python server IP with 5000 port 
<img width="1920" height="1008" alt="image" src="https://github.com/user-attachments/assets/4b51b83e-8fc2-4cb0-a9f2-5606382b964e" />


##  Author

Megha Patil  
DevOps & Cloud Enthusiast  
