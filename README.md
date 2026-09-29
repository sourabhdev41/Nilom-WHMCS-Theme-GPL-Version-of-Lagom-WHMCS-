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
