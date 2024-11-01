---
title: Alibaba Cloud Setup ECS
published: 2024-10-11
description: Using ECS on alibaba cloud for deploying a code
tags: [alibaba, cloud]
category: Cloud
draft: false
---


# What is Alibaba Cloud?
Alibaba Cloud is a cloud computing service provider from Alibaba Group, offering a wide range of cloud solutions, including data storage, databases, networking, artificial intelligence, and security. Known as one of the largest cloud providers in Asia, Alibaba Cloud provides infrastructure and digital tools for businesses to efficiently build and manage scalable applications.

## Create Instance
- Select Operating System.
- Choose Ubuntu.
:::note
I Use Ubuntu V.16.04 64bit.
:::

## Security Group
:::important
On security group try enable or check the HTTPS (TCP:443) and HTTP (TCP:80)
:::
![security-group](./alibaba-security.png)

## Management
- Logon Credential you can choose custom password 

![logon](/src/content/posts/alibaba-image/management.png)

- You can finish your order


# ECS

## Use ssh
![connect](/src/content/posts/alibaba-image/ssh.png)
:::tip
if you wanna use ssh instead of Remote connection from alibaba you can use ssh
:::

```bash
ssh root@your-public-ip
```
and then insert custom password you make on Logon Credential
![security-group](/src/content/posts/alibaba-image/terminal-ssh.png)


## Use Terminal On alibaba cloud
![connect](/src/content/posts/alibaba-image/ssh.png)
- You can click Connect
![remote-conect](/src/content/posts/alibaba-image/remote-con.png)
- Click Sign in now
![terminal-1](/src/content/posts/alibaba-image/terminal-1.png)
:::note
Connection use ip public
:::
- and then insert your password

# Terminal
first thing first you can update your ubuntu 
```bash
apt-update
```

## Install Nginx
installing nginx on your server
```bash
sudo apt install nginx -y
```

## Uploading file to server
Uploading file or folder,i choose github because is familiar for me.
- installing git into your server
```bash
apt install git
```
- make a repository on your github

### You can move into terminal and then copy this

```bash
cd /var/www/html
```
### Clone your repository

```bash
git clone https://github.com/your/repository
```

# Configure Nginx
- on your terminal type this

You can use Vim
```bash
vim /etc/nginx/sites-available/default
```
or Nano
```bash
nano /etc/nginx/sites-available/default
```

## Configure using nano
![nano](/src/content/posts/alibaba-image/nginx-conf-nano.png)
:::tip
Use your arrow key for move the cursor
:::

on the config you can see **root /var/www/html/yourprojectname;**

and then **Write Out** by type combination **CTRL + O**
![nano-write](/src/content/posts/alibaba-image/nano-write.png)
if you see this file name to write you can hit **enter**

To EXIT nano type Combination key CTRL + X

## Restart Nginx
Restart Nginx by type this
```bash
sudo systemctl restart nginx
```

# Accses The Website
![ip](/src/content/posts/alibaba-image/alibaba-instance.png)
On instance you can copy the public ip into your search bar.
congratulations your website running on alibaba cloud using ECS









