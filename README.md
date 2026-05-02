# Lumitag

AI photo tagger for Windows. Point it at a folder, pick a tagging mode, and Lumitag writes keywords straight into your photos' EXIF/IPTC/XMP metadata. Works with Lightroom, digiKam, Bridge, and anything else that reads standard photo metadata.

## What it does

Lumitag runs multiple AI models locally on your machine — no cloud, no uploads, no subscriptions. Your photos never leave your computer.

- **Scene recognition** — landscapes, portraits, architecture, food, sports, and 30+ scene types
- **Object detection** — people, animals, vehicles, furniture, electronics — 80 object categories
- **Image captioning** — natural language descriptions written to EXIF
- **Content tagging** — thousands of visual tags from anime-trained models (surprisingly good on real photos)
- **OCR** — reads text in photos (signs, documents, receipts)
- **Translation** — tags in English, Polish, German, French, Spanish, and 6 more languages

## Tagging modes

Pick a mode and go:

- **Szybki / Quick** (~3s/photo) — scene + objects. Good enough for most libraries.
- **Standardowy / Standard** (~6s/photo) — adds content tags. The sweet spot.
- **Optymalny / Optimal** (~12s/photo) — adds AI captions. For archivists who want everything.
- **Własny / Custom** — pick exactly which models to run.

Times are for CPU. GPU (NVIDIA) is 3-5× faster.

## Screenshots

See screenshots and more at **[lumitag.netlify.app](https://lumitag.netlify.app)**

## Download

Grab the latest installer from [Releases](../../releases).

**Windows 10/11.** No Python needed — everything is bundled.

> **SmartScreen warning?** Windows may show "Windows protected your PC" because the installer isn't code-signed yet. Click "More info" → "Run anyway". See [installation guide](INSTALL.md) for details.

## Free vs Pro

Lumitag is free for 100 photos. All models, all modes, no restrictions — just a limit on how many photos you can process.

Need more? **Lumitag Pro** removes the limit entirely. One-time purchase, no subscription.

**[Buy Lumitag Pro → lumitag.netlify.app](https://lumitag.netlify.app/#pricing)**

## Installation guide

See [INSTALL.md](INSTALL.md) for step-by-step instructions, including the SmartScreen workaround.

## Support

**Found a bug?** [Open an issue](../../issues) — include the log file from `%LOCALAPPDATA%\Lumitag\logs\`.

**Question or feedback?** lumitag.support@gmail.com

## Models

Lumitag uses these open-source AI models (downloaded on first use):

- **SigLIP** — scene classification (Apache 2.0)
- **RT-DETR** — object detection (Apache 2.0)
- **WD Tagger** — content tagging (Apache 2.0)
- **Florence-2** — image captioning (MIT)
- **EasyOCR** — text recognition (Apache 2.0)

GPU users can also enable **Joy-Caption** for premium-quality captions (requires NVIDIA GPU with 6+ GB VRAM).

## Tech

Built with Python, PySide6, and HuggingFace Transformers. Runs on embedded Python — no system Python required. Tags written via ExifTool.

## License

Lumitag is proprietary software. See [EULA](EULA.md) for terms.

Third-party licenses: see `LICENSES/THIRD_PARTY_LICENSES.txt` in the installation directory.
