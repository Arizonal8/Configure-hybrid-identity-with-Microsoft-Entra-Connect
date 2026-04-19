# DNS & Domain Configuration

## Overview

This section focuses on configuring DNS and setting up a custom domain in Microsoft Entra ID to enable hybrid identity.

---

## What This Does

* Adds custom domain (`arizaylab.tech`)
* Verifies domain ownership via DNS
* Enables domain usage for authentication

---

## Technologies Used

* Microsoft Entra ID
* DNS Management (GoDaddy/Namecheap/Cloudflare)
* Azure Portal

---

## Setup Steps

### 1. Add Custom Domain

* Go to Entra Admin Center
* Navigate to **Custom Domain Names**
* Add domain: `arizaylab.tech`

---

### 2. Verify Domain

* Add TXT record in DNS provider
* Example:

  * Name: @
  * Value: MS=xxxxxxx
* Click **Verify**

---

### 3. Set as Primary Domain

* Make `arizaylab.tech` primary

---

## Outcome

A verified domain ready for hybrid identity and user authentication.
