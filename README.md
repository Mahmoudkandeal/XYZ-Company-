# XYZ Company 
**Prepared by:** Eng. Mahmoud Hamed Abdel Moniem
---
## Overview

This project focuses on setting up and configuring a basic internal server for XYZ Company. It includes IP configuration, hostname setup, user management, permission controls, Apache web server installation, and testing website accessibility.

---

## 🖧 IP Address Configuration (`nmcli` & `ip add`)

Configuring the IP address is crucial to allow the server to communicate with other devices in the internal network.  
We used:

- `nmcli` to modify the network interface and assign a static IP.  
- `ip add` to verify the assigned IP address.

![IP Configuration](images/1.png)

---

## 🖥️ Hostname Configuration (`hostnamectl`)

Setting the correct hostname helps easily identify the server on the network.

- The hostname was set using: `hostnamectl set-hostname internal.xyz.local`

![Hostname Configuration](images/2.png)

---

## 📄 Edit `/etc/hosts` File

The `/etc/hosts` file maps the hostname to the IP address locally.  
This simulates DNS functionality so users can access the site via a name instead of an IP.

![Hosts File](images/3.png)

---

## 👥 Check Created Users (`cat /etc/passwd`)

Created users for role-based access:

- `admin1`
- `developer1`
- `viewer1`

Each has specific access permissions for better security and control.

![Users](images/4.png)

---

## 🔐 Check Sudo Privileges (`sudo -l -U admin1`)

To ensure `admin1` can perform administrative tasks, we checked sudo privileges:

- Added `admin1` to the `wheel` group.

![Sudo Check](images/5.png)

---

## 📁 Verify Directory Permissions

- `developer1` has write access to website directory.
- `admin1` has access to shared files.
  
Commands used:

- `chown` – Change file ownership  
- `chmod` – Set file permissions

![Permissions](images/6.png)
![Permissions](images/7.png)
![Permissions](images/8.png)

---

## 🌐 Check Apache Service Status

Apache installation and status verification:

![Permissions](images/9.1.png)
![Permissions](images/9.png)
---

## 🌐 Using Hosts file to check from the host

![Permissions](images/10.png)
![Permissions](images/11.png)
