# THAT GIRL AI 🎬

A Kaggle-based AI animation workspace for **THAT GIRL**.

## What this is

This repo is the setup hub for the AI animation pipeline we're building for the *THAT GIRL* project.

It is designed around:
- Kaggle GPU runtime
- 2× Tesla T4
- ComfyUI
- Wan 2.2 Animate 14B GGUF
- Gradio + ComfyUI API
- Reference-character animation / performance transfer

## Important

The large AI model files are **not stored in GitHub**. They are too large and have their own licensing terms.

The pipeline expects the required model assets to be attached to the Kaggle notebook as Kaggle Datasets under `/kaggle/input`.

## Quick start

1. Open the notebook:
   `wan-2-2-animate-gguf-comfyui-gradio.ipynb`
2. Import it into Kaggle.
3. Turn on **GPU: T4 ×2**.
4. Attach the required Kaggle model datasets.
5. Run the notebook from the top.
6. Use the Gradio interface when it appears.

## Required model datasets

The current pipeline expects these Kaggle input directories:

- `wan-animate-q6-k-gguf`
- `wan-animate-gguf-text-encoder`
- `wan-animate-vae`
- `wan-animate-loras`
- `wan-animate-clip-vision`
- `wan-animate-custom-nodes`
- `wan-video-workflow`

## Upstream project

The underlying Kaggle implementation is based on the public Wan 2.2 Animate Kaggle project by kelvinweijun:

https://github.com/kelvinweijun/wan-2.2-animate-comfyui-kaggle

Model files come from the respective Hugging Face repositories referenced by that project.

## What comes next

This is the **animation engine**, not the entire finished microdrama system yet. After the engine is working, we'll add the THAT GIRL layer: character bible, scene inputs, dialogue/voice, lip-sync, shot assembly, continuity, and episode rendering.
