---
layout: post
title:  "Creating a virtual machine (ubuntu) with virtual box"
date:   2022-07-11 16:52:06 +0800
categories: cs_learning
---
Yesterday, I created a virtual machine for ubuntu system using VirtualBox.
1. Download the iso file of the operating system:
![ubuntu.iso](https://user-images.githubusercontent.com/60023638/178227735-87d4dc0a-1926-45e4-86a1-8e09f5452ab7.png)
2. Open VirtualBox, then choose the corresponding operating system:
![VirtualBox1](https://user-images.githubusercontent.com/60023638/178228102-10852f20-308e-4387-897b-616d5f30d79a.png)
3. Mount the iso file on VirtualBox:
![VirtualBox](https://user-images.githubusercontent.com/60023638/178228343-78ea470c-37b3-4726-ab43-eda03661dfde.png)
4. Format the disk space.
5. Complete the regualr settings.
6. Set network adapters:
   _ there can be multiple adapters
   _ For my virtual machine, one adapter is used for NAT, the other one is used to connect to the host through ssh
   ![image](https://user-images.githubusercontent.com/60023638/178288696-2ebb5253-85d5-41f3-933a-73754464c2d0.png)
7. remotely connect to the virtual machine through ssh:
   On host system, search for folder _.ssh_ . There should be a public key _id_rsa.pub_ .
   Then open it either using 
   ```
   cat id_rsa.pub
   ```
   or
   ```
   vim id_rsa.pub
   ```
   Switch to the virtual machine, again, find _.ssh_ folder and open it with
   ```
   vim authorized_keys
   ```
   and paste the public key to the file, then save and close the file with
   ```
   :wq [ENTER]
   ```
8. Use
   ```
   ip a
   ```
   to chech the ip address of the virtual machine, and connect to the virtual machine through ssh remotely.
