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


