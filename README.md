# AppForge — Release Channel

This repository hosts **release artifacts only**. It contains no source code.

The application's updater reads:

```
https://github.com/Archangel-77/appforge-releases/releases/latest/download/manifest.json
```

`manifest.json`:

```json
{
  "version": "1.0.1",
  "msi_url": "https://github.com/Archangel-77/appforge-releases/releases/download/v1.0.1/AppForge-1.0.1.msi",
  "sha256": "<sha256 of the MSI>",
  "notes": "..."
}
```

Each release also ships `SHA256SUMS.txt`. The installer verifies the MSI hash
from the manifest before running it, so an unsigned build is still
tamper-evident. Verify a manual download with:

```powershell
Get-FileHash .\AppForge-1.0.1.msi -Algorithm SHA256
```

Source code lives in a private repository.
