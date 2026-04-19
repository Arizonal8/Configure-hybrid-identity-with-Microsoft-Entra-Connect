# Windows Server & Active Directory Configuration

## Overview

This section covers installing and configuring Active Directory Domain Services (AD DS) on the Windows Server VM.

---

## What This Does

* Installs Active Directory
* Promotes server to Domain Controller
* Creates internal domain (`arizaylab.local`)
* Creates users for synchronization

---

## Technologies Used

* Windows Server 2022
* Active Directory Domain Services (AD DS)
* DNS Server

---

## Setup Steps

### 1. Install AD DS

* Open Server Manager
* Add Roles:

  * Active Directory Domain Services

---

### 2. Promote to Domain Controller

* Create new forest:

  * `arizaylab.local`
* Set DSRM password

---

### 3. Create Users

* Open **Active Directory Users and Computers**
* Create test users

---

### 4. Configure UPN Suffix

* Add:

  * `arizaylab.tech`
* Update users to match cloud domain

---

## Outcome

A fully configured on-premises Active Directory environment.
