---
title: WSL 2
published: 2024-11-01
description: 'Setup WSL-2 On Windows 11'
image: './wsl2.jpg'
tags: [windows subsystem linux]
category: 'wsl'
draft: false 
lang: 'en'
---

# How to install Linux on Windows with WSL

## Turn Windows features on or off
- Enable Virtual Machine Platform and Windows Subsystem For Linux
![turnon](./turn-on.png)
:::important
You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11 to use the commands below.
:::

```bash
wsl --install
```
or you can install on microsoft store
![ms-store](./ubuntu-store.png)

## Check Your WSL Running Or Not
```bash
wsl -l -v
```
![wslrun](./wsl-chck-run.png)

## Upgrade version from WSL 1 to WSL 2

:::important
To set the default version to WSL 1 or WSL 2 when a new Linux distribution is installed
:::
```bash
wsl --set-version Ubuntu-20.04 2
```

# Done Your WSL now is version 2