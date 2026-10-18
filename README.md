🚀 MERN DevOps Automation

A hands-on DevOps portfolio project by Muhammad Ahmad Raza

This project takes the original MERN Stack Employee Records application and extends it with containerization, cloud deployment, and DevOps automation.

The application was originally created by MongoDB Developer. My contribution focuses on the DevOps implementation and deployment workflow.

🎯 Project Goals

Containerize the frontend and backend using Docker.

Run the application services using Docker Compose.

Deploy the application to an AWS EC2 Linux instance.

Publish container images to Docker Hub.

Build a CI/CD workflow using GitHub Actions.

Implement secure AWS authentication with IAM OIDC and deployment management through AWS Systems Manager (SSM).

🛠️ Technology Stack

Tool

Purpose

React, Vite

Frontend application

Node.js, Express

Backend API

MongoDB

Application database

Docker

Containerization

Docker Compose

Multi-container management

Nginx

Frontend web server

Docker Hub

Container image registry

AWS EC2

Application hosting

GitHub Actions

CI/CD automation

AWS IAM OIDC

GitHub Actions authentication

AWS Systems Manager

Remote instance management

🏗️ Architecture

                 GitHub Repository
                        |
                        v
                 GitHub Actions
                        |
              Build and publish images
                        |
                        v
                    Docker Hub
                        |
              AWS OIDC / AWS SSM
                        |
                        v
                    AWS EC2
                        |
                   Docker Compose
                        |
              +---------+---------+
              |                   |
              v                   v
        React + Nginx       Node.js + Express
                                  |
                                  v
                               MongoDB

The diagram represents the intended automated deployment flow. Update it as the complete CI/CD pipeline is verified.

🐳 Docker Images

The project uses separate images for the frontend and backend.

Frontend: ahmad459/mern-devops-frontend

Backend: ahmad459/mern-devops-backend

☁️ AWS Deployment

The application has been deployed to an AWS EC2 Linux instance using Docker Compose.

The deployment work includes:

Running the application in containers.

Serving the frontend through Nginx.

Connecting the frontend to the backend API.

Running MongoDB as a containerized service.

Configuring EC2 network access and security-group rules.

🔄 CI/CD Automation

The project is being developed toward an automated deployment workflow using GitHub Actions, Docker Hub, AWS IAM OIDC, and AWS Systems Manager.

Planned workflow stages:

Trigger the workflow when changes are pushed to GitHub.

Build the frontend and backend images.

Push updated images to Docker Hub.

Authenticate to AWS using OIDC.

Trigger deployment commands through AWS Systems Manager.

Verify the updated services on EC2.

Status: Update this section when the end-to-end workflow has been successfully tested.

▶️ Run Locally with Docker Compose

Prerequisites

Git

Docker Desktop or Docker Engine

Docker Compose

1. Clone this repository

git clone https://github.com/Ahmad-000/mern-devops-automation.git
cd mern-devops-automation

2. Start the application

docker compose up -d --build

3. Check the containers

docker compose ps

4. View logs

docker compose logs -f

5. Stop the application

docker compose down

Use the ports configured in docker-compose.yml to access the application.

📂 Project Structure

mern-devops-automation/
├── mern/
│   ├── client/          # React frontend
│   └── server/          # Express API
├── docker-compose.yml
├── README.md
└── .github/
    └── workflows/      # GitHub Actions workflows, if configured

📚 Original Application

This project is based on the MERN Stack Example by MongoDB Developer.

Original repository

Original MERN tutorial

Original video walkthrough

The original application and its underlying code remain credited to their author. This repository documents my DevOps learning, infrastructure configuration, containerization, and deployment work.

👨‍💻 Author

Muhammad Ahmad Raza

GitHub: Ahmad-000

LinkedIn: Connect with me

⭐ This repository is part of my hands-on DevOps learning and portfolio journey.
