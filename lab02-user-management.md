# Lab 02 - User Management and Permissions

## Objective 
Create and manage users, groups and file permissions on Ubuntu Server 24.04

## Commands Used
sudo adduser labuser
sudo groupadd labgroup
sudo usermod -aG labgroup labuser
groups labuser
sudo touch /home/labuser/testfile.txt
sudo chmod 640 /home/labuser/testfile.txt
sudo chown labuser:labgroup /home/labuser/testfile.txt
sudo deluser labuser

## Key Concepts
- adduser: creates a new user
- groupadd: creates a new group
- usermod -aG: adds a user to a group
- chmod: changes file permissions
- chown: changes file owner and group
- deluser: removes a user

## Result
Successfully created a user, assigned them to a group, set a file permisssions, and removed the user
