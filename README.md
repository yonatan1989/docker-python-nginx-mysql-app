# Python Application with Nginx Load Balancer and MySQL Database

This project sets up a Python web application with an Nginx load balancer, running in Docker containers using Docker Compose.

## Features
1. **Python Web Application**:
   - Route `/`: 
     - Sets a cookie with the internal IP for 5 minutes.
     - Logs client IP, date, and time to a MySQL table (`access_log`).
     - Returns the server's internal IP to the browser.
   - Route `/showcount`:
     - Displays a global counter.

2. **Nginx Load Balancer**:
   - Routes traffic to the application containers (3 replicas).
   - Implements stickiness using cookies (users stick to the same server for 5 minutes).

3. **MySQL Database**:
   - Retains data and logs after container stops.

4. **Scalability**:
   - Includes a Bash script to scale the application up or down (e.g., to 5 replicas).

## Requirements
- Docker and Docker Compose installed.

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>


This document assumes a repository structure with the necessary files (e.g., `Dockerfile`, `docker-compose.yml`, `nginx.conf`, `scale.sh`) and provides a concise overview for users.
