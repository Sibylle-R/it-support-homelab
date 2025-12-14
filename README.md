# IT Support Homelab

This repo contains my personal homelab setup.

I use it to practice basic IT support and Active Directory tasks.
Nothing groundbreaking, just a small lab to understand how things actually work.

I started this lab befor I began my HF Informatik studies.
I noticed that many concepts only really make sense once you set them up yourself,
break things, and fix them again.

This lab is focused on:
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
Set up a small Windows domain to understand and get a better feeling for how it is actually used.

### What I implemented so far
- Created a Hyper-V virtual machine (DC01)
- Installed Windows Server 2022
- Set up an internal Hyper-V network
- Basic server preparation before installing Active Directory

### Verification after Domain Promotion

After the reboot, I verified that the server was successfully promoted to a Domain Controller:

- Server name is set to DC01
- Active Directory Users and Computers console is available
- DNS Server role is installed and running
- Domain services are active and accessible

This confirmed that the domain controller is working as expected.

### User creation
Created a test domain user in ADUC to simulate common IT support tasks (account setup, password resets, group membership).

### Group management

Created a security group (IT-Support) and added the test user to it.

## Client setup Windows 11

A Windows 11 client virtual machine (CLIENT01) is currently being installed.
This client will later be joined to the domain to test typical domain login
and user management scenarios.

Notes:
The client setup took a bit longer due to TPM requirements in Hyper-V and also since Windows 11 wants you to connect isntantly to the internet
I had to use a small workaround. OOBE\BYPASSNRO 

### Client domain join

A Windows 11 client (CLIENT01) was configured with the domain controller as DNS server and successfully joined to the lab.local domain.

### Domain login test

I managed to log in with Max Muster as a User in to Windows 11 client using domain credentials.
This verified correct DNS resolution and authentication against the domain controller.


### Group Policy troubleshooting

Initially, the policy did not apply because it was linked to a computer OU
while configuring a user-based policy. After moving the domain user into
a dedicated user OU and linking the GPO correctly, the policy applied as expected.


### Group Policy test (User restrictions)

After logging in with a domain user on the Windows 11 client, access to the
Control Panel was successfully blocked, confirming that the policy was applied
correctly.


## What I learned


## Current Progress

- [x] Hyper-V virtual machine created (DC01)
- [x] Windows Server 2022 installed
- [x] Server renamed to DC01
- [x] Static IP and DNS configured
- [x] Active Directory Domain Services installed
- [x] Domain created
- [x] Client joined to domain
- [x] User and group management

This lab is still work in progress and will be extended step by step.
