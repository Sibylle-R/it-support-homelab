# IT Support Homelab

This repository documents my personal homelab projects with a clear focus
on entry-level IT Support and Service Desk tasks.

I built this lab alongside starting my HF Informatik studies to better
understand how day-to-day IT support actually works in real companies,
not just in theory.


## Why this homelab
Instead of only learning concepts, I wanted to work hands-on with a
realistic Windows environment. My goal is to become comfortable with
typical 1st level support tasks such as user issues, authentication
problems and basic troubleshooting.

## Environment
- Host OS: Windows 11 Pro  
- Virtualization: Hyper-V  
- Server: Windows Server 2022 Standard (Desktop Experience)  
- Client: Windows 11 Pro  
- Network: Internal Hyper-V Switch  


## Project 1: Active Directory – Base Setup

### Objective
Set up a basic Windows domain to understand how Active Directory is used
in everyday IT support scenarios.

### What I implemented
- Created a Hyper-V virtual machine (DC01)
- Installed Windows Server 2022
- Configured an internal virtual network
- Prepared the server to act as a Domain Controller

### Notes from the setup
During the initial setup I first used the default Hyper-V switch, but
quickly noticed that it does not reflect a typical company setup.
Switching to an internal network helped me better understand how clients
and servers communicate in a domain environment.

### Relevance for IT Support
Active Directory is central to most 1st level support tasks. User login
issues, password resets and access problems all depend on a correctly
configured domain controller.


## What I learned so far
- How important networking is for Active Directory
- Why many support issues are related to user accounts and permissions
- How a Domain Controller fits into a simple company IT setup


## Current status
- [x] Windows Server installed
- [ ] Active Directory configured
- [ ] Client joined to domain
- [ ] User and group management
