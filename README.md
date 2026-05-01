# kbd-auto-layout APT repository

Public APT repository for [`kbd-auto-layout`](https://github.com/guarinogio/kbd-auto-layout).

This repository contains the Debian package index, signed release metadata, public key, and `.deb` artifacts used by APT.

---

## Install

Add the signing key:

```bash
curl -fsSL https://guarinogio.github.io/kbd-auto-layout-apt/public.key \
  | sudo gpg --dearmor --yes -o /usr/share/keyrings/kbd-auto-layout.gpg
```

Add the APT source:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/kbd-auto-layout.gpg] https://guarinogio.github.io/kbd-auto-layout-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/kbd-auto-layout.list
```

Install:

```bash
sudo apt update
sudo apt install kbd-auto-layout
```

---

## Verify

```bash
apt policy kbd-auto-layout
kbd-auto-layoutctl --version
kbd-auto-layoutctl doctor
```

Expected:

```text
Candidate: 1.6.1
kbd-auto-layoutctl 1.6.1
```

---

## Enable the service

```bash
kbd-auto-layoutctl enable
```

---

## Project repository

Main project:

https://github.com/guarinogio/kbd-auto-layout

Releases:

https://github.com/guarinogio/kbd-auto-layout/releases

---

## Notes

- Distribution: `stable`
- Component: `main`
- Architecture: `amd64`
- Package: `kbd-auto-layout`
