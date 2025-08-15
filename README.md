# SecureFolder - Windows Batch File Folder Protection Utility

A lightweight Windows batch script that provides password-protected folder hiding using advanced security features including salted SHA-256 password hashing and Windows system-level obfuscation.

## 🔒 Features

- **Salted SHA-256 Password Hashing** - Passwords are never stored in plain text
- **System-Level Folder Hiding** - Uses Windows Control Panel CLSID for deep hiding
- **Secure Password Input** - Password entry is hidden from display and console history
- **First-Time Setup Wizard** - Automatic folder creation and password configuration
- **Menu-Driven Interface** - Simple, user-friendly operation
- **Portable** - Single `.bat` file that runs on any Windows system
- **No Dependencies** - Uses only built-in Windows commands and PowerShell

## 🚀 Quick Start

### Installation

1. **Download the Script**
   - Copy the script code into a text editor (Notepad, VS Code, etc.)
   - Save as `SecureFolder.bat`
   - **Important**: Set "Save as type" to "All Files" and encoding to "ANSI" or "UTF-8"

2. **Place the Script**
   - Put `SecureFolder.bat` in any folder where you want your secure folder
   - Works on local drives, USB drives, network locations, etc.

3. **First Run**
   - Double-click `SecureFolder.bat`
   - The script will create a folder called `Private` and prompt you to set a password
   - Your password will be securely hashed and stored

### Basic Usage

1. **Adding Files**: Place your sensitive files in the `Private` folder
2. **Locking**: Run the script and choose option `1` - folder becomes hidden
3. **Unlocking**: Run the script, choose option `1`, enter your password - folder becomes visible again

## 📋 How It Works

### Security Mechanism

```
Password Input → Salt Generation → SHA-256 Hashing → Encrypted Storage
     ↓
File Storage: .lock.meta contains SALT:HASH (hidden system file)
     ↓
Folder Hiding: Renamed to "Control Panel.{CLSID}" + Hidden/System attributes
```

### Technical Details

- **Password Hashing**: Uses SHA-256 with random UUID salt
- **Folder Obfuscation**: Renames folder to Windows Control Panel CLSID `{21EC2020-3AEA-1069-A2DD-08002B30309D}`
- **File Attributes**: Sets hidden (`+h`) and system (`+s`) attributes
- **Metadata Storage**: Stores salt and hash in `.lock.meta` (also hidden/system file)

## 🛡️ Security Features

### ✅ What This Script Protects Against
- Casual browsing and accidental discovery
- Basic file searches in Windows Explorer
- Users who don't know about hidden/system files
- Simple password guessing (thanks to salted hashing)

### ⚠️ Security Limitations
- **Not true encryption** - Files are hidden, not encrypted
- **Advanced users** can still find files by:
  - Showing hidden/system files
  - Using command line tools
  - Searching for the Control Panel CLSID
- **Password hash** could be extracted and attacked offline
- **Physical access** to the computer can bypass protection

### 🎯 Recommended Use Cases
- **Personal privacy** on shared computers
- **Organizing sensitive documents** on personal devices
- **Temporary protection** during file transfers
- **Privacy screen** for personal files

### ❌ NOT Recommended For
- Highly confidential business data
- Financial or legal documents
- Protection against determined attackers
- Compliance with data protection regulations

## 📖 Detailed Usage Guide

### Menu Options

```
============================
   Secure Folder Utility
============================
1. Lock folder    (when folder is visible)
1. Unlock folder  (when folder is hidden)
2. Exit
```

### First-Time Setup
```bash
# When you first run the script:
First-time setup: Creating secure folder and setting password...
Enter new password: [password hidden]
Password set successfully.
```

### Locking Process
```bash
# Files you want to hide → Put in 'Private' folder → Run script → Choose 1
Folder locked.
# 'Private' folder disappears from view
```

### Unlocking Process
```bash
# Run script → Choose 1 → Enter password
Enter password: [password hidden]
Folder unlocked.
# 'Private' folder becomes visible again
```

## 🔧 Configuration

### Customizable Settings (Edit script header)
```batch
set "LOCKFOLDER=Private"                              # Name of your secure folder
set "METAFILE=.lock.meta"                           # Password storage file
set "CLSID={21EC2020-3AEA-1069-A2DD-08002B30309D}" # Control Panel CLSID
```

### Advanced Customization
- Change `LOCKFOLDER` to use a different folder name
- Modify `CLSID` to use a different Windows system object
- Update `METAFILE` to change password storage location

## 🐛 Troubleshooting

### Common Issues

**"The system cannot find the file specified"**
- Ensure script is saved with `.bat` extension
- Check that you're running from the correct directory

**"Access is denied" when locking/unlocking**
- Run Command Prompt as Administrator
- Check if files in the folder are currently open

**Password not working**
- Passwords are case-sensitive
- Ensure no extra spaces when entering password
- Try recreating the password (delete `.lock.meta` file)

**Folder still visible after locking**
- Refresh Windows Explorer (F5)
- Check Windows Explorer settings for showing hidden files

### Recovery Options

**Lost Password**
- Delete the `.lock.meta` file (you may need to show hidden files first)
- Run the script again - it will treat it as first-time setup
- **Note**: You'll lose access to the currently locked folder

**Corrupted Metadata**
- Manually unhide the folder: `attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"`
- Rename it back: `ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" "Private"`

## 📊 File Structure

```
Your Directory/
├── SecureFolder.bat          # Main script
├── Private/                  # Your secure folder (visible when unlocked)
│   ├── your-file-1.txt      # Your protected files
│   ├── your-file-2.jpg      # Your protected files
│   └── ...
├── .lock.meta               # Password hash storage (hidden)
└── Control Panel.{CLSID}/   # Hidden folder (when locked)
```

## ⚖️ License & Disclaimer

This script is provided "as-is" for educational and personal use. 

**IMPORTANT DISCLAIMERS:**
- This tool provides **obfuscation**, not military-grade encryption
- Always keep backups of important files
- Test thoroughly before using with critical data
- Use at your own risk - author not responsible for data loss
- Not suitable for protecting against determined attackers

## 🤝 Contributing

This is a community script! Feel free to:
- Report bugs or issues
- Suggest improvements
- Share enhanced versions
- Contribute to documentation

## 📚 Technical Requirements

- **OS**: Windows 7/8/8.1/10/11
- **Dependencies**: PowerShell (included with Windows)
- **Permissions**: Standard user (Administrator for some troubleshooting)
- **Storage**: Minimal (script is <5KB)

---

**Remember**: This tool is designed for privacy, not security. For sensitive data requiring true protection, consider professional encryption tools like BitLocker, VeraCrypt, or 7-Zip with AES encryption.
