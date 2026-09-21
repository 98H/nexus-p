# Deployment & Operations Guide: P

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-p-64e5af/](/preview/prod-p-64e5af/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-21T09:47:59.318794+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=P Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/tmpzkfgus5j/workspaces/prod-p-64e5af
ExecStart=/usr/bin/python3 /tmp/tmpzkfgus5j/workspaces/prod-p-64e5af/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
