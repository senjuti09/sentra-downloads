# Sentra 1.0.0: downloads for testers

Sentra is a passwordless desktop authenticator and personal security center for Windows and macOS, built for the IIIT-Delhi Usable Security & Privacy course (test week **18–25 November 2026**).

**Get the files from the [v1.0.0 release](https://github.com/senjuti09/sentra-downloads/releases/tag/v1.0.0).**

| File | For |
|---|---|
| `Sentra-Setup-1.0.0.exe` | Windows 10/11 installer (per-user, no admin needed) |
| `Sentra-1.0.0-win-x64.zip` | Windows without installing: unzip and run `Sentra.exe` |
| `Sentra-1.0.0-universal.dmg` | macOS 12+, Intel and Apple silicon |
| `Sentra-User-Guide.pdf` | How to install, the 10 tasks, troubleshooting, testing rules |
| `SHA256SUMS.txt` | Checksums |

**Read the user guide first.** The builds are not signed with paid certificates, so Windows SmartScreen ("More info → Run anyway") and macOS Gatekeeper ("Open Anyway") warn the first time; the guide shows the exact clicks.

## Check your download

```
Windows (PowerShell):  Get-FileHash .\Sentra-Setup-1.0.0.exe -Algorithm SHA256
macOS (Terminal):      shasum -a 256 ~/Downloads/Sentra-1.0.0-universal.dmg
```

```
6574d005493d30432ad70a81e21224a22623024308f0c207182b87fc04d74fa1  Sentra-1.0.0-universal.dmg
c12a46bf69e0cd5521205a7ad12dc09093c2765cef44f3356e27812322380c90  Sentra-1.0.0-win-x64.zip
3bf06ec40dfc5a8ea6fdec6cb8296fab53159376bc980f64978eb8d33ee1911c  Sentra-Setup-1.0.0.exe
7818d7cb006a552377bce75768cfaf2275618ccd22506b5557cb5ba7ac4f3561  Sentra-User-Guide.pdf
```

## Server

- API: `https://sentra.tail658f33.ts.net` (built into the app)
- Campus Portal (demo website that signs in with Sentra): `https://sentra.tail658f33.ts.net/portal`

## Testing rules (short version)

- **In scope:** the Sentra app, the API and Campus Portal, with accounts **you created yourself**.
- **Out of scope:** denial of service, other people's accounts, social engineering, the host machine beyond the API, third-party services.
- **Report findings** by email to **sayan20012002@gmail.com**: steps, what happened, why it matters, your OS. Please don't post working exploits publicly before 25 November.

Full rules: section 15 of the user guide.
