# Fluxo – Unraid Community Applications Template

Unraid template repository for **Fluxo**, a personal finance / household budgeting app.

This repo contains only the Unraid Docker template and Community Applications metadata
(`ca_profile.xml`, `templates/fluxo.xml`, `icon.svg`) — all MIT-licensed. The Fluxo application
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

## Support

Please open an [issue](https://github.com/SynShiftLabs/Fluxo_Unraid/issues) in this
repository for template/installation problems.
