# Windows Folder Protection Scripts

Two powerful Windows batch scripts for protecting your sensitive folders - choose the right level of security for your needs.

## 🔒 Available Protection Methods

| Feature | **Simple Protection** | **Secure Encryption** |
|---------|----------------------|----------------------|
| **Security Level** | 🟡 Privacy Screen | 🔴 Military Grade |
| **Method** | Folder Hiding + Password Hash | AES-256 Encryption |
| **Password Storage** | Salted SHA-256 Hash | PBKDF2 Key Derivation |
| **Data Recovery** | ✅ Always Possible | ❌ Lost Password = Lost Data |
| **File Access** | Hidden but Readable | Completely Encrypted |
| **Performance** | ⚡ Instant | 🐌 Processing Time Required |
| **Use Case** | Personal Privacy | Critical Security |

---

## 🟡 Simple Protection - Privacy Screen

**Perfect for:** Personal computers, casual privacy, shared family devices

### 📋 [Code_Simple.txt](Code_Simple.txt) | 📖 [README_Simple.md](README_Simple.md)

### What It Does:
- **Hides folders** using Windows system attributes and Control Panel CLSID
- **Password protection** with salted SHA-256 hashing
- **Instant operation** - no waiting time
- **Reversible process** - can always recover your files

### Security Features:
```
✅ Salted SHA-256 password hashing (not plain text)
✅ Windows system-level folder hiding
✅ Secure password input (hidden from display)
✅ Metadata protection (hidden system files)
✅ Random UUID salt generation
```

### Ideal For:
- 👨‍👩‍👧‍👦 **Family computers** - keeping personal files private
- 🏢 **Office environments** - hiding sensitive documents from casual browsing
- 🎒 **Portable drives** - privacy protection for USB sticks
- 📱 **Quick privacy** - when you need instant folder hiding
- 🔍 **Preventing accidental access** - stops casual snooping

### ⚠️ Limitations:
```
❌ Advanced users can find hidden folders
❌ Not protection against determined attackers
❌ Files remain readable if discovered
❌ System administrators can bypass hiding
```

---

## 🔴 Secure Encryption - Military Grade Protection

**Perfect for:** Confidential business data, financial records, legal documents

### 📋 [Code_SecureEncrypt.txt](Code_SecureEncrypt.txt) | 📖 [README_SecureEncrypt.md](README_SecureEncrypt.md)

### What It Does:
- **True AES-256 encryption** - files are genuinely unreadable
- **PBKDF2 key derivation** with 10,000 iterations
- **Complete data destruction** - original files permanently deleted
- **Military-grade security** - meets government encryption standards

### Security Features:
```
✅ AES-256-CBC encryption (NSA approved)
✅ PBKDF2 key stretching (10,000 iterations)
✅ Automatic compression before encryption
✅ Secure password input with memory protection
✅ Complete original data destruction
✅ Cryptographic integrity protection
```

### Ideal For:
- 💼 **Business confidential data** requiring compliance
- 🏥 **Medical records** (HIPAA compliance)
- 💰 **Financial documents** (PCI DSS requirements)
- ⚖️ **Legal files** requiring attorney-client privilege
- 🔬 **Research data** with proprietary information
- 🛡️ **Government contractors** needing security clearance

### ⚠️ Critical Warnings:
```
❌ FORGOTTEN PASSWORD = PERMANENT DATA LOSS
❌ NO RECOVERY METHODS EXIST
❌ MUST MAINTAIN BACKUPS ELSEWHERE
❌ PROCESSING TIME REQUIRED FOR LARGE FILES
```

---

## 🤔 Which One Should You Choose?

### Choose **Simple Protection** if:
- ✅ You need **privacy** rather than security
- ✅ Files are on a **personal/trusted computer**
- ✅ You want **instant** folder hiding/showing
- ✅ You need to **quickly access** files frequently
- ✅ You're okay with **determined users** potentially finding files
- ✅ Data loss would be **inconvenient** but not catastrophic

### Choose **Secure Encryption** if:
- ✅ You need **genuine security** against all threats
- ✅ Files contain **confidential/regulated** information
- ✅ You can **accept processing delays** for large files
- ✅ You have **reliable backup systems** in place
- ✅ Data loss would be **catastrophic** for business/legal reasons
- ✅ You need **compliance** with security regulations

---

## 🚀 Quick Start Guide

### For Simple Protection:
```bash
1. Download Code_Simple.txt → Save as "SecureFolder.bat"
2. Double-click to run → Creates "Private" folder
3. Add files to Private folder
4. Run script → Choose "Lock" → Enter password
5. Folder disappears (hidden)
6. Run script → Choose "Unlock" → Enter password → Folder reappears
```

### For Secure Encryption:
```bash
1. Download Code_SecureEncrypt.txt → Save as "AESSecureFolder.bat"  
2. Create "Private" folder → Add your files
3. Run script → Choose "Encrypt" → Confirm → Enter password
4. Private folder DELETED → Private.locked created (encrypted)
5. Run script → Choose "Decrypt" → Enter password → Folder restored
```

