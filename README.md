# 1Click SeedVR2.5

One-click video & image upscaler powered by ByteDance's SeedVR2 model — wrapped in a simple Windows GUI with TensorRT-accelerated VAE decoding.

> This is the official continuation of the 1Click_SeedVR2.5 project (previous account unavailable).

## Download

Get the latest installer from [Releases](../../releases).

The installer offers optional downloads:
- **Embedded Python** (~2.2 GB) — the complete runtime, no system Python needed
- **AI Models** (~4 GB) — SeedVR2 3B model + VAE weights

## Highlights

- **One click** — drop a video, pick a scale, hit export
- **VAE RT (TensorRT)** — VAE decode runs through a TensorRT engine; engines are downloaded automatically for your GPU (RTX 50 series) and cached
- **384 px engine tier** — much faster decode on 16 GB GPUs
- **Image upscaling** — dedicated 1024 px / 1-frame engine, decode in ~1 second
- **MXF (ProRes OP-1a) support** — broadcast containers accepted directly
- **Built-in MPV preview** with split-view compare (original vs result)
- **Auto Tune** — automatically picks safe batch/tile settings for your GPU
- **Send Logs** — one-click diagnostic bundle to the developer
- **In-app updates**

## Requirements

- Windows 10/11 x64
- NVIDIA RTX GPU (RTX 30/40/50 series; RTX 50 recommended)
- ~6 GB free disk space for runtime + models

## Usage

1. Install the setup
2. Launch `1Click_SeedVR2.5.exe`
3. Drop a video, choose the output scale (2x recommended), press Export

## Building from source

- GUI: PySide6, located in `gui/`
- CLI engine: `seedvr2_videoupscaler/inference_cli.py`
- Windows installer: Inno Setup script in `backup/iss/`

## Acknowledgements

- [ByteDance SeedVR2](https://github.com/ByteDance-Seed/SeedVR2) — the underlying model
- [llama.cpp GGUF](https://github.com/ggml-org/llama.cpp) — quantized weight format
- [mpv](https://mpv.io/) — embedded preview player
- [SageAttention](https://github.com/thu-ml/SageAttention) — attention acceleration
