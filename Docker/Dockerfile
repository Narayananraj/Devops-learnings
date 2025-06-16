# 📝 Dockerfile Examples

A **Dockerfile** is a text document containing instructions to assemble a Docker image. This section provides basic to advanced examples for creating Docker images.

---

## 📌 Basic Dockerfile Structure

```Dockerfile
# Use an official base image
FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && apt-get install -y nginx

# Set environment variables
ENV MY_ENV_VAR=production

# Expose a port
EXPOSE 80

# Set default command
CMD ["nginx", "-g", "daemon off;"] 

--- 

📌 Simple Python App

ROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["python", "app.py"] 

---


📌 Node.js App

FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"] 

--- 

📌 Multi-stage Build (Go App)

# Build Stage
FROM golang:1.22 AS builder
WORKDIR /app
COPY . .
RUN go build -o app .

# Production Stage
FROM alpine:latest
WORKDIR /root/
COPY --from=builder /app/app .
EXPOSE 8080
CMD ["./app"]