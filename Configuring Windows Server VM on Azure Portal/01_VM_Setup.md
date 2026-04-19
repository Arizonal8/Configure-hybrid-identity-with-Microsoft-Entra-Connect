# Azure VM Setup (Windows Server)

## Overview

This section covers the deployment of a Windows Server virtual machine in Microsoft Azure, which serves as the foundation for building an on-premises Active Directory environment.

---

## What This Does

* Creates a Windows Server VM in Azure
* Configures networking and remote access (RDP)
* Prepares the environment for Active Directory installation

---

## Technologies Used

* Microsoft Azure
* Azure Virtual Machines
* Windows Server 2022
* Remote Desktop Protocol (RDP)

---

## Setup Steps

### 1. Create Virtual Machine

* Navigate to Azure Portal
* Select **Create → Virtual Machine**
* Choose:

  * Image: Windows Server 2022
  * Size: B2s (or similar)

---

### 2. Configure Networking

* Enable Public IP
* Allow inbound port:

  * **RDP (3389)**

---

### 3. Connect to VM

* Download RDP file
* Login using admin credentials

---

## Outcome

A fully functional Windows Server VM ready for Active Directory configuration.
