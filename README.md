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

It provides a responsive client area and matching order form experience with flexible layouts, color schemes, design styles, dark mode, and centralized configuration.

### Highlights

- **100% Unencoded Pure PHP** — Runs natively on PHP 8.1, 8.2, 8.3 and 8.4+.
- **No ionCube Loader Required** — No loader version mismatch when upgrading PHP.
- **Zero Licensing System** — No license keys, phone-home callbacks, or expiration checks.
- **WHMCS 9.x Ready** — Designed for WHMCS 9.x environments.
- **Flexible Configuration** — Manage the theme through the WHMCS admin addon or `theme-config.php`.
- **Responsive Design** — Mobile-first layout designed for desktop, tablet and mobile devices.

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

### 📐 Navigation Layouts

Choose from four different navigation layouts:

| Layout | Description |
|---|---|
| `default` | Clean top horizontal navigation bar |
| `condensed` | Compact single-row navigation with inline search |
| `left-nav` | Modern vertical sidebar navigation |
| `left-nav-wide` | Expanded vertical sidebar with additional descriptions |

### ✨ Design Styles

Nilom provides four design styles:

- `default`
- `modern`
- `depth`
- `futuristic`

### 🌓 Dark Mode

Built-in dark/light mode support with:

- Manual theme switcher
- Force dark mode
- Force light mode
- Automatic OS preference detection
- Cookie-based preference persistence

### 🛒 Matching Order Form

The included order form theme provides a matching shopping experience for:

- Product configuration
- Domain search
- Domain registration
- Domain renewal
- TLD selection
- Fraud checking
- Checkout
- Shopping cart

### ⚡ Performance

Nilom is designed to minimize unnecessary overhead:

- Pure PHP implementation
- No external licensing callbacks
- No license verification delays
- Lightweight theme configuration
- Optimized client-area assets

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
    │   └── ... (Smarty template files)
    │
    └── orderforms/
        └── nilom/
            ├── theme.yaml
            └── ... (Cart template files)
