# Installing Lumitag

## Download

1. Go to [Releases](../../releases) and download the latest `Lumitag_Setup_x.x.x.exe`.

## SmartScreen warning

Windows will probably show a blue "Windows protected your PC" screen. This happens because the installer isn't code-signed (code signing certificates cost $200-400/year — not worth it for a solo project at this stage).

**The app is safe.** You can verify by checking the source code structure in this repo, or by scanning the installer with your antivirus.

To proceed:

1. Click **"More info"** (the small text link, easy to miss)
2. Click **"Run anyway"**

*(screenshot placeholder: smartscreen_1.png — the blue warning screen)*
*(screenshot placeholder: smartscreen_2.png — after clicking "More info", showing "Run anyway" button)*

## Installation

The installer is straightforward:

1. Accept the license agreement
2. Choose install location (default: `%LOCALAPPDATA%\Programs\Lumitag`)
3. Click Install
4. Launch Lumitag

**No admin rights needed.** Lumitag installs to your user folder, not Program Files.

## First run

On first launch, Lumitag will:

1. Check your system (Python, GPU, disk space)
2. Install required Python packages (~500 MB)
3. You're ready to tag

AI models are downloaded on-demand when you first use each tagging mode (~300 MB - 2 GB depending on mode).

## Uninstalling

Use "Add or remove programs" in Windows Settings, or run the uninstaller from the Start Menu. Your settings and usage data are stored in the Windows registry under `HKCU\Software\Lumitag` — the uninstaller removes these too.

Log files in `%LOCALAPPDATA%\Lumitag\logs\` are not removed automatically. Delete them manually if you want.

## Troubleshooting

**App won't start?** Check the log file in `%LOCALAPPDATA%\Lumitag\logs\` — the latest `.log` file will have the error.

**Models won't download?** Make sure you have internet access and ~2 GB free disk space. Models are cached in `%USERPROFILE%\.cache\huggingface\`.

**GPU not detected?** Lumitag needs NVIDIA GPU with CUDA support. AMD and Intel GPUs are not supported yet. Make sure you have recent NVIDIA drivers installed.

**Still stuck?** [Open an issue](../../issues) and attach your log file.
