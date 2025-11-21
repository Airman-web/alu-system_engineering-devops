Web Stack Debugging #0 — Give Me a Page

This project introduces web stack debugging using a broken Docker container. The goal is to diagnose why the web server inside the container is not returning a page and fix it using only command-line operations.

 Objective

Inside the provided Docker container (holbertonschool/265-0), Apache is not serving any content on port 80.
The task is to restore the web server and make it serve a page containing:

Hello Holberton

 What I Did

Installed Apache (missing in the container)

Started the Apache service

Replaced the default index page with one containing the required text

Ensured the server successfully responds on port 80 when curled

Files

0-give_me_a_page
A Bash script that:

Installs Apache

Starts the service

Creates an index page containing Hello Holberton

Usage

Run the container:

docker run -p 8080:80 -d -it holbertonschool/265-0


Enter it:

docker exec -ti <container_id> bash


Then execute:

./0-give_me_a_page


Test from your machine:

curl 0:8080


You should see:

Hello Holberton
