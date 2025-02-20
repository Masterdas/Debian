# Debian Full Setup in Termux
---
## **Installation Steps**
### **1. Update & Upgrade Packages**
```
pkg update && pkg upgrade -y
```

### **2. Install `proot-distro`**
```
pkg install proot-distro -y
```

### **3. Check Available Distributions**
```
proot-distro list
```

### **4. Install Debian**
```
proot-distro install debian
```

### **5. Login to Debian**
```
proot-distro login debian
```

### **6. Login as Root User (Optional)**
```
proot-distro login --user root debian
```

### **7. Update & Upgrade Debian Packages**
```
apt update && apt upgrade -y
```

### **8. Install `sudo`, `wget`, and `git`**
```
apt install sudo wget git -y
```

### **9. Create a New User (Optional)**
```
adduser master
```

### **10. Edit sudoers File (Optional)**
```
nano ../etc/sudoers
```
(Add the necessary permissions for the user.)

---
## **Shortcut Commands**
To simplify logging into Debian, create shortcuts:

### **Shortcut for Normal User Login**
```
nano ~/.bashrc
```
Add this line at the end of the file:
```
alias debian="proot-distro login debian"
```
Save and exit, then apply the changes:
```
source ~/.bashrc
```
Now, simply type:
```
debian
```
To start Debian.

### **Shortcut for Root User Login**
```
nano ~/.bashrc
```
Add this line at the end of the file:
```
alias root="proot-distro login --user root debian"
```
Save and exit, then apply the changes:
```
source ~/.bashrc
```
Now, simply type:
```
root
```
To login as the root user.

---
## **Uninstall Debian**
If you want to remove Debian from Termux:
```sh
proot-distro remove debian
```

---
## **Credits by Mahadeb**
This guide was created to help users set up Debian in Termux easily.