---

## 📊 Detailed Comparison

| Aspect | Simple Protection | Secure Encryption |
|--------|------------------|-------------------|
| **Setup Complexity** | 🟢 Very Easy | 🟡 Easy |
| **Daily Use** | 🟢 Instant | 🟡 Processing Time |
| **Security Against Casual Users** | 🟢 Excellent | 🟢 Excellent |
| **Security Against IT Professionals** | 🔴 Poor | 🟢 Excellent |
| **Security Against Forensics** | 🔴 None | 🟢 Excellent |
| **Data Recovery if Password Lost** | 🟢 Possible | 🔴 Impossible |
| **File Access Speed** | 🟢 Instant | 🟡 Must Decrypt First |
| **Storage Overhead** | 🟢 None | 🟡 Temporary 2x Space |
| **Regulatory Compliance** | 🔴 Not Suitable | 🟢 Meets Standards |

---

## 🔧 System Requirements

### Both Scripts Require:
- **OS**: Windows 7/8/8.1/10/11
- **PowerShell**: 3.0+ (included with modern Windows)
- **Permissions**: Standard user (Admin for some troubleshooting)
- **Dependencies**: None (uses built-in Windows components)

### Additional for Secure Encryption:
- **Disk Space**: 2x folder size during encryption/decryption
- **.NET Framework**: 4.0+ (for cryptography classes)
- **Processing Time**: Allow extra time for large files

---

## 🛡️ Security Best Practices

### For Both Methods:
```
✅ Use strong, unique passwords (12+ characters)
✅ Store passwords in reputable password manager
✅ Test with sample files before real use
✅ Keep scripts updated and backed up
✅ Don't use on shared/public computers
```

### Additional for Secure Encryption:
```
✅ ALWAYS maintain external backups
✅ Document passwords in multiple secure locations
✅ Test decryption process regularly
✅ Understand that password loss = data loss
✅ Consider compliance requirements for your data
```

---

## 📚 Documentation & Support

### Complete Documentation:
- **Simple Protection**: [README_Simple.md](README_Simple.md) - Complete usage guide
- **Secure Encryption**: [README_SecureEncrypt.md](README_SecureEncrypt.md) - Comprehensive security guide

### What Each README Contains:
- 📖 **Detailed installation** and setup instructions
- 🔧 **Step-by-step usage** with examples and screenshots
- 🐛 **Troubleshooting guide** for common issues
- ⚙️ **Configuration options** and customization
- 🛡️ **Security analysis** and best practices
- ⚠️ **Important limitations** and warnings

---

## 🤝 Contributing & Support

### Found a Bug or Have Suggestions?
- 🐛 **Report issues** with detailed error messages
- 💡 **Suggest improvements** for better security or usability
- 🔧 **Submit fixes** following existing code style
- 📖 **Improve documentation** with clearer explanations

### Security Considerations:
- 🔍 **Security vulnerabilities** should be reported responsibly
- 🧪 **Test thoroughly** before suggesting changes to encryption code
- 📋 **Document security implications** of any modifications

---

## ⚖️ Legal & Disclaimer

### Important Disclaimers:
```
⚠️ These tools are provided "as-is" for educational and legitimate use
⚠️ Users are responsible for compliance with local laws and regulations
⚠️ Always maintain backups - authors not responsible for data loss
⚠️ Export/usage restrictions may apply in some countries
⚠️ Test thoroughly before using with critical data
```

### Compliance Notes:
- **Simple Protection**: Suitable for privacy, not regulated data
- **Secure Encryption**: Meets most regulatory requirements (GDPR, HIPAA, PCI DSS)
- **Export Controls**: AES-256 encryption may be restricted in some jurisdictions

---

## 🎯 Summary: Choose Your Protection Level

### 🟡 **Simple Protection** = Privacy Screen
*"I want to keep my personal files private on my home computer"*

### 🔴 **Secure Encryption** = Vault-Level Security  
*"I need to protect confidential business data with military-grade encryption"*

### 🤝 **Both Available** = Complete Flexibility
*"Different files need different levels of protection"*

---

## Alternative - Reliably across any systems: **`VeraCrypt`** Encrypted Container

- Works on: Windows, macOS, Linux.
- Advantages:
  - Real encryption (AES, Twofish, etc.).
  - One file acts as a “secure vault” — you mount it to see its contents.
  - Password protected — can’t be opened without correct credentials.
  - No plain text anywhere.
- Setup Steps:
    1. Install VeraCrypt on both Mac, Windows & Linux.
    2. Create an encrypted container file (e.g., SecureVault.hc) on your pen drive.
    3. Mount it in VeraCrypt → enter password → acts like a normal drive.
    4. Dismount to lock.

Why it’s good: You can move that Portable drive between your Mac and any Windows PC or Linux with VeraCrypt installed, and the vault remains secure.

---

**📁 Ready to protect your files? Download the appropriate script and follow the detailed README for your chosen security level!**
