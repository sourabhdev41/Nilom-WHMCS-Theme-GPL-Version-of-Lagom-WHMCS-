# Nilom WHMCS Client & Orderform Theme

<p align="center">
  <img src="templates/nilom/assets/img/logo/logo-inverse.svg" alt="Nilom Theme Logo" width="180">
  <br>
  <strong>A modern, high-performance, responsive WHMCS theme & order form engine.</strong>
  <br>
  <em>Crafted with care by <a href="https://nrwone.in">NRWThemes</a></em>
</p>

<p align="center">
  <a href="https://php.net">
    <img src="https://img.shields.io/badge/PHP-8.1%20%7C%208.2%20%7C%208.3%20%7C%208.4+-777bb4.svg?style=flat-square&logo=php" alt="PHP Version">
  </a>
  <a href="https://whmcs.com">
    <img src="https://img.shields.io/badge/WHMCS-9.0.6%20%7C%209.0.9%20%7C%209.x-29b6f6.svg?style=flat-square" alt="WHMCS Version">
  </a>
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
  - [Option A: Via WHMCS Admin Addon](#option-a-via-whmcs-admin-addon-visual-picker)
  - [Option B: Via theme-config.php](#option-b-via-theme-configphp)
  - [Option C: Live Browser Preview](#option-c-live-browser-preview-via-url)
- [Troubleshooting & Common Issues](#-troubleshooting--common-issues)
- [Custom CSS Guide](#-custom-css-guide)
- [Author & Credits](#-author--credits)

---

## 🌟 Overview

**Nilom** is a modern WHMCS theme designed for web hosting providers, cloud operators, and domain registrars.

Based on the Lagom 2 design framework, Nilom has been adapted into a standalone, unencoded theme with no ionCube requirement and no external licensing system.

### Highlights

- **100% Unencoded Pure PHP** — Runs natively on PHP 8.1, PHP 8.2, PHP 8.3 and PHP 8.4+.
- **No ionCube Loader Required** — No ionCube loader dependency.
- **Zero Licensing System** — No license keys, phone-home callbacks or expiration checks.
- **WHMCS 9.x Ready** — Designed for WHMCS 9.x environments.
- **Dual Management Options** — Configure the theme through the WHMCS Admin Addon or `theme-config.php`.
- **Responsive Design** — Mobile-first interface for desktop, tablet and mobile devices.

---

## 🚀 Key Features

### 🎨 Color Schemes

Nilom includes multiple pre-built color schemes:

- Classic Blue
- Emerald Green
- Vibrant Orange
- Royal Purple
- Crimson Red
- Custom Hex Brand Color

### 📐 Modern Layouts

Nilom provides four navigation layouts:

| Layout | Description |
|---|---|
| `default` | Clean top horizontal navigation bar |
| `condensed` | Single-row compact navigation with inline search |
| `left-nav` | Modern vertical sidebar layout |
| `left-nav-wide` | Expanded vertical sidebar with text descriptions |

### ✨ Design Styles

Choose between four design styles:

```text
default
modern
depth
futuristic
````

### 🌓 Dark Mode Engine

Built-in dark/light mode support with:

* Dark mode switcher
* Force dark mode
* Force light mode
* Automatic OS preference detection
* Cookie-based preference persistence

### 🛒 Matching Order Form

Nilom includes a matching WHMCS order form and shopping cart interface supporting:

* Product configuration
* Domain search
* Domain registration
* Domain renewal
* TLD selection
* Fraud checking
* Shopping cart
* Checkout

### ⚡ Performance

Nilom is designed to minimize unnecessary overhead:

* Pure PHP implementation
* No external licensing callbacks
* No licensing delays
* Centralized configuration
* Optimized theme assets

---

## 📁 Directory Structure

```text
nilom-theme/
├── README.md
│
├── includes/
│   └── hooks/
│       └── nilom_theme.php
│
├── modules/
│   └── addons/
│       └── nilom_theme/
│           └── nilom_theme.php
│
└── templates/
    ├── nilom/
    │   ├── theme.yaml
    │   ├── theme-config.php
    │   ├── assets/
    │   ├── core/
    │   │   ├── config/
    │   │   ├── lang/
    │   │   ├── layouts/
    │   │   ├── styles/
    │   │   └── rstheme.php
    │   └── ... (Smarty .tpl files)
    │
    └── orderforms/
        └── nilom/
            ├── theme.yaml
            └── ... (Cart .tpl files)
```

---

# 🛠️ Step-by-Step Installation Guide

## Method 1: Installation via cPanel

### 1. Download the Theme

Download the latest Nilom release ZIP file from the repository's **Releases** section.

Example:

```text
nilom-whmcs-theme-v9.zip
```

### 2. Open cPanel File Manager

Log in to cPanel and open **File Manager**.

Navigate to your WHMCS installation directory.

Common locations include:

```text
/public_html
```

or:

```text
/public_html/clients
```

### 3. Upload the ZIP

Click **Upload** and upload:

```text
nilom-whmcs-theme-v9.zip
```

### 4. Extract the Files

Right-click the ZIP file and select:

**Extract**

Make sure the extraction destination is your WHMCS root directory.

### 5. Verify File Placement

After extraction, verify that the following files and directories exist:

```text
includes/hooks/nilom_theme.php
modules/addons/nilom_theme/nilom_theme.php
templates/nilom/
templates/orderforms/nilom/
```

### 6. Clear Template Cache

Navigate to:

```text
templates_c/
```

or, depending on your WHMCS configuration:

```text
/home/username/whmcsdata/templates_c/
```

Delete the compiled template files.

---

# Method 2: Installation via SSH / Terminal

Navigate to your WHMCS installation directory:

```bash
cd /path/to/whmcs
```

Extract the release package:

```bash
unzip nilom-whmcs-theme-v9.zip
```

### Set Correct File Permissions

```bash
chmod -R 755 templates/nilom templates/orderforms/nilom modules/addons/nilom_theme
```

Set the hook file permissions:

```bash
chmod 644 includes/hooks/nilom_theme.php
```

### Purge Compiled Template Cache

```bash
rm -rf templates_c/*.php
```

If your `templates_c` directory is stored inside `whmcsdata`:

```bash
rm -rf /path/to/whmcsdata/templates_c/*.php
```

---

# ⚙️ Activating the Theme in WHMCS

After installation:

1. Log in to your **WHMCS Admin Area**.

2. Go to:

   **Configuration → System Settings → General Settings**

3. Open the **General** tab.

4. Set **Template** to:

```text
Nilom
```

5. Open the **Ordering** tab.
6. Set **Default Order Form Template** to:

```text
Nilom
```

7. Click **Save Changes**.

---

# 🎨 Managing Theme Colors & Layouts

Nilom provides multiple ways to manage its appearance.

## Option A: Via WHMCS Admin Addon (Visual Picker)

1. Log in to WHMCS Admin.

2. Go to:

   **System Settings → Addon Modules**

3. Locate:

```text
Nilom Theme Manager
```

4. Click **Activate**.
5. Click **Configure**.
6. Grant access to the required administrator role.
7. Click **Save Changes**.
8. Navigate to:

   **Addons → Nilom Theme Manager**

From the Theme Manager you can configure:

* Pre-built color palettes
* Custom Hex brand color
* Navigation layout
* Design style
* Dark mode behavior
* Custom CSS

### Available Color Palettes

```text
Blue
Green
Orange
Purple
Red
Custom Hex
```

---

## Option B: Via `theme-config.php`

If you prefer configuring Nilom directly through PHP, open:

```text
templates/nilom/theme-config.php
```

Example:

```php
<?php

return [

    // Theme Style
    // default, modern, depth, futuristic
    'style' => 'default',

    // Color Palette
    // default, green, orange, purple, red
    'color' => 'green',

    // Navigation Layout
    // default, condensed, left-nav, left-nav-wide
    'layout' => 'left-nav',

    // Footer Layout
    // default, extended
    'footer_layout' => 'default',

    // Display Mode
    // switcher, force_dark, force_light, auto
    'display_mode' => 'switcher',

    // Sticky / Affixed Navigation
    'sticky_nav' => true,

    // Mobile Menu
    // dropdown, slide
    'mobile_menu' => 'dropdown',

];
```

### Display Modes

#### Theme Switcher

```php
'display_mode' => 'switcher',
```

#### Force Dark Mode

```php
'display_mode' => 'force_dark',
```

#### Force Light Mode

```php
'display_mode' => 'force_light',
```

#### Automatic OS Detection

```php
'display_mode' => 'auto',
```

---

# Option C: Live Browser Preview via URL

You can preview colors, layouts and styles directly through URL parameters without permanently changing your configuration.

### Test Colors

```text
https://yourdomain.com/index.php?rscolor=green
```

```text
https://yourdomain.com/index.php?rscolor=orange
```

```text
https://yourdomain.com/index.php?rscolor=purple
```

```text
https://yourdomain.com/index.php?rscolor=red
```

### Test Layouts

```text
https://yourdomain.com/index.php?rslayout=left-nav
```

### Test Styles and Colors

```text
https://yourdomain.com/index.php?rsstyle=modern&rscolor=green
```

---

# 🔧 Troubleshooting & Common Issues

## 1. `Call to undefined method RSThemes\Helpers\AddonHelper::getNotActiveTemplates()`

### Cause

An old or encoded `modules/addons/RSThemes` directory from a previous Lagom installation may still be present and executing hooks.

### Fix

Using cPanel File Manager, navigate to:

```text
modules/addons/
```

Rename:

```text
RSThemes
```

to:

```text
RSThemes_disabled
```

Alternatively, rename:

```text
modules/addons/RSThemes/hooks.php
```

to:

```text
hooks.php.bak
```

---

## 2. `Call to a member function license() on string`

### Cause

A legacy `RSThemes` addon may still be attempting to communicate with its licensing system.

### Fix

Disable or rename:

```text
modules/addons/RSThemes
```

Nilom does not require the `RSThemes` addon.

---

## 3. Changes Are Not Reflecting in the Browser

If changes are not visible after modifying the configuration, clear the WHMCS template cache.

Go to:

**Utilities → System → System Cleanup**

Then click:

**Empty Template Cache**

After clearing the cache, perform a hard browser refresh.

### Windows / Linux

```text
Ctrl + F5
```

### macOS

```text
Cmd + Shift + R
```

---

# 🎨 Custom CSS Guide

Nilom allows you to add custom CSS without modifying the core template files.

## Method 1: Via Nilom Theme Manager

Navigate to:

**Addons → Nilom Theme Manager**

Find the **Custom CSS** field.

Enter your CSS and click:

**Save Settings**

---

## Method 2: Via `theme-custom.css`

Create:

```text
templates/nilom/core/styles/default/assets/css/theme-custom.css
```

Example:

```css
/* Example: Custom Accent & Button Styles */

:root {
    --brand-primary: #2563eb;
    --brand-primary-faded: rgba(37, 99, 235, 0.12);
}

.btn-primary {
    border-radius: 8px;
    font-weight: 600;
}
```

This lets you customize the theme without directly modifying core template files.

---

# 👤 Author & Credits

* **Theme:** Nilom WHMCS Theme
* **Author:** **NRWThemes**
* **Website:** [https://nrwone.in/](https://nrwone.in/)
* **Design Reference:** Lagom 2 Framework
* **License:** Open Source / Standalone
* **ionCube:** Not Required

---

# ⭐ Support

If you find Nilom useful, consider giving the repository a ⭐ on GitHub.

For bugs, issues or feature requests, please use the repository's **Issues** section.

---

<p align="center">
  <strong>Nilom — Modern WHMCS without unnecessary licensing barriers.</strong>
  <br>
  Built by <a href="https://nrwone.in">NRWThemes</a>
</p>

