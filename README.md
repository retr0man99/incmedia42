CI/CD and Deployment Setup for incmedia42

This repository contains the configuration files and instructions for setting up Continuous Integration (CI), Continuous Deployment (CD), and deployment logic for the incmedia42 project. The project consists of independent components developed in Go, Next.js (TypeScript), and WordPress.

Components
1. Go Application (go-app)

CI Workflow (go_ci.yml)
The CI workflow for the Go application includes the following steps:

Checkout code
Set up Go environment
Install dependencies
Run tests
Run linter
Create Docker image
Trigger deployment if successful

2. Next.js Application (nextjs-app)

CI Workflow (nextjs_ci.yml)
The CI workflow for the Next.js application includes the following steps:

Checkout code
Set up Node.js environment
Install dependencies
Run linter
Run unit tests
Create Docker image
Trigger deployment if successful

3. WordPress Application (wordpress-app)

CI Workflow (wordpress_ci.yml)
The CI workflow for the WordPress application includes the following steps:

Checkout code
Set up PHP environment
Install dependencies
Run coding standards check
Create Docker image
Trigger deployment if successful

4. Deployment Action
The deploy.yml workflow in the main repository incmedia42 is responsible for deploying the Go, Next.js, and WordPress components to a staging environment if all CI workflows are successful.

Deployment Logic
The deployment logic checks the status of the CI workflows for each component and triggers deployment only if all workflows are successful.

5. Docker Compose file can be used to spin up the entire
extended application stack locally.