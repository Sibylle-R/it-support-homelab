# IT Support Homelab

This repo contains my personal homelab setup.

I use it to practice basic IT support and Active Directory tasks.
Nothing groundbreaking, just a small lab to understand how things actually work.

I started this lab befor I began my HF Informatik studies.
I noticed that many concepts only really make sense once you set them up yourself,
break things, and fix them again.

This lab is mainly focused on:
- basic Windows Server setup
- Active Directory fundamentals
- typical first level support scenarios

## Environment
- Host OS: Windows 11 Pro  
- Virtualization: Hyper-V  
- Server: Windows Server 2022 Standard (Desktop Experience)  
- Client: Windows 11 Pro  
- Network: Internal Hyper-V Switch  


## Project 1: Active Directory – Base Setup

### Objective
Set up a small Windows domain to get a better feeling for how Active Directory
is actually used.

### What I implemented 
- Created a Hyper-V virtual machine (DC01)
- Installed Windows Server 2022
- Set up an internal Hyper-V network
- Basic server preparation before installing Active Directory


### Relevance for IT Support
Active Directory plays a big role in daily IT support.
Many common issues like login problems, password resets or missing access
are directly related to the domain controller.


## What I learned so far
- How important basic networking is for Active Directory
- Why many support issues are actually user or permission related
- How a Domain Controller fits into a small company IT setup

## Current Progress

- [x] Hyper-V virtual machine created (DC01)
- [x] Windows Server 2022 installed
- [x] Server renamed to DC01
- [x] Static IP and DNS configured
- [ ] Active Directory Domain Services installed
- [ ] Domain created
- [ ] Client joined to domain
- [ ] User and group management

This lab is still work in progress and will be extended step by step.
