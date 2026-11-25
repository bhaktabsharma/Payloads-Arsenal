# 🔫 Bug Bounty Payload Arsenal

A fast, offline, browser-based payload reference tool for web application security testing and bug bounty hunting. No login. No tracking. No internet required after setup.

---

## 🌐 Live Demo

> **https://YOUR-USERNAME.github.io/payload-arsenal/**

*(Replace with your actual GitHub Pages URL after deployment)*

---

## 📸 Preview

```
┌─────────────────────────────────────────────────────────────────┐
│ 🔫 Bug Bounty Payload Arsenal    Categories: 25  Payloads: 812  │
├──────────────────────┬──────────────────────────────────────────┤
│ 🔍 Search categories │ XSS - Basic               [ Copy All ]   │
├──────────────────────│                                          │
│ XSS - Basic      40  │ <script>alert(1)</script>     [ Copy ]   │
│ XSS - Bypass     40  │ <img src=x onerror=alert(1)>  [ Copy ]   │
│ SQL Injection    40  │ <svg onload=alert(1)>          [ Copy ]   │
│ SSRF             41  │ javascript:alert(1)            [ Copy ]   │
│ LFI / Traversal  40  │ ...                                      │
│ RCE / Cmd Inject 39  │                                          │
│ XXE              39  │                                          │
│ CSRF             39  │                                          │
│ ...                  │                                          │
└──────────────────────┴──────────────────────────────────────────┘
```

---

## ✨ Features

- **812 payloads** across **25 vulnerability categories**
- Instant **search** to filter categories
- **Copy** individual payloads with one click
- **Copy All** to grab every payload in a category at once
- **100% offline** after page load — no external dependencies
- Works in **any modern browser** (Chrome, Firefox, Edge, Safari)
- Clean **dark theme** optimized for long testing sessions
- **No login**, no account, no tracking, no ads

---

## 📂 Payload Categories

| Category | Payloads |
|---|:-:|
| XSS - Basic | 40 |
| XSS - Encoded / Bypass | 40 |
| SQL Injection - Basic | 40 |
| SQL Injection - Encoded / Bypass | 40 |
| SSRF | 41 |
| LFI / Path Traversal | 40 |
| RCE / Command Injection | 39 |
| XXE | 39 |
| CSRF | 39 |
| IDOR | 40 |
| Open Redirect | 40 |
| SSTI | 34 |
| NoSQL Injection | 30 |
| LDAP Injection | 22 |
| XML Injection | 20 |
| File Upload | 41 |
| Authentication Bypass | 33 |
| JWT | 26 |
| GraphQL | 25 |
| WebSocket | 17 |
| HTTP Request Smuggling | 19 |
| CORS Misconfiguration | 15 |
| Host Header Injection | 20 |
| WAF Bypass / Encoding Reference | 42 |
| Misc / Important | 30 |
| **TOTAL** | **812** |

---

## 🚀 Deploy to GitHub Pages

### Step 1 — Fork or create repo

```
1. Click "Use this template" or create a new public repository
2. Name it anything, e.g. payload-arsenal
```

### Step 2 — Upload files

Make sure these two files are in the root of your repo:

```
payload-arsenal/
├── index.html
└── payloads.json
```

### Step 3 — Enable GitHub Pages

```
Repo → Settings → Pages → Source: Deploy from branch → Branch: main / root → Save
```

Your site will be live in ~60 seconds at:

```
https://YOUR-USERNAME.github.io/REPO-NAME/
```

---

## 💻 Run Locally

No build tools or server required for local use:

**Option 1 — Python (recommended)**
```bash
git clone https://github.com/YOUR-USERNAME/payload-arsenal.git
cd payload-arsenal
python3 -m http.server 8080
# Open http://localhost:8080
```

**Option 2 — Node.js**
```bash
npx serve .
# Open http://localhost:3000
```

**Option 3 — VS Code**

Install the **Live Server** extension → right-click `index.html` → Open with Live Server

> ⚠️ Opening `index.html` directly as a `file://` URL will not work because the browser blocks `fetch()` for local files. Use a local server.

---

## 🔧 Add or Expand Payloads

All payloads live in a single file: **`payloads.json`**

### Add payloads to an existing category

```json
"WebSocket": [
    "ws://target.com/socket",
    "wss://target.com/socket",
    "YOUR NEW PAYLOAD HERE"
]
```

### Add a new category

```json
"OAuth Attacks": [
    "redirect_uri=https://evil.com",
    "response_type=token%20id_token",
    "state=CSRF-TEST-VALUE"
]
```

### Rules

- Each payload is a **string in double quotes**
- Separate payloads with **commas** (no comma after the last one)
- Separate categories with **commas** (no comma after the last category)
- Escape internal double quotes as `\"`
- Validate JSON before committing at [jsonlint.com](https://jsonlint.com)

---

## 🦊 Firefox Extension Version

This tool also exists as a Firefox sidebar/popup extension.

### Files needed

```
payload-arsenal-extension/
├── manifest.json
├── sidebar.html
├── sidebar.js
├── styles.css
├── payloads.json
└── icon.png
```

### Load in Firefox

```
1. Go to about:debugging#/runtime/this-firefox
2. Click "Load Temporary Add-on"
3. Select manifest.json from the extension folder
4. Click the extension icon in the toolbar
```

---

## 🖥️ Use as a Side Panel During Testing

**Firefox / Chrome:**
```
Right-click the tab → Move to New Window → Snap to side of screen
```

**Windows Snap:**
```
Drag the window to the left or right edge of your screen
```

This lets you keep the payload tool visible alongside Burp Suite, browser DevTools, or your proxy.

---

## 📁 Project Structure

```
payload-arsenal/
├── index.html        ← Full web app (HTML + CSS + JS in one file)
├── payloads.json     ← All payload data (edit this to add payloads)
└── README.md         ← This file
```

---

## ⚠️ Disclaimer

This tool is intended **strictly for authorised security testing**, including:

- Bug bounty programs where you have explicit permission
- Penetration testing engagements with a signed scope agreement
- Personal lab environments and CTF challenges
- Security research and education

**Using these payloads against systems you do not have explicit written permission to test is illegal and unethical.** The author takes no responsibility for misuse.

Always follow:
- Your bug bounty program's scope and rules
- Responsible disclosure practices
- Local laws and regulations

---

## 📜 License

MIT License — free to use, modify, and distribute with attribution.

---

<div align="center">
  Made for the bug bounty and security research community<br>
  <strong>Test legally. Disclose responsibly. Stay curious.</strong>
</div>
