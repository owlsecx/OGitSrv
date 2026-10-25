# 🦉 OGitSrv

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OGitSrv** — Self-Hosted Git Server Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OGitSrv — Self-Hosted Git Server Auditor. It provides offline, read-only audit of Git SERVER configuration (never touches repositories — see OGitSec for that). Built-in demo/self-test paths and severity gates help validate detections without touching production when those flags are used.

---

## ✨ Features

- Offline, read-only audit of Git SERVER configuration (never touches repositories — see OGitSec for that)
- Gitea / Forgejo app.ini analyzer — INSTALL_LOCK, SECRET_KEY / INTERNAL_TOKEN strength (masked), open registration, 2FA enforcement, webhook SSRF allow- lists, migrations to local networks, pprof / debug, session cookies
- GitLab Omnibus gitlab.rb analyzer — external_url TLS, signup, initial root password, Rack::Attack, local requests from webhooks, monitoring allow-lists, PostgreSQL / Redis binds, LDAP, OmniAuth, nginx TLS
- gitolite.conf + .gitolite.rc — @all write access, GIT_CONFIG_KEYS, UMASK, risky features
- git-daemon (systemd / xinetd / defaults) — export-all, receive-pack, base-path, root execution
- cgitrc — filters, scan-path, git-config, clone URLs

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OGitSrv <paths>
./OGitSrv <paths> --type
./OGitSrv <paths> --discover
./OGitSrv --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
