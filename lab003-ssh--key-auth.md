# Lab 03 - SSH Key Authetication

## Objective
Set up SSH key authentication on Ubuntu Server 24.04 for more secure remote access 

## Steps
1. Generated SSH key pair Windows client 
2. Coped public key to a server authorized_keys file
3. Set correct permissions on authorized_keys
4. Disabled password authentication in sshd_config
5. Verified passwordless SSS logi works

## Commands Used
# On Windows
ssh-keygen -t ed25519 -C "email@example.com"

# On Linux Server
mkdir -p /home/justsolon/.ssh
chmod 700 /home/justsolon/.ssh
nano /home/justsolon/.ssh/authorized_keys
chmod 600 /home/justsolon/.ssh/authorized_keys
sudo nano /etc/ssh/sshd_config
sudo systemctl restart ssh

## Key Concepts
- Public key goes on the server (authorized_keys)
- Private key stays on your machine (never share this)
- chmod 600 on authorized_keys locks it to owner only
- PasswordAuthentication no disables password login

## Result
Successfully configured SSH key authentication. Server only accepts key based login, password login disabled.
