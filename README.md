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

Offline auditor for self-hosted Git server configuration (Gitea/Forgejo, GitLab, gitolite, git-daemon, cgit)

---

## ✨ Features

- Offline, read-only audit of Git SERVER configuration (never touches repositories — see OGitSec for that)
- Gitea / Forgejo app.ini analyzer — INSTALL_LOCK, SECRET_KEY / INTERNAL_TOKEN strength (masked), open registration, 2FA enforcement, webhook SSRF allow- lists, migrations to local networks, pprof / debug, session cookies, CORS, LFS / packages exposure, SSH
- GitLab Omnibus gitlab.rb analyzer — external_url TLS, signup, initial root password, Rack::Attack, local requests from webhooks, monitoring allow-lists, PostgreSQL / Redis binds, LDAP, OmniAuth, nginx TLS
- gitolite.conf + .gitolite.rc — @all write access, GIT_CONFIG_KEYS, UMASK, risky features
- git-daemon (systemd / xinetd / defaults) — export-all, receive-pack, base-path, root execution
- cgitrc — filters, scan-path, git-config, clone URLs
- File permission / ownership checks on the configs
- 129 rules with severity, CWE, MITRE ATT&CK, remediation
- Score 0-100 + grade A+…F, hardened templates
- TXT / MD / JSON / CSV / SARIF exports, --fail-on CI gate
- --demo self-test, --list-rules, --explain RULE

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OGitSrv
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
