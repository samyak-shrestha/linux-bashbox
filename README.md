# 🧰 Bash Toolkit

A collection of **reusable Bash scripts** to automate common Linux tasks like installing `.tar.gz` apps, creating desktop entries, managing system utilities, and enhancing the command-line experience.

---

## 🚀 Features

- 🔧 Install `.tar.gz` GUI applications like Android Studio or PyCharm
- 🖼️ Automatically detect and create `.desktop` entries with icons
- 📈 Extract files with progress bars or fallback spinners
- 📂 Organize and move apps into `/opt`
- ⚙️ Choose launchers and icons from extracted files
- 🧪 Easily extendable with more Linux automation scripts

---

## 📦 Scripts Included

| Script Name         | Description                                                      |
|---------------------|------------------------------------------------------------------|
| `register-bash` | Register scripts as system-wide commands and manage aliases interactively.   |
| `install-tarapp` | Installs `.tar.gz` apps to `/opt`, creates `.desktop` launcher   |
| `update-system.sh`  | (Coming Soon) Updates packages and performs system cleanup       |

---

## 📋 Usage

### 📥 Clone the Repository
```bash
git clone git@github.com:samyak-shrestha/linux-bashbox.git
cd linux-bashbox
chmod +x ./register-bash

```

### Run a Script
```bash
./register-bash
```


### 🧠 Why This Toolkit?

Installing .tar.gz apps or doing system tweaks manually every time is repetitive. This repo provides:

- 🚀 Fast, reusable tools
- 🐧 Linux-focused automation
- 🧰 Scripts anyone can use or extend
- 🎯 Ideal for desktop Linux users and sysadmins alike



---

## 📚 More Documentation

- [Script Registration Tool (`register-bash`)](./Resister-bash.md)  
  *Register your scripts as system-wide commands and manage aliases interactively.*

- [Tarball Application Installer (`install-tarapp.sh`)](./Install-TarApp/install-tarapp.md)  
  *Install `.tar.gz` GUI applications to `/opt` and create desktop launchers easily.*

---

## 🛡️ License

MIT License

Copyright (c) 2025 [Samyak Shrestha](https://github.com/samyak-shrestha)
