# Private Muxtrix Scoop bucket

This repository and the Muxtrix application repository are private. Installation
requires a GitHub account with read access to both
`Phoenixmatrix/scoop-muxtrix` and `Phoenixmatrix/muxtrix`.

## One-time setup

Install Scoop first, then configure Git and add this bucket over SSH:

```powershell
scoop install git
scoop bucket add muxtrix git@github.com:Phoenixmatrix/scoop-muxtrix.git
```

Private GitHub Release downloads require an individual fine-grained GitHub
token. The token must belong to the person installing Muxtrix, be restricted to
`Phoenixmatrix/muxtrix`, grant read-only repository Contents access, and have an
expiration date. Never commit, share, or add the token to a manifest.

Store it in Scoop's user configuration:

```powershell
scoop config gh_token THEIR_INDIVIDUAL_TOKEN
```

Alternatively, set it only for the current PowerShell process:

```powershell
$env:SCOOP_GH_TOKEN = "THEIR_INDIVIDUAL_TOKEN"
```

## Install, update, and uninstall

```powershell
scoop install muxtrix/muxtrix
scoop update
scoop update muxtrix
scoop uninstall muxtrix
```

The package adds a **Muxtrix** Start Menu shortcut and exposes `muxtrixctl` on
the command line. Application settings remain under `%APPDATA%\Muxtrix`, outside
Scoop's installation directory, so ordinary updates do not remove them.
