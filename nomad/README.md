# Job Deployment with Nomad

This project demonstrates a simple Nomad job deployment using Docker.

## Project Structure

```bash
nomad/
└── hello.nomad
Step 1: Create the Folder
mkdir nomad
Step 2: Create the Nomad Job File
touch nomad/hello.nomad
Step 3: Add the Nomad Job Configuration

Open nomad/hello.nomad and add:

job "hello-devops" {
  datacenters = ["dc1"]

  group "app" {
    task "hello" {
      driver = "docker"

      config {
        image = "devops-app"
      }

      resources {
        cpu    = 100
        memory = 128
      }
    }
  }
}
Step 4: Push Changes to GitHub

Add files:

git add .

Commit changes:

git commit -m "Added Nomad job"

Push to GitHub:

git push
Requirements
Nomad
Docker
Git
VS Code (optional)
Purpose

This setup deploys a Docker container using HashiCorp Nomad with minimal CPU and memory resources.