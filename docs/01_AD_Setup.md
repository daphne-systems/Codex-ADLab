# Active Directory Setup Guide

This document outlines the steps to set up an Active Directory (AD) domain on a Windows Server 2025 environment.

---

## 1. Prerequisites

Before starting, ensure:

- Windows Server 2025 is installed.
- Static IP is configured on the server.
- VMware/Hyper-V VM is ready (if using virtual machines).

---

## 2. Install Active Directory Domain Services (AD DS)

1. Open **Server Manager**.
2. Click **Manage → Add Roles and Features**.
3. In the wizard:
   - Choose **Role-based or feature-based installation**.
   - Select your server.
   - Check **Active Directory Domain Services**.
4. Click **Next → Install**.
5. Wait for installation to complete.

---

## 3. Promote Server to Domain Controller

1. In Server Manager, click the **flag notification** → **Promote this server to a domain controller**.
2. Select **Add a new forest** if this is the first DC.
3. Enter your **Root domain name** (e.g., `example.local`).
4. Set **Directory Services Restore Mode (DSRM) password**.
5. Review and confirm **installation options**.
6. Click **Install** and let the server restart.

---

## 4. Verify AD Installation

- Open **Active Directory Users and Computers**.
- Confirm your domain is listed.
- Create a test user to ensure AD is functional.

---

## 5. Configure DNS

- AD installation often configures DNS automatically.
- Verify DNS zones are correctly created.
- Ensure your server points to itself for DNS resolution.

---

## 6. Notes / Troubleshooting

- If the server fails promotion, check:
  - IP configuration (should be static)
  - Network connectivity
