# 🔧 Tarball Application Installer Script

A reusable and interactive Bash script to install `.tar.gz` GUI applications like **Android Studio**, **PyCharm**, etc., by:

- 📦 Extracting the archive
- 🚚 Moving to `/opt/app-name`
- ⚙️ Choosing the correct launcher `.sh` file
- 🖼️ Selecting a `.png` icon
- 🧷 Creating a `.desktop` shortcut in `/usr/share/applications`
- 📈 Showing progress (via `pv` or fallback spinner)

---

## 🚀 Features

✅ Lists all `.tar.gz` files in current directory  
✅ Lets you select the file to install  
✅ Prompts for app name and normalizes:
- Folder: `lower-case-hyphen-name` → `/opt/app-name`
- Menu: `Title Case Display Name` → for GUI apps

✅ Lists all `.sh` executables from `/bin`  
✅ Auto-suggests `.sh` file that matches app name  
✅ Lists all `.png` icons and allows custom selection  
✅ Creates `.desktop` entry (visible in launcher/menu)  
✅ Uses `pv` for extraction progress (optional)  
✅ Fallback spinner if `pv` is not installed  

---

## 📋 Example

```bash
$ ./install_tar_app.sh
📦 Available .tar.gz files:
1. pycharm-2025.1.2.tar.gz
2. android-studio-2025.1.1.13-linux.tar.gz

👉 Enter the number to install: 2
📛 Enter Application Name: android-studio
📈 Using pv for progress...
🕐 Extracting...
...
✅ Installed: Android Studio
```


## 🛠 Requirements

- `bash` (Linux shell)
- `tar`
- `sudo`
- Optional: `pv` — Pipe Viewer for progress bar

📦 Install `pv` (Optional)

If you want visual extraction progress:
```bash
sudo apt install pv
```

## 📁 Output Structure

Given `App Name: android-studio`, it will:

|Item |	Location |
|---|----|
| Installed Folder	| `/opt/android-studio/` |
| Executable	| `/opt/android-studio/bin/android-studio.sh` |
| Icon (if chosen)	| `/opt/android-studio/bin/android-studio.png` |
| Menu Entry (.desktop)	| `/usr/share/applications/android-studio.desktop` |


## 🧠 Why This Script Exists

Manually installing `.tar.gz` apps like JetBrains IDEs often involves repetitive steps:
- Extract
- Move to `/opt`
- Hunt down the right `.sh` file
- Find an icon
- Write your own `.desktop` launcher

This script automates that and makes it easy, fast, and foolproof for beginners.

## 💡 How It Works (Under the Hood)

1. Finds all `.tar.gz` files
2. Extracts selected one into temp folder
3. Moves extracted folder to `/opt/app-folder`
4. Lists `.sh` files → prompts user to choose launcher
5. Lists `.png` files → prompts for icon (optional)
6. Builds `.desktop` file for system launcher
7. Makes `.desktop` executable

## 📌 Limitations & Notes
- The .desktop shortcut is created system-wide (`/usr/share/applications`). You need sudo.
- The script only works with `.tar.gz` files that contain a single root folder with `/bin/*.sh` launcher inside.
- Some apps may not use `.sh` launchers or have icons — the script allows skipping those.

## 🧪 To Do / Ideas

- Add support for `.AppImage`, `.zip`, or `.tar.xz`
- Offer install to `~/.local/share/applications` for user-only setup
- Automatically symlink binary to `/usr/local/bin/app`

## 🛡️ License

MIT — You can use, copy, modify, and distribute freely.
Author: [Samyak Shrestha](https://github.com/samyak-shrestha)

🙏 Credits

Thanks to:
- JetBrains for consistent archive structure
- `pv` for terminal progress

