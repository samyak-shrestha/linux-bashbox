# Script Registration Tool

A Bash utility to register your scripts as system-wide commands and manage command aliases easily.

---

## Features

- **Recursively search** for scripts in the current directory and subdirectories.
- **Copy scripts** to `/usr/local/bin` (removes `.sh` extension for command-like behavior).
- **Make scripts executable** automatically.
- **Prompt for alias creation** (custom or default, or skip).
- **Manage aliases**: list, create/update, or remove aliases via an interactive menu.
- **Ensures aliases are sourced** in your `.bashrc` for persistence.

---

## Usage

### 1. Run the Tool

```bash
./register-bash
```

### 2. Main Menu Options

- `1` - List all executable files and scripts (recursively)
- `2` - List only `.sh` files
- `3` - Search for files by name
- `4` - Manage command aliases
- `5` - Exit

### 3. Registering a Script

- Select a script from the list.
- The script will be copied to `/usr/local/bin` **without the `.sh` extension** and made executable.
- You will be prompted to set an alias:
  - Leave blank to use the default (the filename without `.sh`)
  - Type a custom alias name
  - Type `none` to skip alias creation

### 4. Alias Management

- List all current aliases
- Create or update an alias (shows existing aliases for reference)
- Remove an alias (shows existing aliases for reference)

### 5. Notes

- Aliases are stored in `~/.bash_aliases`
- The tool ensures `~/.bash_aliases` is sourced in your `~/.bashrc`
- After adding or changing aliases, **run**:
  ```bash
  source ~/.bashrc
  ```
  or restart your terminal to use new aliases.

---

## Example

Register a script and set an alias:

```bash
./register-bash
# Choose your script (e.g., install-tarapp.sh)
# When prompted for alias, enter: appify
```

Now you can run your script as:

```bash
appify
```

---

## Requirements

- Bash
- `sudo` privileges (for copying to `/usr/local/bin`)

---

## License

MIT License — You can use, copy, modify, and distribute freely.
Author: [Samyak Shrestha](https://github.com/samyak-shrestha)


---