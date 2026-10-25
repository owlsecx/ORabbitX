# 🦉 ORabbitX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ORabbitX** — Offline RabbitMQ Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ORabbitX is an offline configuration auditor for RabbitMQ. It parses rabbitmq.conf, Erlang-style rabbitmq.config/advanced.config, enabled_plugins and definitions.json exports to flag insecure defaults, listener and TLS issues, and weak credentials. Secrets are masked and findings map to CWE and MITRE ATT&CK.

---

## ✨ Features

- rabbitmq.conf (sysctl) and conf.d merge parser plus a tolerant Erlang-term parser
- Guest/loopback/default-user/anonymous access rules
- Listener, TLS, management and MQTT/STOMP checks
- definitions.json analysis with cleartext detection, hash guessing and shovel URI review
- Erlang cookie and file-permission auditing with offline --root discovery
- TXT/MD/JSON/CSV/SARIF export, self-test and CI gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORabbitX -c /etc/rabbitmq/rabbitmq.conf
./ORabbitX -d definitions.json --sarif -o report.sarif
./ORabbitX --scan --root /mnt/collected --fail-on high
./ORabbitX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
