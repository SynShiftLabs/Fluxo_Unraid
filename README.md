# Fluxo – Unraid Community Applications Template

Unraid template repository for **Fluxo**, a personal finance / household budgeting app.

This repo contains only the Unraid Docker template and Community Applications metadata
(`ca_profile.xml`, `templates/fluxo.xml`, `icon.png`) — all MIT-licensed. The Fluxo application
itself is closed-source and distributed only as a container image:

```
ghcr.io/synshiftlabs/fluxo:latest
```

## Installation

1. Unraid → **Apps** → **Settings** → **Template Repositories** → add:
   `https://github.com/SynShiftLabs/Fluxo_Unraid`
2. Search for "Fluxo" under **Apps** and install.
3. Fluxo needs an external PostgreSQL database — see the template's field descriptions for
   connection details, or the main [deployment guide](https://github.com/SynShiftLabs/Fluxo)
   for setting one up.
4. Default login after first start: `admin` / `admin` (change immediately).

## Troubleshooting

**After a Fluxo update, something looks off** (missing icon, missing field, container fails to
start with settings that used to work): Unraid deliberately does **not** re-sync an
already-installed container's configuration when this template changes — only the underlying
Docker image gets updated automatically. Template changes (new fields, icon format, etc.) only
take effect on a fresh install. Fix: remove the Fluxo container in Unraid (your data is safe —
it lives in the app-data volume and your external Postgres database, not in the container
itself) and reinstall it via **Apps** → search "Fluxo". This is standard Unraid behaviour, not
specific to this template — see the [Unraid forums](https://forums.unraid.net/topic/191930-update-docker-community-app-template/)
for background.

**Container stuck restarting after install**: check the container logs. The most common cause
is a wrong `DB_USER`/`DB_PASSWORD` for the Postgres database — double check those match what's
actually configured on your Postgres server.

## Support

Please open an [issue](https://github.com/SynShiftLabs/Fluxo_Unraid/issues) in this
repository for template/installation problems.
