# Muxtrix Scoop bucket

Public Scoop bucket for [Muxtrix](https://github.com/Phoenixmatrix/muxtrix).

## Install

Install Scoop, then add the bucket and install Muxtrix:

```powershell
scoop bucket add muxtrix https://github.com/Phoenixmatrix/scoop-muxtrix
scoop install muxtrix/muxtrix
```

## Update or uninstall

```powershell
scoop update
scoop update muxtrix
scoop uninstall muxtrix
```

The package adds a **Muxtrix** Start Menu shortcut and exposes `muxtrixctl` on
the command line. Application settings remain under `%APPDATA%\Muxtrix`, outside
Scoop's installation directory, so ordinary updates do not remove them.
