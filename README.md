# PHP Switcher for XAMPP

A fast, modern Windows desktop application for managing and switching between multiple PHP versions in XAMPP with automatic Apache configuration, backups, and phpMyAdmin theming.

---

## 🚀 Download

Download the latest release executable:
* **Latest Release (v1.1)**: [PHP-Switcher-v1.1-win-x64.exe](https://github.com/mtm-zakir/PHP-Switcher-Releases/releases/tag/v1.1)
* **All Releases**: [GitHub Releases Page](https://github.com/mtm-zakir/PHP-Switcher-Releases/releases)

---

## ✨ Key Features

- **One-Click PHP Switching**: Seamlessly switch between bundled and custom PHP 8.x versions (PHP 8.3, 8.4, 8.5).
- **🎨 Modern Theme for phpMyAdmin**: Apply the custom **"Modern by Zakir"** theme for phpMyAdmin with a single click right from the footer.
- **Zero-Footprint Execution**: Runtime packages extract directly into `%APPDATA%\php-switcher-files` and are **permanently deleted** when the application closes.
- **Automatic Apache Configuration**: Automatically updates `httpd-xampp.conf` to match the selected PHP version runtime module and directory.
- **Safe Automatic Backups & Rollback**: Backs up existing PHP installations before switching so you can rollback anytime with one click.
- **Configuration Preservation**: Custom settings in `php.ini` are maintained and applied automatically.
- **Smart Detection**: Automatically detects XAMPP installations across drives (`C:\xampp`, `D:\xampp`, etc.).
- **Silent Background Updates**: Checks for GitHub releases in the background and notifies you when an update is available.

---

## 📝 Changelog

### v1.1
- **Added**: **Modern Theme for phpMyAdmin** (`Modern by Zakir`) one-click installer in the footer. Extracts the theme into `C:\xampp\phpMyAdmin\themes`, sets `$cfg['ThemeDefault'] = 'Modern';` in `config.inc.php`, and opens phpMyAdmin in your default browser automatically.
- **Changed**: Runtime files and bundled versions now extract to the user's AppData directory (`%APPDATA%\php-switcher-files`) instead of creating a `versions` folder next to the executable.
- **Added**: Automatic permanent cleanup of `%APPDATA%\php-switcher-files` whenever the application closes.
- **Added**: Windows Defender SmartScreen mitigation — added assembly publisher metadata (`MTM Zakir`), Authenticode code-signing utility, and automated `Unblock-File` post-build target to clear Mark of the Web (`Zone.Identifier`).
- **Improved**: Filtered package scanner to only detect PHP runtime archives (`php*.zip`), ignoring non-PHP archives.
- **Fixed**: Removed hardcoded development workspace paths.

### v1.0
- Initial public release of PHP Switcher for XAMPP.
- One-click PHP version switching between PHP 8.3, 8.4, and 8.5.
- Automatic XAMPP root and Apache detection.
- Automatic PHP folder backup and rollback manager.
- Fluent dark-mode UI with real-time log viewer.

---

## 🛡️ Windows Defender SmartScreen Note

If Windows displays the blue **"Windows protected your PC"** popup when launching the executable:

### Option 1: Right-Click Properties (Easiest)
1. Right-click `PHP-Switcher-v1.1-win-x64.exe` and select **Properties**.
2. At the bottom of the **General** tab, check the **Unblock** box.
3. Click **Apply** & **OK**, then run the application.

### Option 2: PowerShell Unblock
Open PowerShell in the folder where the `.exe` is located and run:
```powershell
Unblock-File .\PHP-Switcher-v1.1-win-x64.exe
```

### Option 3: Run Anyway
Click **More info** on the SmartScreen dialog, then click **Run anyway**.

---

## 🖥️ System Requirements

- **Operating System**: Windows 10 / Windows 11 (64-bit)
- **Web Stack**: XAMPP for Windows
- **Architecture**: x64

---

## 👤 Developer

Developed with ❤️ by **MTM Zakir**  
LinkedIn: [mtm-zakir](https://www.linkedin.com/in/mtm-zakir)
