Dockerized Python App

 Overview

This project demonstrates how to run a simple Python application inside a Docker container.

Containerization allows applications to run consistently across different environments without installing dependencies directly on the host machine.

 Technologies Used

 Python
 Docker
 Git
 GitHub

 Project Structure

dockerized-python-app
│
├── app.py
├── Dockerfile
└── README.md

 Application Code

 app.py


print("Hello DevOps from Docker")

This simple Python script prints a message when executed.


 Dockerfile

FROM python:3.10
COPY app.py .
CMD ["python", "app.py"]

 Explanation

 **FROM python:3.10**
  Uses an official Python image as the base environment.

 **COPY app.py .**
  Copies the Python script into the container.

 **CMD ["python", "app.py"]**
  Runs the Python application when the container starts.


 Build the Docker Image

Run the following command in the project directory:

docker build -t dockerized-python-app .


This command builds a Docker image for the application.


 Run the Container

```
docker run dockerized-python-app
```

Expected output:

```
Hello DevOps from Docker
```

 What I Learned

* How to containerize a Python application
* How to write a Dockerfile
* How to build Docker images
* How to run applications inside containers

 Author

DevOps Learning Project
