# kbd-auto-layout APT Repository

APT repository for `kbd-auto-layout`.

## Add the repository

```bash
curl -fsSL https://guarinogio.github.io/kbd-auto-layout-apt/public.key \
  | sudo gpg --dearmor --yes -o /usr/share/keyrings/kbd-auto-layout.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/kbd-auto-layout.gpg] https://guarinogio.github.io/kbd-auto-layout-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/kbd-auto-layout.list
```

## Install

```bash
sudo apt update
sudo apt install kbd-auto-layout
```

## Enable the service

```bash
systemctl --user daemon-reload
systemctl --user enable --now kbd-auto-layout.service
```

## Verify

```bash
apt policy kbd-auto-layout
kbd-auto-layoutctl --version
```

## Notes

- Repository URL: `https://guarinogio.github.io/kbd-auto-layout-apt`
- Distribution: `stable`
- Component: `main`
- Architecture: `amd64`

The source project lives here:

- `https://github.com/guarinogio/kbd-auto-layout`
