# Lab 04 - Firewall Setup with UFW

## Objective
Configure UFW firewall on Ubuntu Server 24.04 to control inbound traffic

## Commands Used
sudo ufw status
sudo ufw allow ssh
sudo ufw allow 80
sudo ufw deny 23
sudo ufw enable

## Key Concepts
- UFW = Uncomplicated Firewall
- Always allow SSH before enabling firewall or you lock yourself out
- Default policy blocks all incoming traffic not explicitly allowed
- Allow only ports you need, deny everything else

## Firewall Rules Configured
- Port 22 (SSH) - ALLOW
- Port 80 (HTTP) - ALLOW
- Port 23 (Telnet) - DENY

## Result
Firewall enabled with only necessary ports open. All other traffic blocked by default.
