# Nilom WHMCS Client & Orderform Theme
<p align="center">
  <img src="templates/nilom/assets/img/logo/logo-inverse.svg" alt="Nilom Theme Logo" width="180">
  <br>
  <strong>A modern, high-performance, responsive WHMCS theme & order form engine.</strong>
  <br>
  <em>Crafted with care by <a href="https://nrwone.in">NRWThemes</a></em>
</p>
<p align="center">
  <a href="https://php.net"><img src="https://img.shields.io/badge/PHP-8.1%20|%208.2%20|%208.3%20|%208.4+-777bb4.svg?style=flat-square&logo=php" alt="PHP Version"></a>
  <a href="https://whmcs.com"><img src="https://img.shields.io/badge/WHMCS-9.0.6%20|%209.0.9%20|%209.x-29b6f6.svg?style=flat-square" alt="WHMCS Version"></a>
  <img src="https://img.shields.io/badge/ionCube-Not%20Required-success.svg?style=flat-square" alt="No ionCube">
  <img src="https://img.shields.io/badge/License-Zero%20License%20Lock-brightgreen.svg?style=flat-square" alt="License Free">
  <img src="https://img.shields.io/badge/Responsive-Mobile%20First-orange.svg?style=flat-square" alt="Mobile Ready">
</p>
---
## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Directory Structure](#-directory-structure)
- [Step-by-Step Installation Guide](#-step-by-step-installation-guide)
  - [Method 1: Installation via cPanel](#method-1-installation-via-cpanel)
  - [Method 2: Installation via SSH / Terminal](#method-2-installation-via-ssh--terminal)
- [Activating the Theme in WHMCS](#-activating-the-theme-in-whmcs)
- [Managing Theme Colors & Layouts](#-managing-theme-colors--layouts)
  - [Option A: Via WHMCS Admin Addon (Visual Picker)](#option-a-via-whmcs-admin-addon-visual-picker)
  - [Option B: Via theme-config.php](#option-b-via-theme-configphp)
  - [Option C: Live Browser Preview via URL](#option-c-live-browser-preview-via-url)
- [Troubleshooting & Common Issues](#-troubleshooting--common-issues)
- [Custom CSS Guide](#-custom-css-guide)
- [Author & Credits](#-author--credits)
---
## 🌟 Overview
**Nilom** is a modern WHMCS theme designed for web hosting providers, cloud operators, and domain registrars. Based on the Lagom 2 design framework, Nilom has been freed from ionCube encoding, proprietary licensing servers, and vendor lock-in.
- **100% Unencoded Pure PHP**: Runs natively on **PHP 8.1, PHP 8.2, PHP 8.3, and PHP 8.4+**.
- **No ionCube Loader Required**: Eliminate loader version mismatches when upgrading PHP.
- **Zero Licensing System**: No license keys, no phone-home callbacks, no expiration checks.
- **WHMCS 9.x Ready**: Fully compatible with **WHMCS 9.0.6, 9.0.6-release.1, 9.0.9**, and upcoming 9.x releases.
- **Dual Management Options**: Control colors and layouts via a dedicated WHMCS Admin Addon or a central PHP configuration file.
---
## 🚀 Key Features
* **🎨 5 Pre-Built Color Schemes**: Classic Blue, Emerald Green, Vibrant Orange, Royal Purple, Crimson Red, or choose any **Custom Hex Brand Color**.
* **📐 4 Modern Layouts**:
  * `default`: Clean top horizontal navigation bar.
  * `condensed`: Single-row compact navigation with inline search.
  * `left-nav`: Modern vertical sidebar layout.
  * `left-nav-wide`: Expanded vertical sidebar with text descriptions.
* **✨ 4 Design Styles**: `default`, `modern`, `depth`, and `futuristic`.
* **🌓 Dark Mode Engine**: Built-in dark/light mode toggle with cookie persistence and optional auto-detection of client OS preferences.
* **🛒 Matching Order Form**: Full shopping cart suite (product configurations, domain search, TLD renewal switcher, fraud check, checkout).
* **⚡ Blazing Fast**: Zero database lookups on menu loops and zero external licensing delays.
---
## 📁 Directory Structure
```text
nilom-theme/
├── README.md                                  <-- Documentation
├── includes/
│   └── hooks/
│       └── nilom_theme.php                    <-- Standalone Pure-PHP Hook Engine
├── modules/
│   └── addons/
│       └── nilom_theme/
│           └── nilom_theme.php                <-- Nilom Theme Manager Admin Addon
└── templates/
    ├── nilom/                                 <-- Client Area Theme
    │   ├── theme.yaml                         <-- WHMCS 9.x Theme Identity File
    │   ├── theme-config.php                   <-- Standalone Configuration File
    │   ├── assets/                            <-- Pre-compiled CSS, JS, fonts, SVGs
    │   ├── core/
    │   │   ├── config/                        <-- Page layouts & classes rules
    │   │   ├── lang/                          <-- 25+ language translation files
    │   │   ├── layouts/                       <-- Layout templates (main-menu, footer)
    │   │   ├── styles/                        <-- Style definitions & minified.css
    │   │   └── rstheme.php                    <-- Clean PHP stub (unencoded)
    │   └── ... (Smarty .tpl files)
    └── orderforms/
        └── nilom/                             <-- Order Form / Shopping Cart Theme
            ├── theme.yaml                     <-- Order Form Identity File
            └── ... (Cart .tpl files)
🛠️ Step-by-Step Installation Guide
Method 1: Installation via cPanel
Download the Theme: Download nilom-whmcs-theme-v9.zip from your release assets.

Open cPanel File Manager: Log in to cPanel and open File Manager. Navigate to your WHMCS root directory (e.g., /public_html or /public_html/clients).

Upload the Zip: Click Upload in the top toolbar and upload nilom-whmcs-theme-v9.zip.

Extract the Files: Right-click nilom-whmcs-theme-v9.zip, select Extract, verify the target path is your WHMCS root, and click Extract File(s).

Verify File Placement: Confirm that the files are placed as follows:

includes/hooks/nilom_theme.php
modules/addons/nilom_theme/nilom_theme.php
templates/nilom/
templates/orderforms/nilom/
Clear Template Cache: In cPanel File Manager, navigate to templates_c/ (or /home/username/whmcsdata/templates_c/), select all compiled files, and delete them.

Method 2: Installation via SSH / Terminal
Clone or Copy Files:

bash


cd /path/to/whmcs
# Unzip release package directly into WHMCS root
unzip nilom-whmcs-theme-v9.zip
Set Correct File Permissions:

bash


chmod -R 755 templates/nilom templates/orderforms/nilom modules/addons/nilom_theme
chmod 644 includes/hooks/nilom_theme.php
Purge Compiled Template Cache:

bash


rm -rf templates_c/*.php
# If templates_c is stored in whmcsdata:
rm -rf /path/to/whmcsdata/templates_c/*.php
⚙️ Activating the Theme in WHMCS
Log in to your WHMCS Admin Area.
Go to Configuration (wrench icon) > System Settings > General Settings.
Select Client Theme:
In the General tab, set Template to Nilom.
Select Cart Theme:
In the Ordering tab, set Default Order Form Template to Nilom.
Click Save Changes at the bottom of the page.
🎨 Managing Theme Colors & Layouts
Option A: Via WHMCS Admin Addon (Visual Picker)
In WHMCS Admin, go to System Settings > Addon Modules.
Locate Nilom Theme Manager and click Activate.
Click Configure, grant access to Full Administrator, and click Save Changes.
In your top menu, navigate to Addons > Nilom Theme Manager:
Choose any pre-built color palette (Blue, Green, Orange, Purple, Red).
Or choose Custom Hex and pick any brand color with the live color picker.
Switch navigation layout (Top Bar, Condensed, Left Vertical Sidebar).
Change dark mode behavior.
Click Save Settings to apply changes instantly.
Option B: Via theme-config.php
If you prefer configuring via code without using the addon module, open templates/nilom/theme-config.php:

php


return [
    // Theme Style: 'default', 'modern', 'depth', 'futuristic'
    'style'        => 'default',
    // Color Palette: 'default', 'green', 'orange', 'purple', 'red'
    'color'        => 'green',
    // Navigation Layout: 'default', 'condensed', 'left-nav', 'left-nav-wide'
    'layout'       => 'left-nav',
    // Footer Layout: 'default', 'extended'
    'footer_layout'=> 'default',
    // Dark Mode: 'switcher', 'force_dark', 'force_light', 'auto'
    'display_mode' => 'switcher',
    // Sticky / Affixed Navigation bar
    'sticky_nav'   => true,
    // Mobile Menu: 'dropdown' or 'slide'
    'mobile_menu'  => 'dropdown',
];
Option C: Live Browser Preview via URL
Test colors and styles on the fly without making permanent changes:

text


# Test Colors
https://yourdomain.com/index.php?rscolor=green
https://yourdomain.com/index.php?rscolor=orange
https://yourdomain.com/index.php?rscolor=purple
https://yourdomain.com/index.php?rscolor=red
# Test Layouts & Styles
https://yourdomain.com/index.php?rslayout=left-nav
https://yourdomain.com/index.php?rsstyle=modern&rscolor=green
🔧 Troubleshooting & Common Issues
1. Call to undefined method RSThemes\Helpers\AddonHelper::getNotActiveTemplates()
Cause: An old, encoded modules/addons/RSThemes folder from a previous Lagom install is still present and executing hooks.
Fix: In cPanel File Manager, go to modules/addons/ and rename RSThemes to RSThemes_disabled (or rename modules/addons/RSThemes/hooks.php to hooks.php.bak).
2. Call to a member function license() on string
Cause: Legacy RSThemes addon is trying to phone home to RS Studio licensing servers.
Fix: Disable or rename modules/addons/RSThemes as described above. Nilom does not require RSThemes.
3. Changes Not Reflecting in Browser
Fix: Empty your WHMCS template cache:
In WHMCS Admin, go to Utilities > System > System Cleanup.
Click Empty Template Cache.
Perform a hard refresh in your browser (Ctrl + F5 or Cmd + Shift + R).
🎨 Custom CSS Guide
To add custom CSS without modifying core template files:

Method 1: Via Nilom Theme Manager Addon
Navigate to Addons > Nilom Theme Manager, scroll to the Custom CSS field, enter your rules, and click Save Settings.

Method 2: Via theme-custom.css
Create templates/nilom/core/styles/default/assets/css/theme-custom.css:

css


/* Example: Custom Accent & Button Styles */
:root {
    --brand-primary: #2563eb;
    --brand-primary-faded: rgba(37, 99, 235, 0.12);
}
.btn-primary {
    border-radius: 8px;
    font-weight: 600;
}
👤 Author & Credits
Theme: Nilom WHMCS Theme
Author: NRWThemes
Website: nrwone.in
Base Design Reference: Lagom 2 Framework
License: Open Source / Standalone (Zero Licensing Barrier)
