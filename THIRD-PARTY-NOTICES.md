# Third-party notices

KlausVFX ships with, or downloads on demand, the open-source components below. Each one is covered by its own
licence. KlausVFX's own licence (LICENSE.md) does not apply to them and does not limit your rights under them.

## Bundled in the installer

| Component | Licence | Source |
|---|---|---|
| **FFmpeg** (`ffmpeg.exe`, `ffprobe.exe`), build N-125875-g5d4d3bdc61-20260731, from BtbN/FFmpeg-Builds | GPL-3.0-or-later (built with `--enable-gpl --enable-version3`) | FFmpeg: https://git.ffmpeg.org/ffmpeg.git (commit `5d4d3bdc61`), build scripts: https://github.com/BtbN/FFmpeg-Builds |
| **Qt 6 / PySide6** 6.12 | LGPL-3.0 | https://code.qt.io, https://download.qt.io/official_releases/QtForPython/ |
| **Python** 3.12 | PSF License | https://www.python.org/downloads/source/ |
| **uv** 0.11 | MIT or Apache-2.0 | https://github.com/astral-sh/uv |
| **OpenTimelineIO** 0.18 (+ FCP XML, FCPX XML and AAF adapters) | Apache-2.0 | https://github.com/AcademySoftwareFoundation/OpenTimelineIO |
| **OpenColorIO** 2.6 (incl. the ACES studio config) | BSD-3-Clause | https://github.com/AcademySoftwareFoundation/OpenColorIO |
| **pyaaf2** 1.7 | MIT | https://github.com/markreidvfx/pyaaf2 |
| **NumPy** 2.5 | BSD-3-Clause | https://github.com/numpy/numpy |
| **Pillow** 13 | MIT-CMU | https://github.com/python-pillow/Pillow |
| **xxhash** (Python bindings) 4.0 | BSD-2-Clause | https://github.com/ifduyue/python-xxhash |
| **qrcode** 8.2 | BSD | https://github.com/lincolnloop/python-qrcode |
| **Send2Trash** 2.1 | BSD-3-Clause | https://github.com/arsenetar/send2trash |

FFmpeg runs as a separate program that KlausVFX starts; it is not linked into KlausVFX. You can replace the bundled
`ffmpeg\ffmpeg.exe` with any build you like, or point Settings at your own copy. On request, the author will also send
the exact FFmpeg source used for a given release: open an issue on https://github.com/sarmadvfx1/KlausVFX.

The Qt libraries are separate DLLs in the install folder (`_internal\PySide6`), which you may replace with your own
builds of the same version, as the LGPL allows.

## Downloaded on first use (AI packs and models)

| Component | Licence |
|---|---|
| PyTorch | BSD-3-Clause |
| torchvision | BSD-3-Clause |
| Hugging Face Transformers, Accelerate | Apache-2.0 |
| faster-whisper / CTranslate2 | MIT |
| ONNX Runtime | MIT |
| Whisper models (OpenAI) | MIT |
| SAM 2 / SAM 2.1 models (Meta) | Apache-2.0 |
| rembg and its models | MIT; see https://github.com/danielgatis/rembg for each model's licence |
| NVIDIA CUDA / cuDNN runtime libraries (GPU pack) | NVIDIA software licence |

The install folder contains this file and `LICENSE.md`. Its `licenses\` folder holds the full GPL-3.0 (FFmpeg) and
LGPL-3.0 (Qt) texts and the licence file of every other bundled library. The AI packs keep each package's licence
in its `*.dist-info` folder under `%LOCALAPPDATA%\KlausVFX\packs`.
