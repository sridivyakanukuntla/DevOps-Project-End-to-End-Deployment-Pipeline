# DevOps-Project-End-to-End-Deployment-Pipeline
## Overview
This project outlines the architecture and processes involved in setting up an end-to-end DevOps pipeline. It demonstrates a structured approach to automate the build, test, and deployment phases of an application with continuous monitoring and feedback.
## Pipeline process:
# Steps:
1.	Develop/Update Application: Develop/Update application and push the changes, along with source code to a private GitHub repository
2.	Pipeline Creation: Set up and configure the PIPELINE using JENKINS to automate the build, test and deployment stages.
3.	Source Code Compilation: Compile the source code to check for syntax errors within the pipeline
4.	Unit Testing: Execute unit tests to validate the functionality of the source code
5.	Code Quality Check (Sonar Qube): Use SONAR QUBE for code quality checks to detect bugs in source code
6.	Vulnerability Scan (Trivy tool): Perform vulnerability scan on source code to identify any sensitive data using TRIVY tool and it generates a report in html/txt file
7.	Build Application: Generate the application artifact after a successful build
8.	Artifact Management (Nexus): Publish the application artifact to the NEXUS repository to manage versioning.
9.	Docker Image Build: Build a Docker image and tag it.
10.	Docker Image Vulnerability Scan: Scan the DOCKER image to check for vulnerabilities in containers
11.	Push Docker Image: Push DOCKER image to a Docker Hub Repository
12.	Kubernetes Cluster Audit (Kube-Audit): Perform an audit of Kubernetes cluster to scan for any specific issues in cluster
13.	Application Deployment: Deploy the application to a Kubernetes cluster
14.	Deployment Verification: Verify Deployment status
15.	Pipeline Status Notification: Send an email notification with pipeline status(success or fail)
16.	Application Monitoring: Once application is deployed successfully monitoring is done in 2 ways:
i)	Website Level Monitoring  using BLACK BOX exporter to check website traffic and results are displayed in Grafana
ii)	System level monitoring to check CPU, RAM usage etc. 
17.	Jenkins Monitoring: Use NODE exporter to monitor Jenkins performance
## Project phases:
# PHASE1: Infrastructure Setup
Network Environment:
•	Private
•	Isolated
•	Security
Kubernetes Cluster:
•	Deploy application
•	Scan for vulnerability
Virtual Machines:
•	Set up dedicated servers for tools such as SONARCUBE and NEXUS
•	Install essentials tools-JENKINS, Monitoring tools
# PHASE 2: Version Control
GIT Repository (private)
•	Use a private repository to maintain source code
•	Repository visibility
•	Push Source code to GitHub
# PHASE 3: CI/CD Pipelines
•	Best practices for CI/CD pipeline setup
•	Implement security measures
•	Application deployment to cluster
•	Send mail Notification
# PHASE 4: Monitoring tools
•	System level Monitoring: Track CPU, RAM etc.
•	Website level Monitoring: Monitor website traffic and performance using Grafana.
