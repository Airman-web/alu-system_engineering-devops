Web Stack Debugging #1 — Nginx Likes Port 80
🔹 Overview

This project trains debugging skills for web stacks. In this task, a Docker container with Ubuntu has Nginx installed but not serving requests on port 80. The goal is to fix the container so that Nginx runs properly and listens on all active IPv4 addresses on port 80.

🔹 Objective

Ensure Nginx is installed.

Start Nginx so it listens on port 80.

After running the script, curling the container root returns the default Nginx page.

🔹 Solution

The provided Bash script 0-nginx_likes_port_80:

Updates the package list.

Installs Nginx if not present.

Starts the Nginx service.

After execution, curl 0:80 returns the Nginx welcome page, confirming the web server is running.

🔹 Files

0-nginx_likes_port_80 – Bash script that fixes the web stack.

#!/usr/bin/env bash
# Ensure Nginx is installed and listening on port 80

apt-get update
apt-get install -y nginx
service nginx start

🔹 Usage

Run the container:

docker run -p 8080:80 -d -it ubuntu:16.04


Copy the script into the container or mount it.

Execute:

./0-nginx_likes_port_80


Test:

curl 0:80


You should see the default Nginx welcome page.