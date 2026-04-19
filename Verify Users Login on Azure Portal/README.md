# Hybrid Identity with Microsoft Entra Connect

## Overview

This section connects on-premises Active Directory with Microsoft Entra ID using Microsoft Entra Connect.

---

## What This Does

* Syncs users from AD to Entra ID
* Enables hybrid identity
* Implements Password Hash Synchronization

---

## Technologies Used

* Microsoft Entra ID
* Microsoft Entra Connect Sync
* Azure AD Connect
* PowerShell

---

## Setup Steps

### 1. Install Entra Connect

* Download from Entra Admin Center
* Select **Custom Installation**

---

### 2. Configure Authentication

* Choose:

  * Password Hash Synchronization (PHS)

---

### 3. Connect Directories

* Sign in with Entra Admin account
* Connect on-prem AD

---

### 4. Configure Sync

* Select Users OU
* Enable Password Writeback (optional)

---

### 5. Run Sync

* Start initial synchronization

---

## Verification

* Go to Entra ID → Users
* Confirm:

  * **On-premises synced = Yes**

---

## Outcome

A working hybrid identity environment with synchronized users across on-prem and cloud.
