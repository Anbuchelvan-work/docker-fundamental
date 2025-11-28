# Docker Basics — Day 1

## What is Docker?
A platform that allows you to build, run, and ship applications inside containers.

## Key Concepts
- Image → a packaged application
- Container → a running instance of an image
- Dockerfile → file used to build images
- Docker Hub → public image registry

## Basic Commands
- docker --version  
- docker pull <image>  
- docker run <image>  
- docker ps  
- docker stop <container>  
- docker rm <container>

## Notes
- Containers are lightweight and portable.
- Docker eliminates the "works on my machine" problem.

## Dockerfile Basics

A **Dockerfile** is a set of instructions used to build a Docker image.

### Common Dockerfile Instructions

#### FROM — base image
```
FROM python:3.10
```

#### WORKDIR — set working directory
```
WORKDIR /app
```

#### COPY — copy files into image
```
COPY . /app
```

#### RUN — execute commands during build
```
RUN pip install -r requirements.txt
```

#### CMD — run container command
```
CMD ["python", "app.py"]
```

### Example Dockerfile
```
FROM python:3.10
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
CMD ["python", "app.py"]
```

### Notes
- Dockerfile builds → create images
- Containers run **from** images
- Each instruction creates a new layer
- Keep Dockerfiles small and clean
