# Frontend Website Deployment using Docker and Amazon EC2

## Project Overview

This project demonstrates how to deploy a static frontend website using Docker, Nginx, GitHub, and Amazon EC2.

## Repository Link

GitHub Repository:
https://github.com/umeshkumargadapa/docker-frontend-website

## Technologies Used

* HTML
* CSS
* JavaScript
* Docker
* Nginx
* Git
* GitHub
* Amazon EC2

## Website Features

* Home Section
* About Section
* Services Section
* Contact Section
* Responsive Design
* Docker Container Deployment

## Project Structure

docker-frontend-website/

├── Dockerfile

├── index.html

├── style.css

└── README.md

## Dockerfile

```dockerfile
FROM nginx:latest

COPY . /usr/share/nginx/html

EXPOSE 80
```

## Deployment Steps

### Step 1: Clone Repository

```bash
git clone https://github.com/umeshkumargadapa/docker-frontend-website.git
cd docker-frontend-website
```

### Step 2: Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
```

### Step 3: Build Docker Image

```bash
sudo docker build -t frontend-site .
```

### Step 4: Run Docker Container

```bash
sudo docker run -d -p 80:80 --name website frontend-site
```

### Step 5: Verify Running Container

```bash
sudo docker ps
```

### Step 6: Access Website

Open the browser:

http://16.112.31.29

## Docker Commands

### List Containers

```bash
sudo docker ps
```

### Stop Container

```bash
sudo docker stop website
```

### Start Container

```bash
sudo docker start website
```

### Restart Container

```bash
sudo docker restart website
```

### Remove Container

```bash
sudo docker rm website
```

### View Logs

```bash
sudo docker logs website
```

## Update Application Workflow

### Local Machine

```bash
git add .
git commit -m "Website Updated"
git push
```

### EC2 Server

```bash
git pull

sudo docker stop website
sudo docker rm website

sudo docker build -t frontend-site .

sudo docker run -d -p 80:80 --name website frontend-site
```

## Architecture Diagram

Developer

↓

GitHub Repository

↓

Amazon EC2

↓

Docker Container

↓

Nginx

↓

Frontend Website

## Screenshots Included

* EC2 Instance
* Docker Image
* Running Container
* Website Home Page
* Docker Logs
* Updated Website After Git Pull

## Author

Umesh Kumar

GitHub:
https://github.com/umeshkumargadapa

Repository:
https://github.com/umeshkumargadapa/docker-frontend-website
