# Auro Installer

This repository is used to host the official Windows installer for the **Auro** application.

> 🚫 No source code is included in this repository.  
> 🔐 This is intentional for security and privacy purposes.

---

## 📑 Table of Contents

- [📦 Download](#-download)
- [📋 What is Auro?](#-what-is-auro)
- [✅ Installation Instructions](#-installation-instructions)
- [🛡️ Grant SQL Server Permission to Write Backups to OneDrive](#️-grant-sql-server-permission-to-write-backups-to-onedrive)
  - [✅ Steps to Grant Full Control to SQL Server](#-steps-to-grant-full-control-to-sql-server)
- [🔒 Security Notice](#-security-notice)
- [📫 Support](#-support)

---

## 📦 Download

Latest version of the Auro installer:

👉 [Download Auro Setup 1.0.5](https://github.com/jon4thanDev/auro-installer/releases/download/auro/auro.Setup.1.0.5.exe)

_Make sure to only download installers from this official repository to avoid tampered versions._

---

## 📋 What is Auro?

**Auro** is a desktop application designed to create automation for creating Microsoft SQL Server database backup and compression.

## Features

- Backup automation
- Backup manual
- Cleanup automation
- Cleanup manual

---

## ✅ Installation Instructions

1. Click the download link above.
2. Run the installer.
3. Follow the on-screen instructions.
4. Done — Auro will be ready to use!

---

## 🛡️ Grant SQL Server Permission to Write Backups to OneDrive

If you're backing up your SQL Server database to a OneDrive folder (e.g. `C:\Users\USERNAME\OneDrive\Backups`) and encounter an error like:

follow the steps below to fix the permissions issue.

### ✅ Steps to Grant Full Control to SQL Server

1. **Open Folder Security Settings**

   - Navigate to the folder: `C:\Users\YOUR_USERNAME\OneDrive\Backups`
   - Right-click the folder and select **Properties**
   - Go to the **Security** tab
   - Click **Edit...**

2. **Add SQL Server Service User**

   - Click the **Add...** button
   - In the object name field, enter:
     ```
     NT SERVICE\MSSQL$MSSQLSERVER01
     ```
     > Replace `MSSQLSERVER01` with your actual SQL Server instance name
   - Click **Check Names**
     - It should underline or auto-correct if valid
   - Click **OK**

3. **Grant Full Control**

   - Select the newly added user (`NT SERVICE\MSSQL$MSSQLSERVER01`)
   - In the permissions box, check ✅ **Full Control**
   - Click **Apply**, then **OK**

4. **Restart SQL Server**
   - Press `Win + R`, type `services.msc`, and hit **Enter**
   - Find **SQL Server (MSSQLSERVER01)** in the list
   - Right-click and choose **Restart**

---

After following these steps, your database backup should succeed and be saved in your OneDrive backup folder without access issues.

## 🔒 Security Notice

- This repo contains **only the official installer**.
- The source code is hosted privately and not available to the public at this time.
- All releases are created and signed by the original developer: **[@jon4thanDev](https://github.com/jon4thanDev)**.

---

## 📫 Support

If you experience any issues with the installation or app, feel free to [open an issue](https://github.com/jon4thanDev/auro-installer/issues) or contact me via [GitHub](https://github.com/jon4thanDev).

---
